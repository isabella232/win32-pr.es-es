---
title: Establecer derechos en tipos específicos de objetos
description: En el procedimiento siguiente se muestra cómo establecer una ACE que solo puede heredar una clase específica de objetos .
ms.assetid: 42712458-69c7-4fe1-bfb3-b3fb28092a56
ms.tgt_platform: multiple
keywords:
- establecimiento de derechos en tipos de objetos de AD
- objetos de AD , estableciendo derechos en
- Active Directory, usar, seguridad, establecer derechos para tipos de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d8740b4454eac5de158c826ec135a0becf6777f320e16729598187a3093f088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183293"
---
# <a name="setting-rights-to-specific-types-of-objects"></a>Establecer derechos en tipos específicos de objetos

En el procedimiento siguiente se muestra cómo establecer una ACE que solo puede heredar una clase específica de objetos .

 **Para establecer una ACE que solo puede heredar una clase específica de objetos**

1.  Establezca la [**propiedad IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ ACETYPE ACCESS ALLOWED \_ \_ \_ OBJECT** o **ADS \_ ACETYPE ACCESS DENIED \_ \_ \_ OBJECT**.
2.  Establezca la [**propiedad IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para incluir la marca \_ ACEFLAG \_ INHERIT ACE de \_ ADS.
3.  Establezca la [**propiedad IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **el schemaIDGUID** de la clase de objeto que puede heredar la ACE.
4.  Establezca la [**propiedad IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS FLAG \_ \_ INHERITED OBJECT TYPE \_ \_ PRESENT**.

> [!IMPORTANT]
> Establezca **ADS \_ ACEFLAG INHERIT \_ \_ ACE** para que la ACE se herede. Además, debe establecer **ADS \_ ACEFLAG INHERIT ONLY \_ \_ \_ ACE** si el tipo de objeto al que se aplica esta ACE no coincide con el tipo de objeto del contenedor donde se especifica la ACE. Si esto no se hace, la ACE también se hará efectiva en el contenedor y puede conceder derechos no deseados.

 

Para obtener más información y ejemplos de código que se pueden usar para establecer este tipo de ACE, vea Código de ejemplo para establecer una [ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 