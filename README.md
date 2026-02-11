open class IAM(
    val name: String = "Ramen",
    val aka: String = "beyalora",
    val about: String = "Coding is my primary work",
    val languages: Array<String> = arrayOf(
        "Kotlin",
        "Java",
        "JavaScript"
    ),
    val editors: Array<String> = arrayOf(
        "Me",
        "Im",
        "Ramen",
    ),
    val activities: Array<String> = arrayOf(
        "Cycling",
        "Designing",
        "Debloating",
        "Exploring",
    ),
    val status: String = "Noob!",
) {
    operator fun invoke(action: IAM.() -> Unit) = this.apply(action)

    override fun toString() =
        """
        | Intro:  $name ($aka): $about
        | Langs:  ${languages.joinToString(", ")}
        | Editor: ${editors.joinToString(", ")}
        | Hobby:  ${activities.joinToString(", ")}
        | Status: $status
        """.trimMargin()
}
