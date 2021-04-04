---
title: Establecer permisos en un grupo de propiedades
description: Los permisos se pueden aplicar a un grupo de propiedades.
ms.assetid: cb9f6c04-be94-45b4-ba84-2a79b7625fdd
ms.tgt_platform: multiple
keywords:
- Establecer permisos en un grupo de propiedades AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f2993a537b76b64c7e8e6323c850494b3ce306
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789459"
---
# <a name="setting-permissions-on-a-group-of-properties"></a>Establecer permisos en un grupo de propiedades

Los permisos se pueden aplicar a un grupo de propiedades. Un conjunto de propiedades se identifica mediante el GUID en el atributo [**rightsGUID**](/windows/desktop/ADSchema/a-rightsguid) de un objeto [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright) . Este GUID se establece en el atributo [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid) del objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de cada atributo del grupo.

En el procedimiento siguiente se muestra cómo establecer permisos que se aplican a un grupo de propiedades de objeto.

**Para establecer permisos que se aplican a un grupo de propiedades de objeto**

1.  Establezca la propiedad [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ right \_ DS \_ Read \_ prop**, **ADS \_ right \_ DS \_ Write \_ prop** o ambos valores combinados.
2.  Establezca la propiedad [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS AceType \_ el \_ \_ \_ objeto permitido acceso** o **en \_ ADS \_ AceType \_ acceso denegado \_**.
3.  Establezca la propiedad [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el GUID del conjunto de propiedades. Esta es la propiedad [**rightsGUID**](/windows/desktop/ADSchema/a-rightsguid) del objeto [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright) que identifica el conjunto de propiedades. Este GUID también se establece como [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid) en el objeto attributeSchema de cada propiedad del grupo.
4.  Establezca la propiedad [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **tipo de \_ objeto marca de ADS \_ \_ \_ presente**.

Tenga en cuenta que no debe establecer la marca de **\_ \_ \_ \_ acceso de control DS right de ad** en la propiedad [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) . Esta marca solo se usa para especificar un derecho de acceso de control.

Para obtener más información y un ejemplo de código que se puede usar para establecer derechos de acceso para un conjunto de propiedades, consulte el [código de ejemplo para establecer permisos en un grupo de propiedades](example-code-for-setting-permissions-on-a-group-of-properties.md).

Para obtener más información sobre la creación de una ACE, consulte [configuración de derechos de acceso en un objeto](setting-access-rights-on-an-object.md).

Para obtener más información y un ejemplo de código que se puede usar para establecer una ACE para un conjunto de propiedades, consulte el [código de ejemplo para establecer una ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 