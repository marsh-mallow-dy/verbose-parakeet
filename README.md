# verbose-parakeet
Im lazy so I will not finish this
response = requests.get(url, stream=True)
        response.raise_for_status()

        # Create target directory if it doesn't exist
        os.makedirs(os.path.dirname(save_path), exist_ok=True)
