ytmusicapi: Unofficial API for YouTube Music
############################################

.. image:: https://img.shields.io/pypi/dm/ytmusicapi?style=flat-square
    :alt: PyPI Downloads
    :target: https://pypi.org/project/ytmusicapi/

.. image:: https://img.shields.io/codecov/c/github/sigma67/ytmusicapi?style=flat-square
    :alt: Code coverage
    :target: https://codecov.io/gh/sigma67/ytmusicapi

.. image:: https://img.shields.io/github/v/release/sigma67/ytmusicapi?style=flat-square
    :alt: Latest release
    :target: https://github.com/sigma67/ytmusicapi/releases/latest

.. image:: https://img.shields.io/github/commits-since/sigma67/ytmusicapi/latest?style=flat-square
    :alt: Commits since latest release
    :target: https://github.com/sigma67/ytmusicapi/commits


A work-in-progress API that emulates web requests from the YouTube Music web client.

Currently you need to extract your authentication data from your web browser and provide it through a file for it to work.

.. features

Features
--------
| **Browsing**:

* get artist information and releases (songs, videos, albums, singles)
* get albums
* search (including all filters)

| **Library management**:

* get library contents: playlists, songs, artists, albums and subscriptions
* add/remove library content: rate songs, albums and playlists, subscribe/unsubscribe artists

| **Playlists**:

* create, delete, and modify playlists
* get playlist contents, add/remove tracks

| **Uploads**:

* Upload songs and remove them again
* List uploaded songs, artists and albums


Usage
------
.. code-block:: python

    from ytmusicapi import YTMusic

    ytmusic = YTMusic('headers_auth.json')
    playlistId = ytmusic.create_playlist("test", "test description")
    search_results = ytmusic.search("Oasis Wonderwall")
    ytmusic.add_playlist_items(playlistId, [search_results[0]['videoId']])

The `tests <https://github.com/sigma67/ytmusicapi/blob/master/tests/test.py>`_ are also a great source of usage examples.

.. end-features

Requirements
==============

- Python 3.5 or higher - https://www.python.org

Setup and Usage
===============

See the `Documentation <https://ytmusicapi.readthedocs.io/en/latest/usage.html>`_ for detailed instructions

Contributing
==============

Pull requests are welcome. There are still some features that are not yet implemented.
Please, refer to `CONTRIBUTING.rst <https://github.com/sigma67/ytmusicapi/blob/master/CONTRIBUTING.rst>`_ for guidance.