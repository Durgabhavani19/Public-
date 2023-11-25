def detect_fake_news(news):
    # Basic rules for fake news detection
    if "BREAKING" in news.upper() and "CONFIRMED" not in news.upper():
        return "Likely fake news"
    elif "EXCLUSIVE" in news.upper():
        return "Possibly biased news"
    else:
        return "Seems legitimate"

# Example usage
news_article = "BREAKING: UFOs spotted in the White House! CONFIRMED by anonymous sources."
result = detect_fake_news(news_article)
print(result)
