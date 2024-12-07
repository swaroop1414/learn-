from collections import Counter

def read_fasta(filename):
    """Reads a FASTA file and returns the sequence as a string."""
    sequence = ""
    with open(filename, "r") as file:
        for line in file:
            if not line.startswith(">"):  
                sequence += line.strip()
    return sequence

def nucleotide_counts(sequence):
    """Returns a dictionary with nucleotide counts."""
    return Counter(sequence)

def calculate_gc_content(sequence):
    """Returns the GC content as a percentage."""
    gc_count = sequence.count('G') + sequence.count('C')
    return (gc_count / len(sequence)) * 100

def reverse_complement(sequence):
    """Returns the reverse complement of a DNA sequence."""
    complement = {'A': 'T', 'T': 'A', 'G': 'C', 'C': 'G'}
    rev_comp = "".join(complement[nuc] for nuc in reversed(sequence))
    return rev_comp

if __name__ == "__main__":
    # Sample FASTA file path
    fasta_file = r"C:\Users\swaro\Downloads\sequence.fasta" 
    # Read the sequence
    dna_sequence = read_fasta(fasta_file)
    
    # Perform analysis
    print("DNA Sequence Analysis:")
    print(f"Length of sequence: {len(dna_sequence)}")
    
    # Nucleotide counts
    counts = nucleotide_counts(dna_sequence)
    print("Nucleotide Counts:", counts)
    
    # GC content
    gc_content = calculate_gc_content(dna_sequence)
    print(f"GC Content: {gc_content:.2f}%")
    
    # Reverse complement
    rev_comp = reverse_complement(dna_sequence)
    print("Reverse Complement:", rev_comp)
