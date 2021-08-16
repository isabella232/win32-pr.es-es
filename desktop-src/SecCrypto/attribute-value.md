---
description: Establece o recupera el valor del atributo.
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Attribute.Value, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41737e086f1889531322115c8ff57e64c8893063f498b2566f0010f0f3f0ca30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773709"
---
# <a name="attributevalue-property"></a>Attribute.Value, propiedad

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use [**la clase CryptographicAttributeObject en**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) el espacio de nombres [**System.Security.Cryptography.**](/previous-versions/windows/)\]

La **propiedad Value** establece o recupera el valor del atributo.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a>Valor de propiedad

Variable **Variant** que contiene el valor del atributo. Para los **atributos CAPICOM \_ AUTHENTICATED \_ ATTRIBUTE SIGNING \_ \_ TIME,** el tipo de datos es **DATE**. Para todos los demás atributos, el valor de propiedad es una cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
