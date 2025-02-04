# Unhandled JSON Decoding Exception in Dart

This repository demonstrates a common error in Dart applications that use the `http` package to fetch JSON data and how to fix it.

The `bug.dart` file shows the original code with the unhandled exception. The `bugSolution.dart` demonstrates how to correctly handle the potential `FormatException` thrown by `jsonDecode`.

## Problem

The original code doesn't handle the case where the API response is not valid JSON. If this occurs, `jsonDecode` will throw a `FormatException`, resulting in an unhandled exception and the application may crash.

## Solution

The improved code adds a `try-catch` block around `jsonDecode` to handle the `FormatException`.  This prevents application crashes and allows for graceful error handling.