# ![LOGO](logo.png) Jira **flow**ground Connector

## Description

A generated **flow**ground connector for the Jira API (version v3).

Generated from: https://api.apis.guru/v2/specs/atlassian.com/jira/v3/swagger.json<br/>
Generated at: 2019-05-07T17:37:00+03:00

## API Description

The Jira Cloud Platform REST API

## Authorization

Supported authorization schemes:
- Basic Authentication
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Returns all application properties or a single application property.

#### Input Parameters
* `key` - _optional_ - The key of the application property.
* `keyFilter` - _optional_ - When a key isn't provided, this filters the list of results by the application property key using a regular expression. For example, using jira.lf.* will return all application properties with keys that start with jira.lf..
* `permissionLevel` - _optional_ - The permission level of all items being returned in the list.

### Returns the application properties that are accessible on the Advanced Settings page. To navigate to the Advanced Settings page in Jira, choose the Jira icon > Jira settings > System, General Configuration and then click Advanced Settings (in the upper right).

### Changes the value of an application property. For example, you can change the value of the jira.clone.prefix from its default value of CLONE - to Clone - if you prefer sentence case capitalization. Editable properties are described below along with their default values.

#### Input Parameters
* `id` - _required_ - The key of the application property to update.

### Returns all application roles. In Jira, application roles are managed using the Application access configuration page.

### Returns an application role.

#### Input Parameters
* `key` - _required_ - The key of the application role. Use the Get all application roles method to get the key for each application role.

### Returns the global attachment settings, that is, whether attachments are enabled and the maximum attachment size allowed.

### Deletes an attachment from an issue.

#### Input Parameters
* `id` - _required_ - The ID of the attachment.

### Returns the metadata for an attachment. Note that the attachment itself is not returned.

#### Input Parameters
* `id` - _required_ - The ID of the attachment.

### Returns the metadata for the contents of an attachment, if it is an archive, and metadata for the attachment itself. For example, if the attachment is a ZIP archive, then information about the files in the archive is returned and metadata for the ZIP archive. Currently, only the ZIP archive format is supported.

#### Input Parameters
* `id` - _required_ - The ID of the attachment.

### Returns the metadata for the contents of an attachment, if it is an archive. For example, if the attachment is a ZIP archive, then information about the files in the archive is returned. Currently, only the ZIP archive format is supported.

#### Input Parameters
* `id` - _required_ - The ID of the attachment.

### Returns a list of audit records. The list can be filtered to include items:

#### Input Parameters
* `filter` - _optional_ - The query string.
* `from` - _optional_ - The date and time on or after which returned audit records must have been created. If to is provided from must be before to or the result set will be empty.
* `limit` - _optional_ - The maximum number of results to return. The maximum is 1000.
* `offset` - _optional_ - The number of records to skip before returning the first result.
* `to` - _optional_ - The date and time on or before which returned audit results must have been created. If from is provided to must be after from or the result set will be empty.

### Returns a list of system avatar details by owner type, where the owner types are issue type, project, or user.

#### Input Parameters
* `type` - _required_ - The avatar type.

### Returns the comments for a list of comment IDs.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about comments in the response. This parameter accepts multiple values separated by a comma:
    Possible values: renderedBody, properties.

### Returns the keys of all the properties of a comment.

#### Input Parameters
* `commentId` - _required_ - The ID of the comment.

### Deletes a comment property.

#### Input Parameters
* `commentId` - _required_ - The ID of the comment.
* `propertyKey` - _required_ - The key of the property.

### Returns the value of a comment property.

#### Input Parameters
* `commentId` - _required_ - The ID of the comment.
* `propertyKey` - _required_ - The key of the property.

### Creates or updates the value of a property for a comment. Use this resource to store custom data against a comment.

#### Input Parameters
* `commentId` - _required_ - The ID of the comment.
* `propertyKey` - _required_ - The key of the property. The maximum length is 255 characters.

### Creates a component. Use components to provide containers for issues within a project. Permissions required: Any of the following:

### Deletes a component. Permissions required: Any of the following:

#### Input Parameters
* `id` - _required_ - The ID of the component.
* `moveIssuesTo` - _optional_ - The ID of the component to replace the deleted component. If this value is null no replacement is made.

### Returns a component. Permissions required: Browse projects project permission.

#### Input Parameters
* `id` - _required_ - The ID of the component.

### Modifies a component. Any fields included in the request are overwritten. If leadUserName is an empty string ("") the component lead is removed. Permissions required: Any of the following:

#### Input Parameters
* `id` - _required_

### Returns the counts of issues assigned to the component. Permissions required: Permission to access Jira.

#### Input Parameters
* `id` - _required_ - The ID of the component.

### Returns the global settings in Jira. These settings determine whether optional features (for example, sub-tasks, time tracking, and others) are enabled. If time tracking is enabled, this method also returns the time tracking configuration.

### Disables time tracking.

### Returns the time tracking provider that is currently selected. Note that if time tracking is disabled, then a successful but empty response is returned.

### Selects a time tracking provider.

### Returns all time tracking providers. By default, Jira only has one time tracking provider: JIRA provided time tracking. However, you can install other time tracking providers via apps from the Atlassian Marketplace. For more information on time tracking providers, see the documentation for the Time Tracking Provider module.

### Returns the time tracking settings. This includes settings such as the time format, default time unit, and others. For more information, see Configuring time tracking.

### Sets the time tracking settings.

### Returns a custom field option. For example, an option in a cascading select list.

#### Input Parameters
* `id` - _required_ - The ID of the custom field option. To find this ID, configure the custom field and edit its options in Jira. Click the option and its ID will show in the URL as the selectedParentOptionId parameter.

### Returns a list of dashboards owned by or shared with the user. The list may be filtered to include only favorite or owned dashboards.

#### Input Parameters
* `filter` - _optional_ - The filter applied to the list of dashboards. Valid values are:
    Possible values: favourite, my.
* `maxResults` - _optional_ - The maximum number of items to return per page. Maximum is 1000.
* `startAt` - _optional_ - The index of the first item to return in a page of results (page offset).

### Returns the keys of all properties for a dashboard item.

#### Input Parameters
* `dashboardId` - _required_ - The ID of the dashboard.
* `itemId` - _required_ - The ID of the dashboard item.

### Deletes a dashboard item property.

#### Input Parameters
* `dashboardId` - _required_ - The ID of the dashboard.
* `itemId` - _required_ - The ID of the dashboard item.
* `propertyKey` - _required_ - The key of the dashboard item property.

### Returns the key and value of a dashboard item property.

#### Input Parameters
* `dashboardId` - _required_ - The ID of the dashboard.
* `itemId` - _required_ - The ID of the dashboard item.
* `propertyKey` - _required_ - The key of the dashboard item property.

### Sets the value of a dashboard item property. Use this resource in apps to store custom data against a dashboard item.

#### Input Parameters
* `dashboardId` - _required_ - The ID of the dashboard.
* `itemId` - _required_ - The ID of the dashboard item.
* `propertyKey` - _required_ - The key of the dashboard item property. The maximum length of the key is 255 bytes.

### Returns a dashboard.

#### Input Parameters
* `id` - _required_ - The ID of the dashboard.

### Evaluates a Jira expression and returns its value.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma:
    Possible values: meta.complexity.

### Returns all issue fields in Jira, both system and custom fields.

### Creates a custom field.

### Returns all options defined for a select list issue field. A select list issue field is a type of issue field that allows a user to select an value from a list of options.

#### Input Parameters
* `fieldKey` - _required_ - The field key is specified in the following format: $(app-key)__$(field-key). For example, example-add-on__example-issue-field.
* `maxResults` - _optional_ - The maximum number of items to return per page. For example, 20.
* `startAt` - _optional_ - The starting index of the returned objects. For example, 1.

### Creates an option for a select list issue field.

#### Input Parameters
* `fieldKey` - _required_

### Returns options defined for a select list issue field that can be viewed and selected by the currently logged in user.

#### Input Parameters
* `fieldKey` - _required_ - The field key is specified in the following format: $(app-key)__$(field-key). For example, example-add-on__example-issue-field.
* `maxResults` - _optional_ - The maximum number of items to return per page. For example, 20.
* `projectId` - _optional_ - Filters the results to options that are only available in the specified project. For example, 10000.
* `startAt` - _optional_ - The starting index of the returned objects. For example, 1.

### Returns options defined for a select list issue field that can be viewed by the currently logged in user.

#### Input Parameters
* `fieldKey` - _required_ - The field key is specified in the following format: $(app-key)__$(field-key). For example, example-add-on__example-issue-field.
* `maxResults` - _optional_ - The maximum number of items to return per page. For example, 20.
* `projectId` - _optional_ - Filters the results to options that are only available in the specified project. For example, 10000.
* `startAt` - _optional_ - The starting index of the returned objects. For example, 1.

### Deletes an option from a select list issue field.

#### Input Parameters
* `fieldKey` - _required_ - The field key is specified in the following format: $(app-key)__$(field-key). For example, example-add-on__example-issue-field.
* `optionId` - _required_ - The ID of the option to be deleted. For example, 3.

### Returns an option from a select list issue field.

#### Input Parameters
* `fieldKey` - _required_ - The field key is specified in the following format: $(app-key)__$(field-key). For example, example-add-on__example-issue-field.
* `optionId` - _required_ - The ID of the option to be returned. For example, 3.

### Updates an option for a select list issue field. If the option does not exist, a new option is created.

#### Input Parameters
* `fieldKey` - _required_ - The field key is specified in the following format: $(app-key)__$(field-key). For example, example-add-on__example-issue-field.
* `optionId` - _required_ - The ID of the option to be updated. For example, 3.

### Deselects a select list issue field option in all issues that it has been selected in. A different option can be selected to replace the deselected option. The update can also be limited to a smaller set of issues by using a JQL query.

#### Input Parameters
* `fieldKey` - _required_ - The field key is specified in the following format: $(app-key)__$(field-key). For example, example-add-on__example-issue-field.
* `jql` - _optional_ - A JQL query that specifies the issues to be updated. For example, project=10000.
* `optionId` - _required_ - The ID of the option to be deselected. For example, 3.
* `replaceWith` - _optional_ - The ID of the option that will replace the currently selected option. For example, 2.

### Returns all filters. Deprecated, use Search for filters that supports search and pagination. Permissions required: None, however only the following filters are returned:

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about filter in the response. This parameter accepts multiple values separated by a comma:
    Possible values: sharedUsers, subscriptions.

### Creates a new filter. The new filter is not shared and not selected as a favorite. Permissions required: Permission to log in to Jira.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about filter in the response. This parameter accepts multiple values separated by a comma:
    Possible values: sharedUsers, subscriptions.

### Returns the default sharing settings for new filters and dashboards for a user. Permissions required: Permission to log in to Jira (i.e., member of the users group).

### Sets the default sharing for new filters and dashboards for a user. Permissions required: Permission to log in to Jira (i.e., member of the users group).

### Returns the favorite filters of the calling user. Permissions required: Permission to log in to Jira (i.e., member of the users group).

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about filter in the response. This parameter accepts multiple values separated by a comma:
    Possible values: sharedUsers, subscriptions.

### Returns the filters owned by the calling user. If includeFavourites is true, the user's favorite filters are also returned. Permissions required: Permission to log in to Jira (i.e., member of the users group).

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about filter in the response. This parameter accepts multiple values separated by a comma:
    Possible values: sharedUsers, subscriptions.
* `includeFavourites` - _optional_ - Include the user's favorite filters in the response.

### Search for filters. This method is similar to Get filters except that you can refine the results to include filters that have specific attributes. For example, filters with a particular name. Permissions required: None, however only the following filters are returned (if no search parameters are set):

#### Input Parameters
* `accountId` - _optional_ - Returns filters with an owner that exactly matches accountId of the owner. This parameter cannot be used with the owner parameter.
* `expand` - _optional_ - Use expand to include additional information about filter in the response. This parameter accepts multiple values separated by a comma:
    Possible values: sharedUsers, subscriptions.
* `filterName` - _optional_ - Returns filters with a name that partially matches filterName.
* `groupname` - _optional_ - Returns filters that are shared with a group that has a name that exactly matches groupname.
* `maxResults` - _optional_ - The maximum number of items to return per page. Max is 50.
* `orderBy` - _optional_ - Orders the results by a property of the filter. For example, name.
    Possible values: id, name, description, owner, favourite_count, favouritedCount, is_favourite, favourite.
* `owner` - _optional_ - Returns filters with an owner that exactly matches owner. This parameter cannot be used with the accountId parameter.
* `projectId` - _optional_ - Returns filters that are shared with a project that has an ID that exactly matches projectId.
* `startAt` - _optional_ - The index of the first item to return in a page of results (page offset). The base index is 0.

### Delete a filter. Permissions required: Permission to log in to Jira, however the following rules govern what a user can delete:

#### Input Parameters
* `id` - _required_ - The ID of the filter to delete.

### Returns a filter. Permissions required: None, however the calling user must have permission view the filter.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about filter in the response. This parameter accepts multiple values separated by a comma:
    Possible values: sharedUsers, subscriptions.
* `id` - _required_ - The ID of the filter to return.

### Updates an existing filter. Use this method to update a filter's name, description, JQL, or sharing. Permissions required: Permission to log in to Jira, however the following rules govern what a user can update:

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about filter in the response. This parameter accepts multiple values separated by a comma:
    Possible values: sharedUsers, subscriptions.
* `id` - _required_ - The ID of the filter to update.

### Reset the user's column configuration for the filter to the default. Permissions required: Permission to log in to Jira (i.e., member of the users group) and permission to view the filter.

#### Input Parameters
* `id` - _required_ - The ID of the filter.

### Returns the columns configured for a filter. The column configuration is used when the filter's results are viewed in List View with the Columns set to Filter. Permissions required: None, however the calling user must have permission to view the filter.

#### Input Parameters
* `id` - _required_ - The ID of the filter.

### Sets the columns for a filter. Only navigable fields can be set as columns. Use Get fields to get the list fields in Jira. A navigable field has navigable set to true. Permissions required: Permission to log in to Jira (i.e., member of the users group) and permission to view the filter.

#### Input Parameters
* `id` - _required_ - The ID of the filter.

### Removes a filter as a favorite for the calling user. Permissions required: Permission to log in to Jira (i.e., member of the users group) and permission to view the filter.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about filter in the response. This parameter accepts multiple values separated by a comma:
    Possible values: sharedUsers, subscriptions.
* `id` - _required_ - The ID of the filter.

### Add a filter as a favorite for the calling user. Permissions required: Permission to log in to Jira (i.e., member of the users group) and permission to view the filter.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about filter in the response. This parameter accepts multiple values separated by a comma:
    Possible values: sharedUsers, subscriptions.
* `id` - _required_ - The ID of the filter.

### Returns the share permissions for a filter. A filter can be shared with groups, projects, all logged-in users, or the public. Sharing with all logged-in users or the public is known as a global share permission. Permissions required: None, however the calling user must have permission to view the filter.

#### Input Parameters
* `id` - _required_ - The ID of the filter.

### Add a share permissions to a filter. If you add a global share permission (i.e., all logged-in users or the public) it will overwrite all share permissions for the filter.Be aware that this method uses different objects for updating share permissions compared to Update filter. Permissions required: Share dashboards and filters global permission and the calling user must own the filter.

#### Input Parameters
* `id` - _required_ - The ID of the filter.

### Deletes a share permission from a filter. Permissions required: Permission to log in to Jira (i.e., member of the users group) and the calling user must own the filter.

#### Input Parameters
* `id` - _required_ - The ID of the filter.
* `permissionId` - _required_ - The ID of the share permission.

### Returns a share permission for a filter. A filter can be shared with groups, projects, all logged-in users, or the public. Sharing with all logged-in users or the public is known as a global share permission. Permissions required: None, however the calling user must have permission to view the filter.

#### Input Parameters
* `id` - _required_ - The ID of the filter.
* `permissionId` - _required_ - The ID of the share permission.

### Deletes a group.

#### Input Parameters
* `groupname` - _optional_ - The name of the group.
* `swapGroup` - _optional_ - The group to transfer restrictions to. Only comments and worklogs are transferred. If restrictions are not transferred, comments and worklogs will be inaccessible after the deletion.

### This resource is deprecated, use group/member.

#### Input Parameters
* `expand` - _optional_ - List of fields to expand.
* `groupname` - _optional_ - The name of the group.

### Creates a group.

### Returns all users in a group. Users are ordered by username.

#### Input Parameters
* `groupname` - _optional_ - The name of the group.
* `includeInactiveUsers` - _optional_ - Include inactive users.
* `maxResults` - _optional_ - The maximum number of users to return per page.
* `startAt` - _optional_ - The index of the first user to return.

### Removes a user from a group. Permissions required: Administer Jira global permission.

#### Input Parameters
* `accountid` - _optional_ - The accountId of the user, which uniquely identifies the user across all Atlassian products. For example, 384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192. Required, unless username is specified.
* `groupname` - _optional_ - The name of the group.
* `username` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The username of the user. For example, admin. Required, unless accountId is specified.

### Adds a user to a group.

#### Input Parameters
* `groupname` - _optional_ - The name of the group.

### Returns a list of groups whose names contain a query string. A list of group names can be provided to exclude groups from the results.

#### Input Parameters
* `accountId` - _optional_ - Parameter not in use.
* `exclude` - _optional_ - A list of groups to exclude from the result.
* `maxResults` - _optional_ - The maximum number of groups to return. The maximum number of groups that can be returned is limited by the system property jira.ajax.autocomplete.limit.
* `query` - _optional_ - The string to find in group names.
* `userName` - _optional_ - Parameter not in use.

### Returns a list of users and groups matching a string. The string is used:

#### Input Parameters
* `avatarSize` - _optional_ - The size of the avatar to return. If an invalid value is provided, the default value is used.
* `caseInsensitive` - _optional_ - Indicates whether the search for groups should be case insensitive.
* `excludeConnectAddons` - _optional_ - Indicates whether Connect app users and groups should be excluded from the search results. If an invalid value is provided, the default value is used.
* `fieldId` - _optional_ - The custom field ID of the field this request is for.
* `issueTypeId` - _optional_ - The ID of an issue type that returned users and groups must have permission to view. To include multiple issue type IDs repeat this parameter, use of a comma separated list is not supported. Special values, such as -1 (all standard issue types) and -2 (all subtask issue types), are supported. This parameter is only used when fieldId is present.
* `maxResults` - _optional_ - The maximum number of items to return in each list. The maximum is 1000.
* `projectId` - _optional_ - The ID of a project that returned users and groups must have permission to view. To include multiple projects repeat this parameter, use of a comma separated list is not supported. This parameter is only used when fieldId is present.
* `query` - _optional_ - The search string.
* `showAvatar` - _optional_ - Indicates whether the user avatar should be returned. If an invalid value is provided, the default value is used.

### Creates an issue or, where the option to create sub-tasks is enabled in Jira, a sub-task. A transition may be applied, to move the issue or sub-task to a workflow step other than the default start step, and issue properties set.

#### Input Parameters
* `updateHistory` - _optional_ - Indicates whether the project in which the issue is created is added to the user's Recently viewed project list, as shown under Projects in Jira.

### Creates issues and, where the option to create sub-tasks is enabled in Jira, sub-tasks. Transitions may be applied, to move the issues or sub-tasks to a workflow step other than the default start step, and issue properties set.

### Returns details of projects, issue types within projects, and, when requested, the create screen fields for each issue type for the user. Use the information to populate the requests in Create issue and Create issues.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about in the response. This parameter accepts multiple values separated by a comma:
    Possible values: projects.issuetypes.fields, fields, update.
* `issuetypeIds` - _optional_ - Comma-separated list of issue type IDs. May be specified multiple times and with issuetypeNames.
* `issuetypeNames` - _optional_ - Comma-separated list of issue type names. May be specified multiple times and with issuetypeIds.
* `projectIds` - _optional_ - Comma-separated list of project IDs. May be specified multiple times and with projectKeys.
* `projectKeys` - _optional_ - Comma-separated list of project keys. May be specified multiple times and with projectIds.

### Returns a list of suggested issues matching the auto-completion query for the user executing this request. This operation checks the user's history and browsing context to return issue suggestions.

#### Input Parameters
* `currentIssueKey` - _optional_ - Key of the issue defining search context. The issue defining a context is excluded from the search results.
* `currentJQL` - _optional_ - JQL that defines the search context. Only issues matching this JQL query are included in the results. Note that username and userkey have been deprecated as search terms for this parameter. See the migration guide for details. Use accountId instead.
* `currentProjectId` - _optional_ - ID of a project defining search context. Only issues belonging to a given project are suggested.
* `query` - _optional_ - Query used to filter issue search results.
* `showSubTaskParent` - _optional_ - Set to false to exclude parent issue from the suggestions list if search is performed in the context of a sub-task.
* `showSubTasks` - _optional_ - Set to false to exclude subtasks from the suggestions list.

### Deletes a property value from multiple issues. The issues to be updated can be specified by filter criteria.

#### Input Parameters
* `propertyKey` - _required_ - The key of the property.

### Sets a property value on multiple issues. The issues to be updated can be specified by a filter.

#### Input Parameters
* `propertyKey` - _required_ - The key of the property. The maximum length is 255 characters.

### Deletes an issue.

#### Input Parameters
* `deleteSubtasks` - _optional_ - Indicates whether the issue's sub-tasks are deleted when the issue is deleted.
* `issueIdOrKey` - _required_ - The ID or key of the issue.

### Returns the details for an issue.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about the issues in the response. This parameter accepts multiple values separated by a comma:
    Possible values: renderedFields, names, schema, transitions, operations, editmeta, changelog, versionedRepresentations, fields.
* `fields` - _optional_ - A comma-separated list of fields to return for the issue. Use it to retrieve a subset of fields. Allowed values:
    Possible values: *all, *navigable, summary,comment, -description, *navigable,-comment.
* `fieldsByKeys` - _optional_ - Indicates whether fields in fields are referenced by keys rather than IDs. This parameter is useful where fields have been added by a connect app and a field's key may differ from its ID.
* `issueIdOrKey` - _required_ - The ID or key of the issue. For example, JRACLOUD-1549.
* `properties` - _optional_ - A comma-separated list of issue properties to return for the issue. Allowed values:
    Possible values: *all, *all,-prop1, prop1, prop1,prop2, prop2.
* `updateHistory` - _optional_ - Indicates whether the project in which the issue is created is added to the user's Recently viewed project list, as shown under Projects in Jira. This also populates the JQL issues search lastViewed field.

### Edits an issue. A transition may be applied and issue properties updated as part of the edit.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.
* `notifyUsers` - _optional_ - Indicates whether a notification email about the issue update is sent to all watchers. To disable the notification, administer Jira or administer project permissions are required. If the user doesn't have the necessary permission the request is ignored.
* `overrideEditableFlag` - _optional_ - Indicates whether screen security should be overridden to enable uneditable fields to be edited. Available to Connect app users with admin permissions.
* `overrideScreenSecurity` - _optional_ - Indicates whether screen security should be overridden to enable hidden fields to be edited. Available to Connect app users with admin permissions.

### Assigns an issue to a user. Use this operation when the calling user does not have the Edit Issues permission but has the Assign issue permission for the project that the issue is in.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue to be assigned.

### Adds one or more attachments to an issue. Attachments are posted as multipart/form-data (RFC 1867).

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue that attachments are added to.

### Returns a paginated list of all updates of an issue, sorted by date, starting from the oldest.

#### Input Parameters
* `issueIdOrKey` - _required_ - ID or key of the issue.
* `maxResults` - _optional_ - Maximum number of items to return per page. See Pagination section for more details.
* `startAt` - _optional_ - Page offset, ie. index of the first item returned in the page of results. Base index: 0.

### to get comments for

#### Input Parameters
* `expand` - _optional_ - optional flags: renderedBody (provides body rendered in HTML)
* `issueIdOrKey` - _required_ - to get comments for
* `maxResults` - _optional_ - how many results on the page should be included. Defaults to 50.
* `orderBy` - _optional_ - ordering of the results.
* `startAt` - _optional_ - the page offset, if not specified then defaults to 0

### a string containing the issue id or key the comment will be added to

#### Input Parameters
* `expand` - _optional_ - optional flags: renderedBody (provides body rendered in HTML)
* `issueIdOrKey` - _required_ - a string containing the issue id or key the comment will be added to

### a string containing the issue id or key the comment belongs to

#### Input Parameters
* `id` - _required_ - id of the comment to be deleted
* `issueIdOrKey` - _required_ - a string containing the issue id or key the comment belongs to

### of the issue the comment belongs to

#### Input Parameters
* `expand` - _optional_ - optional flags: renderedBody (provides body rendered in HTML)
* `id` - _required_ - the ID of the comment to request
* `issueIdOrKey` - _required_ - of the issue the comment belongs to

### a string containing the issue id or key the comment belongs to

#### Input Parameters
* `expand` - _optional_ - optional flags: renderedBody (provides body rendered in HTML)
* `id` - _required_ - id of the comment to be updated
* `issueIdOrKey` - _required_ - a string containing the issue id or key the comment belongs to

### Returns the edit screen fields for an issue that are visible to and editable by the user. Use the information to populate the requests in Edit issue.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.
* `overrideEditableFlag` - _optional_ - Indicates whether non-editable fields should be returned. Available to connect app users with admin permissions.
* `overrideScreenSecurity` - _optional_ - Indicates whether hidden fields should be returned. Available to connect app users with admin permissions.

### Creates an email notification for an issue and adds it to the mail queue.

#### Input Parameters
* `issueIdOrKey` - _required_ - ID or key of the issue that the notification is sent for.

### Returns the URIs and keys of an issue's properties.

#### Input Parameters
* `issueIdOrKey` - _required_ - The key or ID of the issue.

### Deletes an issue's property.

#### Input Parameters
* `issueIdOrKey` - _required_ - The key or ID of the issue.
* `propertyKey` - _required_ - The key of the property.

### Returns the key and value of an issue's property.

#### Input Parameters
* `issueIdOrKey` - _required_ - The key or ID of the issue.
* `propertyKey` - _required_ - The key of the property.

### Sets the value of an issue's property. Use this resource to store custom data against an issue.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.
* `propertyKey` - _required_ - The key of the issue property. The maximum length is 255 characters.

### Deletes the remote issue link from the issue using the link's global ID.

#### Input Parameters
* `globalId` - _optional_ - The global ID of a remote issue link.
* `issueIdOrKey` - _required_ - The ID or key of the issue.

### Returns the remote issue links for an issue. When a remote issue link global ID is provided the record with that global ID is returned, otherwise all remote issue links are returned.

#### Input Parameters
* `globalId` - _optional_ - The global ID of the remote issue link.
* `issueIdOrKey` - _required_ - The ID or key of the issue.

### Creates or updates a remote issue link for an issue.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.

### Deletes a remote issue link from an issue.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.
* `linkId` - _required_ - The ID of a remote issue link.

### Returns a remote issue link for an issue.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.
* `linkId` - _required_ - The ID of the remote issue link.

### Updates a remote issue link for an issue.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.
* `linkId` - _required_ - The ID of the remote issue link.

### Returns either all transitions or a transition that can be performed by the user on an issue, based on the issue's status.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about in the response. This parameter accepts multiple values separated by a comma:
    Possible values: transitions.fields, fields, update.
* `issueIdOrKey` - _required_ - The ID or key of the issue.
* `skipRemoteOnlyCondition` - _optional_ - Indicates whether transitions with the condition Hide From User Condition are included in the response.
* `transitionId` - _optional_ - The ID of the transition.

### Performs an issue transition and, if the transition has a screen, updates the fields from the transition screen. Optionally, issue properties can be set.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.

### Deletes a user's vote from an issue. This is the equivalent of the user clicking Unvote on an issue in Jira.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.

### Returns details about the votes on an issue.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.

### Adds the user's vote to an issue. This is the equivalent of the user clicking Vote on an issue in Jira.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.

### Deletes a user as a watcher of an issue.

#### Input Parameters
* `accountId` - _optional_ - The account ID of the user. Required if username is omitted, otherwise must be omitted.
* `issueIdOrKey` - _required_ - The ID or key of the issue.
* `username` - _optional_ - The name of the user. Required if accountId is omitted, otherwise must be omitted.

### Returns the watchers for an issue.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.

### Adds a user as a watcher of an issue. If no user is specified the calling user is added.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.

### Returns all worklogs for an issue.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about worklogs in the response. This parameter accepts multiple values separated by a comma:
    Possible values: properties.
* `issueIdOrKey` - _required_ - The ID or key of the issue.
* `maxResults` - _optional_ - The maximum number of items to return per page. Maximum is 1048576.
* `startAt` - _optional_ - The index of the first item to return in a page of results (page offset).

### Adds a worklog to an issue.

#### Input Parameters
* `adjustEstimate` - _optional_ - Defines how to update the issue's time estimate, the options are:
    Possible values: new, newEstimate, leave, manual, reduceBy, auto, timeSpent.
* `expand` - _optional_ - Use expand to include additional information about work logs in the response. This parameter accepts multiple values separated by a comma:
    Possible values: properties.
* `issueIdOrKey` - _required_ - The ID or key the issue.
* `newEstimate` - _optional_ - The value to set as the issue's remaining time estimate, as days (#d), hours (#h), or minutes (#m or #). For example, 2d. Required when adjustEstimate is new.
* `notifyUsers` - _optional_ - Indicates whether users watching the issue are notified by email.
* `overrideEditableFlag` - _optional_ - Indicates whether the worklog entry should be added to the issue even if the issue is not editable, because jira.issue.editable set to false or missing. For example, the issue is closed. Only connect app users with admin scope permission can use this flag.
* `reduceBy` - _optional_ - The amount to reduce the issue's remaining estimate by, as days (#d), hours (#h), or minutes (#m). For example, 2d. Required when adjustEstimate is manual.

### Deletes a worklog from an issue.

#### Input Parameters
* `adjustEstimate` - _optional_ - Defines how to update the issue's time estimate, the options are:
    Possible values: new, newEstimate, leave, manual, increaseBy, auto, timeSpent.
* `id` - _required_ - The ID of the worklog.
* `increaseBy` - _optional_ - The amount to increase the issue's remaining estimate by, as days (#d), hours (#h), or minutes (#m or #). For example, 2d. Required when adjustEstimate is manual.
* `issueIdOrKey` - _required_ - The ID or key of the issue.
* `newEstimate` - _optional_ - The value to set as the issue's remaining time estimate, as days (#d), hours (#h), or minutes (#m or #). For example, 2d. Required when adjustEstimate is new.
* `notifyUsers` - _optional_ - Indicates whether users watching the issue are notified by email.
* `overrideEditableFlag` - _optional_ - Indicates whether the work log entry should be added to the issue even if the issue is not editable, because jira.issue.editable set to false or missing. For example, the issue is closed. Only connect app users with admin permissions can use this flag.

### Returns a worklog.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about work logs in the response. This parameter accepts multiple values separated by a comma:
    Possible values: properties.
* `id` - _required_ - The ID of the worklog.
* `issueIdOrKey` - _required_ - The ID or key of the issue.

### Updates a worklog.

#### Input Parameters
* `adjustEstimate` - _optional_ - Defines how to update the issue's time estimate, the options are:
    Possible values: new, newEstimate, leave, auto, timeSpent, timeSpentSeconds.
* `expand` - _optional_ - Use expand to include additional information about worklogs in the response. This parameter accepts multiple values separated by a comma:
    Possible values: properties.
* `id` - _required_ - The ID of the worklog.
* `issueIdOrKey` - _required_ - The ID or key the issue.
* `newEstimate` - _optional_ - The value to set as the issue's remaining time estimate, as days (#d), hours (#h), or minutes (#m or #). For example, 2d. Required when adjustEstimate is new.
* `notifyUsers` - _optional_ - Indicates whether users watching the issue are notified by email.
* `overrideEditableFlag` - _optional_ - Indicates whether the worklog should be added to the issue even if the issue is not editable, for example, because the issue is closed. Only connect app users with admin permissions can use this flag.

### Returns the keys of all properties for a worklog.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.
* `worklogId` - _required_ - The ID of the worklog.

### Deletes a worklog property.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.
* `propertyKey` - _required_ - The key of the property.
* `worklogId` - _required_ - The ID of the worklog.

### Returns the value of a worklog property.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.
* `propertyKey` - _required_ - The key of the property.
* `worklogId` - _required_ - The ID of the worklog.

### Sets the value of a worklog property. Use this operation to store custom data against the worklog.

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.
* `propertyKey` - _required_ - The key of the issue property. The maximum length is 255 characters.
* `worklogId` - _required_ - The ID of the worklog.

### Creates a link between two issues. Use this operation to indicate a relationship between two issues and optionally add a comment to the from (outward) issue. To use this resource the site must have Issue Linking enabled.

### Deletes an issue link.

#### Input Parameters
* `linkId` - _required_ - The ID of the issue link.

### Returns an issue link.

#### Input Parameters
* `linkId` - _required_ - The ID of the issue link.

### Returns a list of all issue link types.

### Creates an issue link type. Use this operation to create descriptions of the reasons why issues are linked. The issue link type consists of a name and descriptions for a link's inward and outward relationships.

### Deletes an issue link type.

#### Input Parameters
* `issueLinkTypeId` - _required_ - The ID of the issue link type.

### Returns an issue link type.

#### Input Parameters
* `issueLinkTypeId` - _required_ - The ID of the issue link type.

### Updates an issue link type.

#### Input Parameters
* `issueLinkTypeId` - _required_ - The ID of the issue link type.

### Returns all issue security schemes.

### Returns an issue security scheme along with its security levels.

#### Input Parameters
* `id` - _required_ - The ID of the issue security scheme. Use the Get issue security schemes operation to get a list of issue security scheme IDs.

### Returns all issue types. Permissions required: Permission to access Jira, however, only issue types that are visible to the user are returned.

### Creates an issue type and adds it to the default issue type scheme. Permissions required: Administer Jira global permission.

### Deletes the issue type. If the issue type is in use, all uses are updated with the alternative issue type (alternativeIssueTypeId). A list of alternative issue types can be obtained from the Get alternative issue types resource. Permissions required: Administer Jira global permission.

#### Input Parameters
* `alternativeIssueTypeId` - _optional_ - The ID of the replacement issue type.
* `id` - _required_ - The ID of the issue type.

### Returns an issue type. Permissions required:

#### Input Parameters
* `id` - _required_ - The ID of the issue type.

### Updates the issue type. Permissions required: Administer Jira global permission.

#### Input Parameters
* `id` - _required_ - The ID of the issue type.

### Returns a list of issue types that can be used to replace the issue type. The alternative issue types are those assigned to the same workflow scheme, field configuration scheme, and screen scheme. Permissions required: Permission to access Jira.

#### Input Parameters
* `id` - _required_ - The ID of the issue type.

### Loads an avatar for the issue type.

#### Input Parameters
* `id` - _required_ - The ID of the issue type.
* `size` - _optional_ - The length of each side of the crop region.
* `x` - _optional_ - The X coordinate of the top-left corner of the crop region.
* `y` - _optional_ - The Y coordinate of the top-left corner of the crop region.

### Returns all the issue type property keys of the issue type. Permissions required:

#### Input Parameters
* `issueTypeId` - _required_ - The ID of the issue type.

### Deletes the issue type property. Permissions required: Administer Jira global permission.

#### Input Parameters
* `issueTypeId` - _required_ - The ID of the issue type.
* `propertyKey` - _required_ - The key of the property. Use Get issue type property keys to get a list of all issue type property keys.

### Returns the key and value of the issue type property. Permissions required:

#### Input Parameters
* `issueTypeId` - _required_ - The ID of the issue type.
* `propertyKey` - _required_ - The key of the property. Use Get issue type property keys to get a list of all issue type property keys.

### Creates or updates the value of the issue type property. Use this resource to store and update data against an issue type. The value of the request body must be a valid, non-empty JSON blob. The maximum length of the property value is 32768 bytes. Permissions required: Administer Jira global permission.

#### Input Parameters
* `issueTypeId` - _required_ - The ID of the issue type.
* `propertyKey` - _required_ - The key of the issue type property. The maximum length of the key is 255 bytes.

### Returns reference data for JQL searches. This is a downloadable version of the documentation provided in Advanced searching - fields reference and Advanced searching - functions reference, along with a list of JQL-reserved words. Use this information to assist with the programmatic creation of JQL queries or the validation of queries built in a custom query builder.

### Returns the JQL search auto complete suggestions for a field.

#### Input Parameters
* `fieldName` - _optional_ - The name of the field.
* `fieldValue` - _optional_ - The partial field item name entered by the user.
* `predicateName` - _optional_ - The name of the CHANGED operator predicate for which the suggestions are generated. The valid predicate operators are by, from, and to.
* `predicateValue` - _optional_ - The partial predicate item name entered by the user.

### The query strings having personal data that need to be migrated. There should be at most 100 queries.

### Returns a list of permissions indicating which permissions the user has. Details of the user's permissions can be obtained in a global, project, or issue context.

#### Input Parameters
* `issueId` - _optional_ - The ID of the issue.
* `issueKey` - _optional_ - The key of the issue. Ignored if issueId is provided.
* `permissions` - _optional_ - A comma separated list of permission keys. Omitting this parameter is deprecated. To get the list of available permissions, use Get all permissions. Note that deprecated keys cannot be used. Deprecated keys are not returned by Get all permissions but are returned by this operation if permissions is omitted.
* `projectId` - _optional_ - The ID of project.
* `projectKey` - _optional_ - The key of project. Ignored if projectId is provided.

### Deletes a preference of the user, which restores the default value of system defined settings.

#### Input Parameters
* `key` - _optional_ - The key of the preference.

### Returns the value of a preference of the user.

#### Input Parameters
* `key` - _optional_ - The key of the preference.

### Creates a preference for the user or updates its value. An arbitrary preference can be created with the value containing up to 255 characters. In addition, the following keys define system preferences that can be set or created:

#### Input Parameters
* `key` - _optional_ - The key of the preference. Maximum length is 255 characters.

### Deletes the locale of the current user, which restores the default setting.

### Returns the locale for the current user.

### Sets the locale of the current user. The requested locale must be one supported by the instance of Jira.

### Returns details for the authenticated user.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about user in the response. This parameter accepts multiple values separated by a comma:
    Possible values: groups, applicationRoles.

### Returns a paginated list of notification schemes in order by display name.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma:
    Possible values: all, field, group, notificationSchemeEvents, projectRole, user.
* `maxResults` - _optional_ - The maximum number of items to return per page. Max is 50.
* `startAt` - _optional_ - The index of the first item to return in a page of results (page offset). The base index is 0.

### Returns a notification scheme, including the list of events and the recipients who will receive notifications for those events.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma:
    Possible values: all, field, group, notificationSchemeEvents, projectRole, user.
* `id` - _required_ - The ID of the notification scheme. Use Get notification schemes paginated to get a list of notification scheme IDs.

### Returns all permissions, including:

### Returns all the projects where the user is granted a list of project permissions.

### Returns all permission schemes.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma. Note that permissions are included when you specify any value:
    Possible values: all, field, group, permissions, projectRole, user.

### Creates a new permission scheme. You can create a permission scheme with or without defining a set of permission grants. Permissions required: Administer Jira global permission.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma. Note that permissions are always included when you specify any value:
    Possible values: all, field, group, permissions, projectRole, user.

### Deletes a permission scheme. Permissions required: Administer Jira global permission.

#### Input Parameters
* `schemeId` - _required_ - The ID of the permission scheme being deleted (e.g., 10000).

### Returns a permission scheme. Permissions required: Permission to log in to Jira.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma. Note that permissions are included when you specify any value:
    Possible values: all, field, group, permissions, projectRole, user.
* `schemeId` - _required_ - The ID of the permission scheme to return (e.g., 10000).

### Updates a permission scheme. Below are some important things to note when using this resource:

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma. Note that permissions are always included when you specify any value:
    Possible values: all, field, group, permissions, projectRole, user.
* `schemeId` - _required_ - The ID of the permission scheme to update (e.g., 10000).

### Returns all permission grants for a permission scheme. Permissions required: Permission to log in to Jira.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma. Note that permissions are always included when you specify any value:
    Possible values: permissions, user, group, projectRole, field, all.
* `schemeId` - _required_ - The ID of the permission scheme (e.g., 10010).

### Creates a new permission grant in the given permission scheme. Permissions required: Administer Jira global permission.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma. Note that permissions are always included when you specify any value:
    Possible values: permissions, user, group, projectRole, field, all.
* `schemeId` - _required_ - The ID of the permission scheme in which to create a new permission grant.

### Deletes a permission grant from a permission scheme. See About permission schemes and grants for more details. Permissions required: Administer Jira global permission.

#### Input Parameters
* `permissionId` - _required_ - The ID of the permission grant to delete (e.g., 10847).
* `schemeId` - _required_ - The ID of the permission scheme to delete the permission grant from (e.g., 10000).

### Returns a permission grant. Permissions required: Permission to log in to Jira.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma. Note that permissions are always included when you specify any value:
    Possible values: all, field, group, permissions, projectRole, user.
* `permissionId` - _required_ - The ID of the permission grant (e.g., 10000).
* `schemeId` - _required_ - The ID of the permission scheme (e.g., 10010).

### Returns the list of all issue priorities.

### Returns an issue priority.

#### Input Parameters
* `id` - _required_ - The ID of the issue priority.

### Returns all projects visible to the currently logged in user. Deprecated, use Get projects paginated that supports search and pagination. For projects to be visible, the authenticated user must be granted either Browse projects or Administer projects permissions. If no user is logged in, it returns all projects that are visible for anonymous users.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma:
    Possible values: description, issueTypes, lead, projectKeys.
* `recent` - _optional_ - Returns the most recently accessed projects for the current user. You may specify the number of results to return up to a maximum of 20. If no user is logged in, then the recently accessed projects will be returned based on the current HTTP session.

### Creates a new project.

### Returns projects visible to the currently logged in user. For projects to be visible, the authenticated user must be granted either Browse projects or Administer projects permissions. If no user is logged in, then all projects visible to anonymous users are returned.

#### Input Parameters
* `action` - _optional_ - Filter results by projects for which the calling user has permission to perform the given action. The view action corresponds with the Browse projects project permission, and the edit action corresponds with Administer project permissions.
* `categoryId` - _optional_ - The ID of the project's category. A complete list of category IDs can be found using the Get all project categories resource.
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma:
    Possible values: description, projectKeys, lead, issueTypes, url.
* `maxResults` - _optional_ - The maximum number of items to return per page. Max 50.
* `orderBy` - _optional_ - Order the results by a particular field. If the orderBy field is not set, then projects are listed in ascending order by project key:
    Possible values: category, key, name, owner.
* `query` - _optional_ - Filter the results using a literal string. Projects with a matching key or name are returned (case insensitive).
* `startAt` - _optional_ - The starting index of the first item returned in the page of results (page offset). The base index is 0.
* `typeKey` - _optional_ - Orders results by the project type. This parameter accepts multiple values separated by a comma. Valid values are business, service_desk, and software.

### Returns all project types, whether or not the instance has a valid license for each type.

### Returns a project type.

#### Input Parameters
* `projectTypeKey` - _required_ - The key of the project type.

### Returns a project type if it is accessible to the logged in user.

#### Input Parameters
* `projectTypeKey` - _required_ - The key of the project type.

### Deletes an existing project.

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).

### Returns the project details for the specified project.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma. Note that the project description, issue types, and project lead are included in all responses by default:
    Possible values: description, issueTypes, lead, projectKeys.
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).

### Updates the project details of an existing project.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma. Note that the project description, issue types, and project lead are included in all responses by default:
    Possible values: description, issueTypes, lead, projectKeys.
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).

### Sets the avatar displayed for a project.

#### Input Parameters
* `projectIdOrKey` - _required_ - The ID or (case-sensitive) key of the project.

### Deletes a custom avatar from a project. Note that system avatars cannot be deleted.

#### Input Parameters
* `id` - _required_ - The ID of the avatar.
* `projectIdOrKey` - _required_ - The project ID or (case-sensitive) key.

### Loads an avatar for a project.

#### Input Parameters
* `projectIdOrKey` - _required_ - The ID or (case-sensitive) key of the project.
* `size` - _optional_ - The length of each side of the crop region.
* `x` - _optional_ - The X coordinate of the top-left corner of the crop region.
* `y` - _optional_ - The Y coordinate of the top-left corner of the crop region.

### Returns all project avatars, grouped by system and custom avatars.

#### Input Parameters
* `projectIdOrKey` - _required_ - The ID or (case-sensitive) key of the project.

### Returns a paginated representation of all components existing in a single project. See the Get project components resource if you want to get a full list of versions without pagination.

#### Input Parameters
* `maxResults` - _optional_ - The maximum number of components to return per page. Max 50.
* `orderBy` - _optional_ - Order the results by a particular field:
    Possible values: description, issueCount, lead, name.
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).
* `query` - _optional_ - Filter the results using a literal string. Components with a matching name or description are returned (case insensitive).
* `startAt` - _optional_ - The starting index of the returned list of components. The base index is 0.

### Returns all components existing in a single project. See the Get project components paginated resource if you want to get a full list of components with pagination.

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).

### Returns all project property keys for the project.

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).

### Removes the property from the project.

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).
* `propertyKey` - _required_ - The project property key. Use Get project property keys to get a list of all project property keys.

### Returns the value of the project property.

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).
* `propertyKey` - _required_ - The project property key. Use Get project property keys to get a list of all project property keys.

### Sets the value of the project property. You can use project properties to store custom data against the project.

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).
* `propertyKey` - _required_ - The key of the project property. The maximum length is 255 bytes.

### Returns a list of project roles for the project.

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).

### Deletes actors from a project role for the project.

#### Input Parameters
* `group` - _optional_ - The name of the group to remove from the project role.
* `id` - _required_ - The ID of the project role. Use Get all project roles to get a list of project role IDs.
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).
* `user` - _optional_ - The user account ID of the user to remove from the project role.

### Returns the project role's details and actors associated with the project. The list of actors is sorted by display name.

#### Input Parameters
* `id` - _required_ - The ID of the project role. Use Get all project roles to get a list of project role IDs.
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).

### Adds additional actors to a project role for the project.

#### Input Parameters
* `id` - _required_ - The ID of the project role. Use Get all project roles to get a list of project role IDs.
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).

### Associates actors with the project role for the project, replacing all existing actors.

#### Input Parameters
* `id` - _required_ - The ID of the project role. Use Get all project roles to get a list of project role IDs.
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).

### Returns all project roles and the details for each role. Note that the list of project roles is common to all projects.

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).

### Returns the valid statuses for a project. The statuses are grouped by issue type, as each project has a set of valid issue types and each issue type has a set of valid statuses.

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).

### Updates the project type.

#### Input Parameters
* `newProjectTypeKey` - _required_ - The key of the new project type.
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).

### Returns a paginated representation of all versions existing in a single project. See the Get project versions resource if you want to get a full list of versions without pagination.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma:
    Possible values: issuesstatus, operations, remotelinks.
* `maxResults` - _optional_ - The maximum number of versions to return per page. Max 50.
* `orderBy` - _optional_ - Order the results by a particular field:
    Possible values: description, name, releaseDate, sequence, startDate.
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).
* `query` - _optional_ - Filter the results using a literal string. Versions with matching name or description are returned (case insensitive).
* `startAt` - _optional_ - The starting index of the returned list of versions (page offset). The base index is 0.
* `status` - _optional_ - A comma separated string used to filter the results by version status.

### Returns all versions existing in a single project. The response is not paginated. Use Get project versions paginated if you want to get the versions in a project with pagination.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma:
    Possible values: operations.
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).

### Returns the issue security scheme associated with the project.

#### Input Parameters
* `projectKeyOrId` - _required_ - The project ID or project key (case sensitive).

### Gets a notification scheme associated with the project. See the Get notification scheme resource for more information about notification schemes.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma:
    Possible values: all, field, group, notificationSchemeEvents, projectRole, user.
* `projectKeyOrId` - _required_ - The project ID or project key (case sensitive).

### Gets the permission scheme associated with the project.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma. Note that permissions are included when you specify any value:
    Possible values: all, field, group, permissions, projectRole, user.
* `projectKeyOrId` - _required_ - The project ID or project key (case sensitive).

### Associates a permission scheme with a particular project. See Managing project permissions for more information about permission schemes.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts multiple values separated by a comma. Note that permissions are included when you specify any value:
    Possible values: all, field, group, permissions, projectRole, user.
* `projectKeyOrId` - _required_ - The project ID or project key (case sensitive).

### Returns all issue security levels for the project that the currently authenticated user has access to. If the user does not have permission to see an issue security level, then that level is not returned. If the user lacks the Set Issue Security permission, then an empty list is returned.

#### Input Parameters
* `projectKeyOrId` - _required_ - The project ID or project key (case sensitive).

### Returns all project categories.

### Creates a project category.

### Deletes a project category.

#### Input Parameters
* `id` - _required_ - ID of the project category to delete.

### Returns a project category.

#### Input Parameters
* `id` - _required_ - The ID of the project category.

### Updates a project category.

#### Input Parameters
* `id` - _required_

### Validates a project key by confirming the key is a valid string and not in use.

#### Input Parameters
* `key` - _optional_ - The project key.

### Validates a project key and, if the key is invalid or in use, generates a valid random string for the project key.

#### Input Parameters
* `key` - _optional_ - The project key.

### Checks that a project name isn't in use. If the name isn't in use, the passed string is returned. If the name is in use, this operation attempts to generate a valid project name based on the one supplied, usually by adding a sequence number. If a valid project name cannot be generated, a 404 response is returned.

#### Input Parameters
* `name` - _optional_ - The project name.

### Returns a list of all issue resolution values.

### Returns an issue resolution value.

#### Input Parameters
* `id` - _required_ - The ID of the issue resolution value.

### Gets a list of all project roles, complete with project role details and default actors.

### Creates a new project role with no default actors. You can use the Add default actors to project role the project method to add default actors to the project role after creating it.

### Deletes a project role. You must specify a replacement project role if you wish to delete a project role that is in use.

#### Input Parameters
* `id` - _required_ - The ID of the project role to delete. Use Get all project roles to get a list of project role IDs.
* `swap` - _optional_ - The ID of the project role that will replace the one being deleted.

### Gets the project role details and the default actors associated with the role. The list of default actors is sorted by display name.

#### Input Parameters
* `id` - _required_ - The ID of the project role. Use Get all project roles to get a list of project role IDs.

### Update either the project role's name or its description.

#### Input Parameters
* `id` - _required_ - The ID of the project role. Use Get all project roles to get a list of project role IDs.

### Update the project role's name and description. You must include both a name and a description in the request.

#### Input Parameters
* `id` - _required_ - The ID of the project role. Use Get all project roles to get a list of project role IDs.

### Removes default actors from the project role. You may remove either a group or user, but you cannot remove a group and a user in the same request.

#### Input Parameters
* `group` - _optional_ - The group name of the group to be removed as a default actor.
* `id` - _required_ - The ID of the project role. Use Get all project roles to get a list of project role IDs.
* `user` - _optional_ - The user account ID of the user to remove as a default actor.

### Returns the default actors for the project role.

#### Input Parameters
* `id` - _required_ - The ID of the project role. Use Get all project roles to get a list of project role IDs.

### Adds default actors to the given role. You may add either groups or users, but you cannot add groups and users in the same request.

#### Input Parameters
* `id` - _required_ - The ID of the project role. Use Get all project roles to get a list of project role IDs.

### Returns all screens.

#### Input Parameters
* `maxResults` - _optional_ - The maximum number of items to return per page. Maximum is 100.
* `startAt` - _optional_ - The index of the first item to return in a page of results (page offset).

### Adds a field to the default tab of the default screen.

#### Input Parameters
* `fieldId` - _required_ - The ID of the field.

### Returns the fields that can be added to a tab on a screen.

#### Input Parameters
* `screenId` - _required_ - The ID of the screen.

### Returns the list of tabs for a screen.

#### Input Parameters
* `projectKey` - _optional_ - The key of the project.
* `screenId` - _required_ - The ID of the screen.

### Creates a tab for a screen.

#### Input Parameters
* `screenId` - _required_ - The ID of the screen.

### Deletes a screen tab.

#### Input Parameters
* `screenId` - _required_ - The ID of the screen.
* `tabId` - _required_ - The ID of the screen tab.

### Updates the name of a screen tab.

#### Input Parameters
* `screenId` - _required_ - The ID of the screen.
* `tabId` - _required_ - The ID of the screen tab.

### Returns all fields for a screen tab.

#### Input Parameters
* `projectKey` - _optional_ - The key of the project.
* `screenId` - _required_ - The ID of the screen.
* `tabId` - _required_ - The ID of the screen tab.

### Adds a field to a screen tab.

#### Input Parameters
* `screenId` - _required_ - The ID of the screen.
* `tabId` - _required_ - The ID of the screen tab.

### Removes a field from a screen tab.

#### Input Parameters
* `id` - _required_ - The ID of the field.
* `screenId` - _required_ - The ID of the screen.
* `tabId` - _required_ - The ID of the screen tab.

### Moves a screen tab field.

#### Input Parameters
* `id` - _required_ - The ID of the field.
* `screenId` - _required_ - The ID of the screen.
* `tabId` - _required_ - The ID of the screen tab.

### Moves a screen tab.

#### Input Parameters
* `pos` - _required_ - The position of tab. The base index is 0.
* `screenId` - _required_ - The ID of the screen.
* `tabId` - _required_ - The ID of the screen tab.

### Searches for issues using JQL. Permissions required: Permission to access Jira.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about issues in the response. This parameter accepts multiple values separated by a comma:
    Possible values: renderedFields, names, schema, transitions, operations, editmeta, changelog, versionedRepresentations, fields.
* `fields` - _optional_ - A comma-separated list of fields to return for each issue, use it to retrieve a subset of fields. Allowed values:
    Possible values: *all, *navigable, summary,comment, -description, *all,-comment.
* `fieldsByKeys` - _optional_ - Reference fields by their key (rather than ID).
* `jql` - _optional_ - The JQL that defines the search. If no JQL expression is provided, all issues are returned. Note that username and userkey have been deprecated as search terms for this parameter. See the migration guide for details. Use accountId instead.
* `maxResults` - _optional_ - The maximum number of items to return per page. Maximum is 100.
* `properties` - _optional_ - A comma-separated list of up to 5 issue properties to include in the results.
* `startAt` - _optional_ - The index of the first item to return in the page of results (page offset).
* `validateQuery` - _optional_ - Determines how to validate the JQL query and treat the validation results. Supported values are:
    Possible values: strict, warn, none, true, false.

### Searches for issues using JQL. Permissions required: Permission to access Jira.

### Returns details of an issue security level.

#### Input Parameters
* `id` - _required_ - The ID of the issue security level.

### Returns information about the Jira instance.

### Returns the default issue navigator columns.

### Sets the default issue navigator columns.

### Returns a list of all statuses associated with workflows.

### Returns a status. The status must be associated with a workflow to be returned.

#### Input Parameters
* `idOrName` - _required_ - The ID or name of the status.

### Returns a list of all status categories.

### Returns a status category. Status categories provided a mechanism for categorizing statuses.

#### Input Parameters
* `idOrKey` - _required_ - The ID or key of the status category.

### Returns the status of a long-running asynchronous task.

#### Input Parameters
* `taskId` - _required_ - The ID of the task.

### Cancels a task.

#### Input Parameters
* `taskId` - _required_ - The ID of the task.

### Returns the system and custom avatars for a project or issue type.

#### Input Parameters
* `entityId` - _required_ - The ID of the entity item.
* `type` - _required_ - The type of the entity. Valid values are project and issuetype.

### Loads a custom avatar for a project or issue type.

#### Input Parameters
* `entityId` - _required_ - The ID of the entity item.
* `size` - _optional_ - The length of each side of the crop region.
* `type` - _required_ - The type of the entity. Valid values are project and issuetype.
* `x` - _optional_ - The X coordinate of the top-left corner of the crop region.
* `y` - _optional_ - The Y coordinate of the top-left corner of the crop region.

### Deletes an avatar from a project or issue type.

#### Input Parameters
* `id` - _required_ - The ID of the avatar.
* `owningObjectId` - _required_ - The ID of the entity item.
* `type` - _required_ - The type of the entity. Valid values are project and issuetype.

### Deletes a user. Permissions required: Site administration (i.e., member of the site-admin group).

#### Input Parameters
* `accountId` - _optional_ - The accountId of the user, which uniquely identifies the user across all Atlassian products. For example, 384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192. Required, unless username or key is specified.
* `key` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The key of the user. For example, admin. Required, unless accountId or username is specified.
* `username` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The username of the user. For example, admin. Required, unless accountId or key is specified.

### Returns a user. Permissions required: None.

#### Input Parameters
* `accountId` - _optional_ - The accountId of the user, which uniquely identifies the user across all Atlassian products. For example, 384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192. Required, unless username or key is specified.
* `expand` - _optional_ - Use expand to include additional information about users in the response. This parameter accepts multiple values separated by a comma:
    Possible values: groups, applicationRoles.
* `key` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The key of the user. For example, admin. Required, unless accountId or username is specified.
* `username` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The username of the user. For example, admin. Required, unless accountId or key is specified.

### Creates a user. This resource is retained for legacy compatibility. As soon as a more suitable alternative is available this resource will be deprecated. The option is provided to set or generate a password for the user. When using the option to generate a password, by omitting password from the request, include "notification": "true" to ensure the user is sent an email advising them that their account has been created. This email includes a link for the user to set their password. If the notification isn't sent for a generated password, the user will need to be sent a reset password request from Jira. Permissions required: Administer Jira global permission

### Returns a list of users who fulfill both of these criteria:

#### Input Parameters
* `maxResults` - _optional_ - The maximum number of items to return per page. Maximum is 1000.
* `projectKeys` - _optional_ - A comma-separated list of project keys (case sensitive).
* `query` - _optional_ - A query string that is matched against user attributes, such as key, name, displayName, and emailAddress, to find relevant users. The string can match any part of the attribute's value. For example, query=john matches a user with a displayName of John Smith and a user with an emailAddress of jane.johnson@example.com.
* `startAt` - _optional_ - The index of the first item to return in a page of results (page offset).
* `username` - _optional_ - This parameter has been deprecated due to privacy changes. Use query instead. See the migration guide for details. A query string used to search username, display name, and email address. The string is matched to the starting letters of any word in the searched fields. For example, ar matches to the username archie but not mark.

### Returns a list of users that can be assigned to an issue. Use this method to find the list of users who can be assigned to:

#### Input Parameters
* `actionDescriptorId` - _optional_ - The ID of the transition.
* `issueKey` - _optional_ - The key of the issue. Required, unless project is specified.
* `maxResults` - _optional_ - The maximum number of items to return per page. Maximum is 1000.
* `project` - _optional_ - The project ID or project key (case sensitive). Required, unless issueKey is specified.
* `query` - _optional_ - A query string that is matched against user attributes, such as key, name, displayName, and emailAddress, to find relevant users. The string can match any part of the attribute's value. For example, query=john matches a user with a displayName of John Smith and a user with an emailAddress of jane.johnson@example.com. Required, unless username is specified.
* `startAt` - _optional_ - The index of the first item to return in a page of results (page offset).
* `username` - _optional_ - This parameter has been deprecated due to privacy changes. Use query instead. See the migration guide for details. A query string used to search username, display name, and email address. The string is matched to the starting letters of any word in the searched fields. For example, ar matches to the username archie but not mark. Required, unless accountId is specified.

### Returns details of users specified in a list of usernames or keys. Permissions required: Administer Jira global permission. Users with permission to access Jira can call this method, but empty search results are returned.

#### Input Parameters
* `key` - _optional_ - Comma-separated list of user keys. Required if username isn't provided.
* `maxResults` - _optional_ - The maximum number of items to return per page. Maximum is 200.
* `startAt` - _optional_ - The index of the first item to return in a page of results (page offset).
* `username` - _optional_ - Comma-separated list of usernames. Required if key isn't provided.

### Resets the default issue table columns for the user to the system default. If a username is not passed, the calling user's default columns are reset. Permissions required:

#### Input Parameters
* `accountId` - _optional_ - The accountId of the user, which uniquely identifies the user across all Atlassian products. For example, 384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192. Required, unless username is specified.
* `username` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The username of the user. For example, admin. Required, unless accountId is specified.

### Returns the default issue table columns for the user. If a username is not passed in the request, the calling user's details are returned. Permissions required:

#### Input Parameters
* `accountId` - _optional_ - The accountId of the user, which uniquely identifies the user across all Atlassian products. For example, 384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192. Required, unless username is specified.
* `username` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The username of the user. For example, admin. Required, unless accountId is specified.

### Sets the default issue table columns for the user. If a username is not passed, the calling user's default columns are set. If no column details are sent, then all default columns are removed. The parameters for this resource are expressed as HTML form data. For example, in curl: curl -X PUT -d username=<username> -d columns=summary -d columns=description <url> Permissions required:

#### Input Parameters
* `accountId` - _optional_ - The accountId of the user, which uniquely identifies the user across all Atlassian products. For example, 384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192. Required, unless username is specified.

### Returns the groups to which a user belongs. Permissions required: Browse users and groups global permission.

#### Input Parameters
* `accountId` - _optional_ - The account ID of the user.
* `key` - _optional_ - The key of the user.
* `username` - _optional_ - The username of the user. Deprecated in favour of accountId.

### Returns a list of users who fulfill both of these criteria:

#### Input Parameters
* `issueKey` - _optional_ - The issue key for the issue.
* `maxResults` - _optional_ - The maximum number of items to return per page. Maximum is 1000.
* `permissions` - _optional_ - A comma-separated list of permissions. The valid permissions are:
* `projectKey` - _optional_ - The project key for the project (case sensitive).
* `query` - _optional_ - A query string that is matched against user attributes, such as key, name, displayName, and emailAddress, to find relevant users. The string can match any part of the attribute's value. For example, query=john matches a user with a displayName of John Smith and a user with an emailAddress of jane.johnson@example.com.
* `startAt` - _optional_ - The index of the first item to return in a page of results (page offset).
* `username` - _optional_ - This parameter has been deprecated due to privacy changes. Use query instead. See the migration guide for details. A query string used to search username, display name, and email address. The string is matched to the starting letters of any word in the searched fields. For example, ar matches to the username archie but not mark.

### Returns a list of users whose attributes match the query term. The returned object includes the html field where the matched query term is highlighted with the HTML strong tag. A list of account IDs can be provided to exclude users from the results. Permissions required: Browse users and groups global permission. Users with permission to access Jira can call this method, but will only get search results for an exact name match.

#### Input Parameters
* `exclude` - _optional_ - This parameter has been deprecated due to privacy changes. Use excludeAccountIds instead. See the migration guide for details. A comma-separated list of usernames to exclude from the search results.
* `excludeAccountIds` - _optional_ - A comma-separated list of account IDs to exclude from the search results.
* `maxResults` - _optional_ - The maximum number of items to return. Maximum is 1000. The total number of matched users is returned in total.
* `query` - _optional_ - A search input that is matched against appropriate user attributes to find relevant users.
* `showAvatar` - _optional_ - Include the URI to the user's avatar.

### Returns the keys of all properties for a user. Permissions required:

#### Input Parameters
* `accountId` - _optional_ - The accountId of the user, which uniquely identifies the user across all Atlassian products. For example, 384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192. Required, unless username or key is specified.
* `userKey` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The key of the user. For example, admin. Required, unless accountId or username is specified.
* `username` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The username of the user. For example, admin. Required, unless accountId or key is specified.

### Deletes a property from a user. Permissions required:

#### Input Parameters
* `accountId` - _optional_ - The accountId of the user, which uniquely identifies the user across all Atlassian products. For example, 384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192. Required, unless username or key is specified.
* `propertyKey` - _required_ - The key of the user's property.
* `userKey` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The key of the user. For example, admin.
* `username` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The username of the user. For example, admin. Required, unless accountId or key is specified.

### Returns the value of a user's property. If no property key is provided Get user property keys is called. Permissions required:

#### Input Parameters
* `accountId` - _optional_ - The accountId of the user, which uniquely identifies the user across all Atlassian products. For example, 384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192. Required, unless username or key is specified.
* `propertyKey` - _required_ - The key of the user's property.
* `userKey` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The key of the user. For example, admin.
* `username` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The username of the user. For example, admin. Required, unless accountId or key is specified.

### Sets the value of a user's property. Use this resource to store custom data against a user. Permissions required:

#### Input Parameters
* `accountId` - _optional_ - The accountId of the user, which uniquely identifies the user across all Atlassian products. For example, 384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192. Required, unless username or key is specified.
* `propertyKey` - _required_ - The key of the user's property. The maximum length of the key is 255 bytes.
* `userKey` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The key of the user. For example, admin. Required, unless accountId or username is specified.
* `username` - _optional_ - This parameter has been deprecated due to privacy changes. Use accountId instead. See the migration guide for details.The username of the user. For example, admin. Required, unless accountId or key is specified.

### Returns a list of users that match the search string and property. Permissions required: Browse users and groups global permission. Users with permission to access Jira can call this method, but empty search results are returned.

#### Input Parameters
* `includeActive` - _optional_ - Include active users.
* `includeInactive` - _optional_ - Include inactive users.
* `maxResults` - _optional_ - The maximum number of items to return per page. Maximum is 1000.
* `property` - _optional_ - A query string used to search properties. Property keys are specified by path, so property keys containing dot (.) or equals (=) characters cannot be used. The query string cannot be specified using a JSON object. Example: To search for the value of nested from {"something":{"nested":1,"other":2}} use thepropertykey.something.nested=1.
* `query` - _optional_ - A query string that is matched against user attributes (key, name, displayName, and emailAddress) to find relevant users. The string can match any part of the attribute's value. For example, query=john matches a user with a displayName of John Smith and a user with an emailAddress of jane.johnson@example.com. Required, unless username is specified.
* `startAt` - _optional_ - The index of the first item to return in a page of results (page offset).
* `username` - _optional_ - This parameter has been deprecated due to privacy changes. Use query instead. See the migration guide for details. A query string used to search username, display name, and email address. The string is matched to the starting letters of any word in the searched fields. For example, ar matches to the username archie but not mark. Required, unless accountId is specified.

### Finds users using a structured query and returns user details. Permissions required: Browse users and groups global permission. The available queries statements are:

#### Input Parameters
* `includeInactive` - _optional_ - Include inactive users in the results.
* `maxResults` - _optional_ - The maximum number of items to return per page. Maximum is 1000.
* `query` - _optional_ - The search query.
* `startAt` - _optional_ - The index of the first item to return in a page of results (page offset).

### Finds users using a structured query and returns a list of user keys. Permissions required: Browse users and groups global permission. The available query statements are:

#### Input Parameters
* `includeInactive` - _optional_ - Include inactive users in the results.
* `maxResults` - _optional_ - The maximum number of items to return per page. Maximum is 1000.
* `query` - _optional_ - The search query.
* `startAt` - _optional_ - The index of the first item to return in a page of results (page offset).

### Returns a list of users who fulfill both of these criteria:

#### Input Parameters
* `issueKey` - _optional_ - The issue key for the issue. Required, unless projectKey is specified.
* `maxResults` - _optional_ - The maximum number of items to return per page. Maximum is 1000.
* `projectKey` - _optional_ - The project key for the project (case sensitive). Required, unless issueKey is specified.
* `query` - _optional_ - A query string that is matched against user attributes, such as key, name, displayName, and emailAddress, to find relevant users. The string can match any part of the attribute's value. For example, query=john matches a user with a displayName of John Smith and a user with an emailAddress of jane.johnson@example.com. Required, unless username is specified.
* `startAt` - _optional_ - The index of the first item to return in a page of results (page offset).
* `username` - _optional_ - This parameter has been deprecated due to privacy changes. Use query instead. See the migration guide for details. A query string used to search username, display name, and email address. The string is matched to the starting letters of any word in the searched fields. For example, ar matches to the username archie but not mark. Required, unless accountId is specified.

### Creates a project version. Permissions required: Administer Jira global permission or Administer Projects project permission.

### the global ID of the remote resource that is linked to the versions

#### Input Parameters
* `globalId` - _optional_ - the global ID of the remote resource that is linked to the versions

### Deletes a project version. Deprecated, use Delete and replace version that supports swapping version values in custom fields, in addition to the swapping for fixVersion and affectedVersion provided in this resource. Alternative versions can be provided to update issues that use the deleted version in fixVersion or affectedVersion. If alternatives are not provided, occurrences of fixVersion and affectedVersion that contain the deleted version are cleared. Permissions required: Administer Jira global permission or Administer Projects project permission.

#### Input Parameters
* `id` - _required_ - The ID of the version.
* `moveAffectedIssuesTo` - _optional_ - The ID of the version to update affectedVersion to when the field contains the deleted version. The replacement version must be in the same project as the version being deleted and cannot be the version being deleted.
* `moveFixIssuesTo` - _optional_ - The ID of the version to update fixVersion to when the field contains the deleted version. The replacement version must be in the same project as the version being deleted and cannot be the version being deleted.

### Returns a project version. Permissions required: Browse projects project permission

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about version in the response. This parameter accepts multiple values separated by a comma:
    Possible values: operations, remotelinks, issuesstatus.
* `id` - _required_ - The ID of the version.

### Modifies a project version. Permissions required: Administer Jira global permission or Administer Projects project permission.

#### Input Parameters
* `id` - _required_ - The ID of the version.

### Merges two project versions. The merge is completed by deleting the version specified in id and replacing any occurrences of its ID in fixVersion with the version ID specified in moveIssuesTo. Consider using Delete and replace version instead. This resource supports swapping version values in fixVersion, affectedVersion, and custom fields. Permissions required: Administer Jira global permission or Administer Projects project permission.

#### Input Parameters
* `id` - _required_ - The ID of the version to delete.
* `moveIssuesTo` - _required_ - The ID of the version to merge into.

### Modifies the version's sequence within the project, which affects the display order of the versions in Jira. Permissions required: Administer Jira global permission or Administer Projects project permission.

#### Input Parameters
* `id` - _required_ - The ID of the version to be moved.

### Returns the following counts for a version:

#### Input Parameters
* `id` - _required_ - The ID of the version.

### Deletes a project version. Permissions required: Administer Jira global permission or Administer Projects project permission. Alternative versions can be provided to update issues that use the deleted version in fixVersion, affectedVersion, or any version picker custom fields. If alternatives are not provided, occurrences of fixVersion, affectedVersion, and any version picker custom field, that contain the deleted version, are cleared. Any replacement version must be in the same project as the version being deleted and cannot be the version being deleted.

#### Input Parameters
* `id` - _required_ - The ID of the version.

### Returns counts of the issues and unresolved issues for the project version. Permissions required: Browse projects project permission

#### Input Parameters
* `id` - _required_ - The ID of the version.

### The version for which to delete ALL existing remote version links

#### Input Parameters
* `versionId` - _required_ - The version for which to delete ALL existing remote version links

### a String containing the version ID

#### Input Parameters
* `versionId` - _required_ - a String containing the version ID

### Create a remote version link via POST. The link's global ID will be taken from the JSON payload if provided; otherwise, it will be generated.

#### Input Parameters
* `versionId` - _required_

### The version ID of the remote link

#### Input Parameters
* `globalId` - _required_ - The global ID of the remote link
* `versionId` - _required_ - The version ID of the remote link

### A REST sub-resource representing a remote version link

#### Input Parameters
* `globalId` - _required_ - The id of the remote issue link to be returned. If {@code null} (not provided) all remote links for the issue are returned.
* `versionId` - _required_ - a String containing the version id

### post_version__versionId__remotelink__globalId_

#### Input Parameters
* `globalId` - _required_
* `versionId` - _required_

### Returns all workflows in Jira or a single workflow.

#### Input Parameters
* `workflowName` - _optional_ - The name of the workflow to be returned. Only one workflow can be specified.

### Deletes a property from a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see Transition properties and Workflow properties.

#### Input Parameters
* `key` - _optional_ - The name of the transition property to delete, also known as the name of the property.
* `transitionId` - _required_ - The ID of the transition. To get the ID, view the workflow in text mode in the Jira admin settings. The ID is shown next to the transition.
* `workflowMode` - _optional_ - The workflow status. Set to live for inactive workflows or draft for draft workflows. Active workflows cannot be edited.
* `workflowName` - _optional_ - The name of the workflow that the transition belongs to.

### Returns the properties on a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see Transition properties and Workflow properties.

#### Input Parameters
* `includeReservedKeys` - _optional_ - Some properties with keys that have the jira. prefix are reserved, i.e., not editable. To include these properties in the results, set this parameter to true.
* `key` - _optional_ - The key of the property being returned, also known as the name of the property. If this parameter is not specified, all properties on the transition are returned.
* `transitionId` - _required_ - The ID of the transition. To get the ID, view the workflow in text mode in the Jira administration console. The ID is shown next to the transition.
* `workflowMode` - _optional_ - The workflow status. Set to live for active and inactive workflows, or draft for draft workflows.
* `workflowName` - _optional_ - The name of the workflow that the transition belongs to.

### Adds a property to a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see Transition properties and Workflow properties.

#### Input Parameters
* `key` - _optional_ - The key of the property being added, also known as the name of the property. Set this to the same value as the key defined in the request body.
* `transitionId` - _required_ - The ID of the transition. To get the ID, view the workflow in text mode in the Jira admin settings. The ID is shown next to the transition.
* `workflowMode` - _optional_ - The workflow status. Set to live for inactive workflows or draft for draft workflows. Active workflows cannot be edited.
* `workflowName` - _optional_ - The name of the workflow that the transition belongs to.

### Updates a workflow transition by changing the property value. Trying to update a property that does not exist results in a new property being added to the transition. Transition properties are used to change the behavior of a transition. For more information, see Transition properties and Workflow properties.

#### Input Parameters
* `key` - _optional_ - The key of the property being updated, also known as the name of the property. Set this to the same value as the key defined in the request body.
* `transitionId` - _required_ - The ID of the transition. To get the ID, view the workflow in text mode in the Jira admin settings. The ID is shown next to the transition.
* `workflowMode` - _optional_ - The workflow status. Set to live for inactive workflows or draft for draft workflows. Active workflows cannot be edited.
* `workflowName` - _optional_ - The name of the workflow that the transition belongs to.

### Creates a workflow scheme.

### Deletes a workflow scheme. Note that a workflow scheme cannot be deleted if it is active (that is, being used by at least one project).

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme. Find this ID by editing the desired workflow scheme in Jira. The ID will be shown in the URL as schemeId (for example, schemeId=10301).

### Returns a workflow scheme.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme. Find this ID by editing the desired workflow scheme in Jira. The ID will be shown in the URL as schemeId (for example, schemeId=10301).
* `returnDraftIfExists` - _optional_ - Returns the workflow scheme's draft rather than scheme itself, if set to true. If the workflow scheme does not have a draft, then the workflow scheme is returned.

### Updates a workflow scheme, including the name, default workflow, issue type to project mappings, and more. If the workflow scheme is active (that is, being used by at least one project), then a draft workflow scheme is created or updated instead, provided that updateDraftIfNeeded is set to true.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme. Find this ID by editing the desired workflow scheme in Jira. The ID will be shown in the URL as schemeId (for example, schemeId=10301).

### Create a draft workflow scheme from an active workflow scheme, by copying the active workflow scheme. Note that an active workflow scheme can only have one draft workflow scheme at any given time.

#### Input Parameters
* `id` - _required_ - The ID of the active workflow scheme that the draft is created from.

### Resets the default workflow for a workflow scheme. That is, the default workflow is set to Jira's system workflow (the jira workflow).

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.
* `updateDraftIfNeeded` - _optional_ - Set to true to create or update the draft of a workflow scheme and delete the mapping from the draft, when the workflow scheme cannot be edited. Defaults to false.

### Returns the default workflow for a workflow scheme. The default workflow is the workflow that is assigned any issue types that have not been mapped to any other workflow. The default workflow has All Unassigned Issue Types listed in its issue types for the workflow scheme in Jira.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.
* `returnDraftIfExists` - _optional_ - Set to true to return the default workflow for the workflow scheme's draft rather than scheme itself. If the workflow scheme does not have a draft, then the default workflow for the workflow scheme is returned.

### Sets the default workflow for a workflow scheme.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.

### Deletes a draft workflow scheme.

#### Input Parameters
* `id` - _required_ - The ID of the active workflow scheme that the draft was originally created from.

### Returns the draft workflow scheme for an active workflow scheme. Draft workflow schemes allow changes to be made to the active workflow schemes: When an active workflow scheme is updated, a draft copy is created. The draft is modified, then the changes in the draft are copied back to the active workflow scheme. See Configuring workflow schemes for more information.Note that:

#### Input Parameters
* `id` - _required_ - The ID of the active workflow scheme that the draft was originally created from.

### Updates a draft workflow scheme. If a draft workflow scheme does not exist for the active workflow scheme, then a draft is created. Note that an active workflow scheme can only have one draft workflow scheme at any given time.

#### Input Parameters
* `id` - _required_ - The ID of the active workflow scheme that the draft was originally created from.

### Resets the default workflow for a workflow scheme's draft. That is, the default workflow is set to Jira's system workflow (the jira workflow).

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.

### Returns the default workflow for a workflow scheme's draft. The default workflow is the workflow that is assigned any issue types that have not been mapped to any other workflow. The default workflow has All Unassigned Issue Types listed in its issue types for the workflow scheme in Jira.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.

### Sets the default workflow for a workflow scheme's draft.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.

### Deletes the issue type-workflow mapping for an issue type in a workflow scheme's draft.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.
* `issueType` - _required_ - The ID of the issue type.

### Returns the issue type-workflow mapping for an issue type in a workflow scheme's draft.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.
* `issueType` - _required_ - The ID of the issue type.

### Sets the workflow for an issue type in a workflow scheme's draft.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.
* `issueType` - _required_ - The ID of the issue type.

### Deletes the workflow-issue type mapping for a workflow in a workflow scheme's draft.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.
* `workflowName` - _optional_ - The name of the workflow.

### Returns the workflow-issue type mappings for a workflow scheme's draft.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.
* `workflowName` - _optional_ - The name of a workflow in the scheme. Limits the results to the workflow-issue type mapping for the specified workflow.

### Sets the issue types for a workflow in a workflow scheme's draft. The workflow can also be set as the default workflow for the draft workflow scheme. Unmapped issues types are mapped to the default workflow.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.
* `workflowName` - _optional_ - The name of the workflow.

### Deletes the issue type-workflow mapping for an issue type in a workflow scheme.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.
* `issueType` - _required_ - The ID of the issue type.
* `updateDraftIfNeeded` - _optional_ - Set to true to create or update the draft of a workflow scheme and update the mapping in the draft, when the workflow scheme cannot be edited. Defaults to false.

### Returns the issue type-workflow mapping for an issue type in a workflow scheme.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.
* `issueType` - _required_ - The ID of the issue type.
* `returnDraftIfExists` - _optional_ - Returns the mapping from the workflow scheme's draft rather than the workflow scheme, if set to true. If no draft exists, the mapping from the workflow scheme is returned.

### Sets the workflow for an issue type in a workflow scheme.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.
* `issueType` - _required_ - The ID of the issue type.

### Deletes the workflow-issue type mapping for a workflow in a workflow scheme.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.
* `updateDraftIfNeeded` - _optional_ - Set to true to create or update the draft of a workflow scheme and delete the mapping from the draft, when the workflow scheme cannot be edited. Defaults to false.
* `workflowName` - _optional_ - The name of the workflow.

### Returns the workflow-issue type mappings for a workflow scheme.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.
* `returnDraftIfExists` - _optional_ - Returns the mapping from the workflow scheme's draft rather than the workflow scheme, if set to true. If no draft exists, the mapping from the workflow scheme is returned.
* `workflowName` - _optional_ - The name of a workflow in the scheme. Limits the results to the workflow-issue type mapping for the specified workflow.

### Sets the issue types for a workflow in a workflow scheme. The workflow can also be set as the default workflow for the workflow scheme. Unmapped issues types are mapped to the default workflow.

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.
* `workflowName` - _optional_ - The name of the workflow.

### Returns a list of IDs and delete timestamps for worklogs deleted after a date and time.

#### Input Parameters
* `since` - _optional_ - The date and time, in UNIX timestamp format, after which deleted worklogs are returned.

### Returns worklog details for a list of worklog IDs.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about worklogs in the response. This parameter accepts properties that returns the properties of each worklog.

### Returns a list of IDs and update timestamps for worklogs updated after a date and time.

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information about worklogs in the response. This parameter accepts properties that returns the properties of each worklog.
* `since` - _optional_ - The date and time, in UNIX timestamp format, after which updated worklogs are returned.

## License

**flow**ground :- Telekom iPaaS / atlassian-com-jira-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
