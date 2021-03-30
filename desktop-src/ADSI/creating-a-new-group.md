---
title: Creación de un nuevo grupo
description: Joe Worden, el administrador de la empresa, debe crear un nuevo grupo.
ms.assetid: a1bea695-d43f-47e6-af74-ba5abb0116a2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a4f46d595aa892ac75aa67d14bbc0356122271
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995635"
---
# <a name="creating-a-new-group"></a>Creación de un nuevo grupo

Joe Worden, el administrador de la empresa, debe crear un nuevo grupo. Le gustaría proteger algunos recursos, como archivos, Active Directory objetos u otros objetos, en función de la pertenencia de este grupo. En el ejemplo de código siguiente se muestra cómo crear un nuevo grupo.


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



Este grupo, administración, se creará en la unidad organizativa ventas. En primer lugar, Joe debe crear un objeto ADSI para la unidad organizativa sales. En segundo lugar, debe establecer el atributo [**samAccountName**](/windows/desktop/AD/group-objects) en este objeto, ya que es un atributo obligatorio por compatibilidad con versiones anteriores. En este ejemplo, cuando se establece **samAccountName** , las herramientas de Windows NT 4,0 como User Manager ven el atributo como **MGMT** en lugar de **Management**.

En tercer lugar, Joe debe especificar el tipo de grupo. En un dominio de Windows 2000, hay tres tipos de grupos: global, local de dominio y universal. Además, el grupo lleva su característica de seguridad. Un grupo puede ser un grupo con seguridad habilitada o no protegido. Esencialmente, los grupos con seguridad habilitada son aquellos a los que se puede conceder o denegar derechos de acceso a los recursos, de manera similar a un usuario. La concesión de acceso a un grupo a un recurso compartido de archivos, por ejemplo, implica que todos los miembros del grupo pueden tener acceso al recurso compartido de archivos. Las listas de distribución no se pueden usar de forma similar; por ejemplo, no se puede conceder a una lista de distribución el derecho a tener acceso a un recurso compartido de archivos. Durante la actualización, los grupos de Windows NT 4,0 se migran como grupos con seguridad habilitada. Los grupos no seguros en Active Directory son similares a las listas de distribución de Exchange. Por lo tanto, la creación de grupos o listas de distribución es una operación similar en Windows 2000. En el modo nativo de Windows 2000 (el modo nativo significa que todos los controladores de dominio de un dominio son equipos que ejecutan Windows 2000 Server), los grupos se pueden anidar en cualquier nivel.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumerar objetos](enumerating-objects.md)
</dt> </dl>

 

 