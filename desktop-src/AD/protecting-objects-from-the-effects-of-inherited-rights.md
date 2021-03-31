---
title: Protección de objetos a partir de los efectos de los derechos heredados
description: Como se describe en el tema herencia y delegación de la administración, las ACE se pueden establecer en un objeto contenedor, como organizationalUnit, domainDNS, contenedor, etc., y propagarse a objetos secundarios en función de las marcas ACE establecidas en esas ACE.
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- Protección de objetos a partir de los efectos de AD de derechos heredados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e49991cd8a479e05b024c6ea2538783a843025
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077505"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a>Protección de objetos a partir de los efectos de los derechos heredados

Como se describe en el tema [herencia y delegación de la administración](inheritance-and-delegation-of-administration.md), las ACE se pueden establecer en un objeto contenedor, como **organizationalUnit**, **domainDNS**, **contenedor**, etc., y propagarse a objetos secundarios en función de las marcas ACE establecidas en esas ACE.

Si tiene un objeto seguro o un objeto cuyas ACE desea controlar explícitamente, como una unidad organizativa privada o un usuario especial, puede evitar que las ACE se propaguen al objeto por su contenedor primario o sus predecesoras del contenedor principal.

Use la propiedad [**IADsSecurityDescriptor. control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para controlar si el objeto hereda DACL y SACL de su contenedor primario.

La propiedad [**IADsSecurityDescriptor. control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) se puede usar para proteger un objeto de los efectos de las ACE heredadas. Las marcas siguientes obligan a que el control de acceso se establezca explícitamente en el objeto e impidan que un usuario modifique el control de acceso al objeto mediante el establecimiento de ACE heredables en el contenedor primario del objeto o de sus predecesores principales.



| Marca                               | Descripción                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DACL de SE \_ \_ protegió**<br/> | Impide que se apliquen las ACE establecidas en la DACL del contenedor principal y los objetos situados por encima del contenedor primario en la jerarquía de directorios a la DACL de objeto.<br/> |
| **SE \_ \_ protegió SACL**<br/> | Impide que se apliquen las ACE establecidas en la SACL del contenedor principal y los objetos situados por encima del contenedor primario en la jerarquía de directorios a la SACL del objeto.<br/> |



 

Tenga en cuenta que la marca de **DACL de se \_ \_** debe presentar para establecer que la **\_ DACL \_ protegida** y la **SACL de se \_ \_** presente deben estar presentes para establecer la **\_ SACL \_ protegida**.

 

