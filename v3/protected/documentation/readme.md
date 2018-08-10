Calls can be done with basic authentication though other options exist (e.g. oauth).

**Important**: you _have_ to pass in a User-Agent, otherwise you get a mysterious 403: https://developer.github.com/v3/#user-agent-required

Glue example to create a repository for an organisation:

```python
nabu.integrations.github.v3.swagger.services.postOrgsOrgRepos(
	parameters: structure(
		org: organisation,
		body: structure(name: project)
	),
	authentication: structure(username: username, password: password),
	headers: series(structure(name: "User-Agent", value: "Nabu")))
```