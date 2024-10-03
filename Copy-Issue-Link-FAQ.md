<div>
  <h1 class="no_toc">
    Copy Issue Link
    <div  style="float: left">
      <a href="https://marketplace.atlassian.com/1225783">
        <img src="/images/copy-issue-link.svg">
      </a>
    </div>
  </h1>
  <br>
</div>

[Copy Issue Link](https://marketplace.atlassian.com/1225783) is a Jira plugin that lets you copy a Jira Issue key & title to your clipboard in one click. You can also use a custom template to include more data and personalize the copied text.

## FAQs
{:.no_toc}

1. Table of Contents
{:toc}

### How can I find the configuration page and create a custom template?

1. To access the configuration page, start by clicking on the the gear icon in the top right corner of Jira. You should see a setting option called: "Apps Add and manage Jira Marketplace apps." Click on that.
![jira-marketplace-apps-settings](/images/jira-marketplace-apps-settings.png)
2. On the left hand side of this app configuration page, you should see a button to click called: "Copy Issue Link Configuration." That should get you to the page to configure custom templates.
![jira-marketplace-apps-management](/images/jira-marketplace-apps-management.png)
3. You should now be on the page to configure custom templates.
![copy-issue-link-configuration](/images/copy-issue-link-configuration.png)

### Can I create more than one custom template?

Yes, you can create up to 4.

### Can I create a button that just copies the Jira Issue Key?

Yes. Navigate to the configuration page (as descirbed in FAQ #1), and create a button with a `Custom Template` value of `$ISSUE_KEY_PLACEHOLDER`:

![copy-issue-link-key-copy](/images/copy-issue-link-key-copy.png)

When you click that button on a Jira Issue, an issue key (e.g. `PROJ-18`) will get added to your clipboard.

### Can I disable the default 'Copy Issue Key + Title Link' button?

Yes. Navigate to the configuration page (as descirbed in FAQ #1), and you will find a checkbox option under to disable the default button under `Advanced`:

![copy-issue-link-disable-default-button.png](/images/copy-issue-link-disable-default-button.png)

### Can I remove whitespace or lowercase a field like the Issue title?

Yes. Check out the, `Advanced Placeholders` section of the configuration page. You can use modifiers like `LOWERCASE`, `DASHEDWHITESPACE`, and `INITIALS` to alter the text before you copy it:

![copy-issue-link-advanced](/images/copy-issue-link-advanced.png)

### Can I create a template for `git` branch names?

Yes.

For example, if you wanted `git` branch names like `<user>/<issue-key>-<issue-summary>`, you could create a button with a `Custom Template` value of:

```
git checkout -b $ISSUE_ASSIGNEE_PLACEHOLDER_LOWERCASE_DASHEDWHITESPACE/$ISSUE_KEY_PLACEHOLDER-$ISSUE_SUMMARY_PLACEHOLDER_LOWERCASE_DASHEDWHITESPACE
```

An example rendered value for the preceding template might be: `git checkout -b peter-rabbit/PROJ-18-fix-bug-in-mobile-app`.

### Can I access Copy Issue Link from the right hand side of an Issue?

Yes, you can access the Copy Issue Link plugin in two places: (1) below the Issue Summary or (2) in the pane to the right of the Issue:

![copy-issue-link-two-portals.png](/images/copy-issue-link-two-portals.png)

### Can I temporarily hide Copy Issue Link under the Issue Summary?

Yes, click the `...` menu on the Copy Issue Link portal under the Issue Summary and then click `Remove` to temporarily hide the plugin. When you're ready to re-open the plugin, click the `Copy Issue Link` button again at the top of the Issue:

![copy-issue-link-hide.png](/images/copy-issue-link-hide.png)

### How can I submit a support request?

You can create a support request through our [support portal](https://davidmuller.atlassian.net/servicedesk/customer/portal/1).

### Additional Resources

- <a href="Copy-Issue-Link-privacy">Privacy policy</a>
- <a href="Copy-Issue-Link-EULA">End user license agreement</a>
- <a href="https://davidmuller.atlassian.net/servicedesk/customer/portal/1">Support portal</a>
- <a href="https://marketplace.atlassian.com/1225783">Marketplace listing</a>
