---
title: Creación de un nuevo grupo
description: Joe Worden, el administrador de la empresa, debe crear un nuevo grupo.
ms.assetid: a1bea695-d43f-47e6-af74-ba5abb0116a2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3f778e9eb953b60ca45665bcd92ff30efb9c111c959e78cf1824407d0a459c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962014"
---
# <a name="creating-a-new-group"></a>Creación de un nuevo grupo

Joe Worden, el administrador de la empresa, debe crear un nuevo grupo. Le gustaría proteger algunos recursos, como archivos, objetos Active Directory u otros objetos, en función de la pertenencia de este grupo. En el ejemplo de código siguiente se muestra cómo crear un nuevo grupo.


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



Este grupo, Administración, se creará en la unidad organizativa Ventas. En primer lugar, Joe debe crear un objeto ADSI para la unidad organizativa Ventas. En segundo lugar, debe establecer el [**atributo samAccountName**](/windows/desktop/AD/group-objects) en este objeto, ya que es un atributo obligatorio para la compatibilidad con versiones anteriores. En este ejemplo, cuando **se establece samAccountName,** Windows herramientas nt 4.0 como el Administrador de usuarios ven el atributo **como mgmt** en lugar de **como administración**.

En tercer lugar, Joe debe especificar el tipo de grupo. En un Windows 2000, hay tres tipos de grupos: Global, Domain Local y Universal. Además, el grupo tiene su característica de seguridad. Un grupo puede ser un grupo habilitado para la seguridad o un grupo no protegido. Básicamente, los grupos habilitados para seguridad son aquellos a los que se pueden conceder o denegar derechos de acceso a los recursos, de forma similar a un usuario. Conceder a un grupo acceso a un recurso compartido de archivos, por ejemplo, implica que todos los miembros del grupo pueden acceder al recurso compartido de archivos. Las listas de distribución no se pueden usar de forma similar; por ejemplo, no se puede conceder a una lista de distribución el derecho de acceso a un recurso compartido de archivos. Durante la actualización, los Windows NT 4.0 se migran como grupos habilitados para seguridad. Los grupos no protegidos de Active Directory son similares a las listas de distribución de Exchange. Por lo tanto, la creación de grupos o listas de distribución son operaciones similares en Windows 2000. En el modo nativo Windows 2000 (el modo nativo significa que todos los controladores de dominio de un dominio son equipos que ejecutan Windows 2000 Server), los grupos se pueden anidar en cualquier nivel.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumerar objetos](enumerating-objects.md)
</dt> </dl>

 

 