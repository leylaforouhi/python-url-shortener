import hashlib

def shorten_url(url):
    # Create a unique 8-character hash for the URL
    url_hash = hashlib.md5(url.encode()).hexdigest()[:8]
    print(f"Original URL: {url}")
    print(f"Shortened ID: {url_hash}")
    return url_hash

if __name__ == "__main__":
    link = "https://www.github.com/your-long-profile-link-example"
    shorten_url(link)
