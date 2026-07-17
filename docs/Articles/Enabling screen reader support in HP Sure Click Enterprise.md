<body class="article">
<div id="header">
</div>
<div id="content">
<div class="admonitionblock important">
<table>
<tr>
<td class="icon">
<div class="title">Important</div>
</td>
<td class="content">
<div class="paragraph">
<p>This article was originally published in English. HP uses machine translation to localize content. If you notice any errors, unclear information, or content that seems misleading, <a href="mailto:wps.support@hpwolf.com">open a support ticket</a>.</p>
</div>
</td>
</tr>
</table>
</div>
<hr>
<div class="sect1">
<h2 id="_enabling_screen_reader_support_in_hp_sure_click_enterprise">Enabling screen reader support in HP Sure Click Enterprise</h2>
<div class="sectionbody">
<div class="sect2">
<h3 id="_overview">Overview</h3>
<div class="paragraph">
<p>HP Sure Click Enterprise 4.4 Release 14 (4.4.28.1603) and above includes support for screen readers. Users who use assistive technologies can navigate protected documents and webpages using supported screen readers.</p>
</div>
</div>
<div class="sect2">
<h3 id="_requirements">Requirements</h3>
<div class="sect3">
<h4 id="_supported_operating_systems">Supported operating systems</h4>
<div class="paragraph">
<p>This feature is supported on the following operating systems:</p>
</div>
<div class="ulist">
<ul>
<li>
<p>Windows 11 x64</p>
</li>
</ul>
</div>
<div class="paragraph">
<p>This feature is not supported on the following operating systems:</p>
</div>
<div class="ulist">
<ul>
<li>
<p>Windows 11 Arm64</p>
</li>
<li>
<p>Windows 10 x64</p>
</li>
</ul>
</div>
</div>
<div class="sect3">
<h4 id="_supported_applications">Supported applications</h4>
<div class="paragraph">
<p>This feature is supported for the following protected applications:</p>
</div>
<div class="ulist">
<ul>
<li>
<p>Microsoft Office M365</p>
</li>
<li>
<p>Microsoft Office 2021</p>
</li>
<li>
<p>Microsoft Office 2024</p>
</li>
<li>
<p>Sure Click Enterprise Secure Browser</p>
</li>
<li>
<p>Mozilla Firefox</p>
</li>
</ul>
</div>
<div class="paragraph">
<p>The feature is not supported for the following protected applications:</p>
</div>
<div class="ulist">
<ul>
<li>
<p>Microsoft Office 2016</p>
</li>
<li>
<p>Microsoft Office 2019</p>
</li>
<li>
<p>Windows Photo Viewer</p>
</li>
<li>
<p>Windows Media Player</p>
</li>
<li>
<p>Adobe Acrobat Reader. Protected PDFs can instead be loaded in the Secure Browser and can be read by screen readers there.</p>
</li>
</ul>
</div>
</div>
<div class="sect3">
<h4 id="_supported_screen_readers">Supported screen readers</h4>
<div class="paragraph">
<p>The following screen readers are supported:</p>
</div>
<div class="ulist">
<ul>
<li>
<p>Microsoft Narrator.</p>
</li>
<li>
<p>NVDA (Non-Visual Desktop Access) version 2025.3.1 and later.</p>
</li>
<li>
<p>JAWS (Job Access With Speech) version 2026.2605.43 and later.</p>
</li>
</ul>
</div>
<div class="admonitionblock note">
<table>
<tr>
<td class="icon">
<div class="title">Note</div>
</td>
<td class="content">
JAWS (Job Access With Speech) requires Sure Click Enterprise 4.4 Release 17 (4.4.31.851) or the Secure Browser 146-2 AppPack release (4.4.30.1479) or later.
</td>
</tr>
</table>
</div>
</div>
</div>
<div class="sect2">
<h3 id="_enabling_screen_reader_support_in_sure_click_enterprise">Enabling screen reader support in Sure Click Enterprise</h3>
<div class="paragraph">
<p>To enable screen reader support for protected documents and websites, in the HP Wolf Security <strong>Dashboard</strong>, under <strong>Settings</strong> &gt; <strong>Threat Containment</strong> &gt; <strong>Accessibility</strong>, select:</p>
</div>
<div class="ulist">
<ul>
<li>
<p><strong>Enable support for screen readers when viewing protected documents or websites</strong></p>
</li>
<li>
<p><strong>View protected PDF documents in Secure Browser</strong></p>
<div class="imageblock">
<div class="content">
<img src="https://files.us.document360.io/ec5d82e2-88dc-4cc5-9e57-f56ea01dd0b4/Images/Documentation/dashboard-accessibility-options.jpg" alt="Wolf Dashboard Accessibility Options" width="70%">
</div>
</div>
</li>
</ul>
</div>
</div>
<div class="sect2">
<h3 id="_deployment">Deployment</h3>
<div class="paragraph">
<p>Screen reader support is available as opt-in to all devices and can be enabled as described above. If you want to enforce this feature on a set of devices, you can do this through the HP Wolf Security Controller.</p>
</div>
<div class="paragraph">
<p>You must:</p>
</div>
<div class="ulist">
<ul>
<li>
<p>Create a policy:</p>
<div class="ulist">
<ul>
<li>
<p>In HP Wolf Security Controller, create a policy named: <code>Enable Screen Reader Support</code>.</p>
</li>
<li>
<p>Add an <strong>Advanced parameter</strong> called <strong>Accessibility.Enable</strong> with a value of 1.</p>
</li>
<li>
<p>Add an <strong>Advanced parameter</strong> called <strong>Untrusted.UseSecureBrowserAsPdfViewer</strong> with a value of 1.</p>
</li>
</ul>
</div>
</li>
</ul>
</div>
<div class="paragraph">
<p>And:</p>
</div>
<div class="ulist">
<ul>
<li>
<p>Create a <code>Managed manually device group</code>:</p>
<div class="ulist">
<ul>
<li>
<p>Create a device group called: <code>Enable Screen Reader Support</code></p>
</li>
<li>
<p>Add devices to this group.</p>
</li>
<li>
<p>Apply the policy created above to this group.</p>
</li>
</ul>
</div>
</li>
</ul>
</div>
<div class="admonitionblock note">
<table>
<tr>
<td class="icon">
<div class="title">Note</div>
</td>
<td class="content">
We recommend applying this policy only to this group. If you apply the policy to your whole organization, then all users lose the ability to configure these settings directly on their devices.
</td>
</tr>
</table>
</div>
</div>
<div class="sect2">
<h3 id="_known_issues">Known issues</h3>
<table class="tableblock frame-all grid-all stretch">
<colgroup>
<col style="width: 13%;">
<col style="width: 87%;">
</colgroup>
<thead>
<tr>
<th class="tableblock halign-left valign-top"><strong>Reference</strong></th>
<th class="tableblock halign-left valign-top"><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td class="tableblock halign-left valign-top"><p class="tableblock"><strong>99863</strong></p></td>
<td class="tableblock halign-left valign-top"><p class="tableblock">Secure Browser may show an 'Aw, Snap!' error when browsing using the keyboard. To fix this issue, close and reopen the affected tab.</p></td>
</tr>
<tr>
<td class="tableblock halign-left valign-top"><p class="tableblock"><strong>99883</strong></p></td>
<td class="tableblock halign-left valign-top"><p class="tableblock">Certain websites in Secure Browser may get narrated when in the background. To workaround this issue, focus the website&#8217;s tab once before going back to your current tab.</p></td>
</tr>
<tr>
<td class="tableblock halign-left valign-top"><p class="tableblock"><strong>86274</strong></p></td>
<td class="tableblock halign-left valign-top"><p class="tableblock">PDF pages on Mozilla Firefox are not narrated.</p></td>
</tr>
<tr>
<td class="tableblock halign-left valign-top"><p class="tableblock"><strong>88800</strong></p></td>
<td class="tableblock halign-left valign-top"><p class="tableblock">Microsoft Narrator turns on scan mode automatically for certain browsers and applications, but not for Secure Browser. See <a href="https://support.microsoft.com/en-us/windows/appendix-b-narrator-keyboard-commands-and-touch-gestures-8bdab3f4-b3e9-4554-7f28-8b15bd37410a">Narrator keyboard commands and touch gestures</a> for more information from Microsoft about enabling Microsoft Narrator manually. After the first instance, Microsoft Narrator remembers this setting for future Secure Browser sessions.</p></td>
</tr>
</tbody>
</table>
<hr>
<div class="paragraph">
<p><strong>Disclaimer:</strong> This article was originally published in English. HP uses machine translation to localize content. If you notice any errors, unclear information, or content that seems misleading, <a href="mailto:wps.support@hpwolf.com">open a support ticket</a>.</p>
</div>
</div>
</div>
</div>
</div>
<div id="footer">
<div id="footer-text">
Last updated 2026-06-12 10:19:18 UTC
</div>
</div>
