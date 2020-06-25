val alphabet = charArrayOf('A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','W','X','Y','Z')

fun vigenere(text: String, keyword: String): String {
    val textList = text.toMutableList()
    val keyList = keyword.toMutableList()
    val output = mutableListOf<Char>()
    var loopCount: Int = 0

    for (char in textList) {
        val index = alphabet.indexOf(char)
        val key = alphabet.indexOf(keyword[loopCount])
        var offset = index + key
        loopCount++

        if (offset >= 26) offset -= 26
        output.add(alphabet[offset])
    }

    return output.joinToString(separator = "")
}

fun generateKey(text: String, key: String): String {
    val keyList = key.toMutableList()
    val generatedKey = mutableListOf<Char>()

    for (i in 0..text.length) {
        for (char in keyList) {
            if (text.length == generatedKey.size) break
            generatedKey.add(char)
        }
    }
    return generatedKey.joinToString(separator = "")
}

fun main() {
    val text = "GEEKSFORGEEKS"
    val key = generateKey(text, "AYUSH")

    println(vigenere(text, key))
}
