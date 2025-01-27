---
title: Roles in an enterprise
intro: 'Everyone in an enterprise is a member of the enterprise. To control access to your enterprise''s settings and data, you can assign different roles to members of your enterprise.'
product: '{% data reusables.gated-features.enterprise-accounts %}'
redirect_from:
  - /github/setting-up-and-managing-your-enterprise-account/roles-for-an-enterprise-account
  - /articles/permission-levels-for-a-business-account/
  - /articles/roles-for-an-enterprise-account
  - /github/setting-up-and-managing-your-enterprise/roles-in-an-enterprise
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
topics:
  - Enterprise
---

## About roles in an enterprise

Everyone in an enterprise is a member of the enterprise. You can also assign administrative roles to members of your enterprise. Each administrator role maps to business functions and provides permissions to do specific tasks within the enterprise.

{% data reusables.enterprise-accounts.enterprise-administrators %}

{% ifversion fpt %}
If your enterprise does not use {% data variables.product.prodname_emus %}, you can invite someone to an administrative role using a user account on {% data variables.product.product_name %} that they control. For more information, see "[Inviting people to manage your enterprise](/github/setting-up-and-managing-your-enterprise/inviting-people-to-manage-your-enterprise)".

In an enterprise using {% data variables.product.prodname_emus %}, new owners and members must be provisioned through your identity provider. Enterprise owners and organization owners cannot add new members or owners to the enterprise using {% data variables.product.prodname_dotcom %}. You can select a member's enterprise role using your IdP and it cannot be changed on {% data variables.product.prodname_dotcom %}. You can select a member's role in an organization on {% data variables.product.prodname_dotcom %}. For more information, see "[About {% data variables.product.prodname_emus %}](/github/setting-up-and-managing-your-enterprise/managing-your-enterprise-users-with-your-identity-provider/about-enterprise-managed-users)."
{% else %}
For more information about adding people to your enterprise, see "[Authentication](/admin/authentication)".

{% endif %}

## Enterprise-Inhaber

Enterprise owners have complete control over the enterprise and can take every action, including:
- Administratoren verwalten
- {% ifversion fpt %}Adding and removing {% elsif ghae or ghes %}Managing{% endif %} organizations {% ifversion fpt %}to and from {% elsif ghae or ghes %} in{% endif %} the enterprise
- Enterprise-Einstellungen verwalten
- Richtlinien organisationsübergreifend durchsetzen
{% ifversion fpt %}- Managing billing settings{% endif %}

Keinen Zugriff haben Enterprise-Inhaber auf die Einstellungen und Inhalte der einzelnen Organisationen, es sei denn, sie sind auch Inhaber einer Organisation oder ihnen wird direkter Zugriff auf das Repository einer Organisation erteilt. Similarly, owners of organizations in your enterprise do not have access to the enterprise itself unless you make them enterprise owners.

An enterprise owner will only consume a license if they are an owner or member of at least one organization within the enterprise. {% ifversion fpt %}Enterprise owners must have a personal account on {% data variables.product.prodname_dotcom %}.{% endif %} As a best practice, we recommend making only a few people in your company enterprise owners, to reduce the risk to your business.

## Enterprise-Mitglieder

Members of organizations owned by your enterprise are also automatically members of the enterprise. Members can collaborate in organizations and may be organization owners, but members cannot access or configure enterprise settings{% ifversion fpt %}, including billing settings{% endif %}.

People in your enterprise may have different levels of access to the various organizations owned by your enterprise and to repositories within those organizations. Du kannst anzeigen, auf welche Ressourcen die einzelnen Personen Zugriff haben. For more information, see "[Viewing people in your enterprise](/github/setting-up-and-managing-your-enterprise/viewing-people-in-your-enterprise)."

Weitere Informationen zu den Berechtigungen auf Organisationsebene findest Du unter „[Berechtigungsebenen für eine Organisation](/articles/permission-levels-for-an-organization).“

People with outside collaborator access to repositories owned by your organization are also listed in your enterprise's People tab, but are not enterprise members and do not have any access to the enterprise. Weitere Informationen zu den Berechtigungen externer Mitarbeiter findest Du unter „[Berechtigungsebenen für eine Organisation](/articles/permission-levels-for-an-organization#outside-collaborators).“

{% ifversion fpt %}

## Abrechnungsmanager

Billing managers only have access to your enterprise's billing settings. Billing managers for your enterprise can:
- Benutzerlizenzen, {% data variables.large_files.product_name_short %}-Pakete und andere Abrechnungseinstellungen anzeigen und verwalten
- Liste der Abrechnungsmanager anzeigen
- Andere Abrechnungsmanager hinzufügen oder entfernen

Billing managers will only consume a license if they are an owner or member of at least one organization within the enterprise. Billing managers do not have access to organizations or repositories in your enterprise, and cannot add or remove enterprise owners. Abrechnungsmanager müssen über ein persönliches Konto auf {% data variables.product.prodname_dotcom %} verfügen.

## About support entitlements

{% data reusables.enterprise-accounts.support-entitlements %}

## Weiterführende Informationen

- „[Informationen zu Enterprise-Konten](/articles/about-enterprise-accounts)“

{% endif %}
