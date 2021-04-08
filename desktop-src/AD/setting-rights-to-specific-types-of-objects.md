---
title: Establecer derechos en tipos específicos de objetos
description: En el procedimiento siguiente se muestra cómo establecer una ACE que solo puede ser heredada por una clase específica de objetos.
ms.assetid: 42712458-69c7-4fe1-bfb3-b3fb28092a56
ms.tgt_platform: multiple
keywords:
- establecer derechos en tipos de objetos AD
- objetos AD, establecer derechos
- Active Directory, usar, seguridad, establecer derechos en tipos de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f44cfbe753e6f92787f8269eab1f4eab4c2e98
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995058"
---
# <a name="setting-rights-to-specific-types-of-objects"></a>Establecer derechos en tipos específicos de objetos

En el procedimiento siguiente se muestra cómo establecer una ACE que solo puede ser heredada por una clase específica de objetos.

 **Para establecer una ACE que solo puede ser heredada por una clase específica de objetos**

1.  Establezca la propiedad [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ AceType \_ acceso \_ a \_ objetos permitidos** o **anuncios \_ AceType \_ acceso \_ denegado \_**.
2.  Establezca la propiedad [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para incluir la \_ marca ADS ACEFLAG \_ inherit \_ ACE.
3.  Establezca la propiedad [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **schemaIDGUID** de la clase de objeto que puede heredar la ACE.
4.  Establezca la propiedad [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **tipo de \_ \_ objeto heredado marca de ADS \_ \_ presente**.

> [!IMPORTANT]
> Establezca **ad \_ ACEFLAG \_ inherit \_ ACE** para que la ACE se herede. Además, si el tipo de objeto al que se aplica esta ACE no coincide con el tipo de objeto del contenedor en el que se especifica la ACE, debe establecer la **\_ ACE ACEFLAG de \_ \_ \_ solo heredar** . Si no se hace esto, la ACE también entrará en vigor en el contenedor y podrá conceder derechos no deseados.

 

Para obtener más información y ejemplos de código que se pueden usar para establecer este tipo de ACE, vea [código de ejemplo para establecer una ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 