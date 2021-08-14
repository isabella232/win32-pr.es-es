---
title: Proteger objetos de los efectos de los derechos heredados
description: Como se describe en el tema Herencia y delegación de administración, las ACE se pueden establecer en un objeto de contenedor, como una organizationalUnit, domainDNS, un contenedor, entre otros, y propagarse a objetos secundarios en función de las marcas ACE establecidas en esas ACE.
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- Protección de objetos de los efectos de los derechos heredados de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcc1067fcfe0d57e2e7aca837b97d73f18b55a41a4f1347ac36224b987918aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185020"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a>Proteger objetos de los efectos de los derechos heredados

Como se describe en el tema Herencia y delegación de [administración,](inheritance-and-delegation-of-administration.md)las ACE se pueden establecer en un objeto contenedor, como **una unidad** organizativa , **domainDNS,** **contenedor,** y así sucesivamente, y propagarse a objetos secundarios en función de las marcas ACE establecidas en esas ACE.

Si tiene un objeto seguro o un objeto cuyaSA desea controlar explícitamente, como una unidad organizativa privada o un usuario especial, puede evitar que las ACE se propaguen al objeto por su contenedor primario o por sus predecesores.

Use la [**propiedad IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para controlar si el objeto hereda las DACL y las SACL de su contenedor primario.

La [**propiedad IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) se puede usar para proteger un objeto de los efectos de las ACE heredadas. Las marcas siguientes obligan a establecer el control de acceso explícitamente en el objeto e impiden que un usuario modifique el control de acceso al objeto estableciendo las ACE heredables en el contenedor primario del objeto o en sus predecesores.



| Marca                               | Descripción                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_SE DACL \_ PROTECTED**<br/> | Impide que las ACE establecidas en la DACL del contenedor primario y los objetos situados por encima del contenedor primario de la jerarquía de directorios se apliquen a la DACL del objeto.<br/> |
| **\_SE SACL \_ PROTECTED**<br/> | Impide que las ACE establecidas en la SACL del contenedor primario y los objetos situados por encima del contenedor primario de la jerarquía de directorios se apliquen a la SACL del objeto.<br/> |



 

Tenga en cuenta que SE la marca **\_ DACL \_ PRESENT** debe estar presente para establecer **SE \_ DACL \_ PROTECTED** y SE **\_ SACL \_ PRESENT** debe estar presente para establecer SE **\_ SACL \_ PROTECTED**.

 

