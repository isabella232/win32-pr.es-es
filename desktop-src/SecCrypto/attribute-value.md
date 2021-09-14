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
ms.openlocfilehash: 6b3d2f41c56fc47277bd71354279e75b423d0c0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253532"
---
# <a name="attributevalue-property"></a>Attribute.Value, propiedad

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use [**la clase CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio [**de nombres System.Security.Cryptography.**](/previous-versions/windows/)\]

La **propiedad Value** establece o recupera el valor del atributo.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a>Valor de propiedad

Variable **Variant** que contiene el valor del atributo. Para los **atributos \_ CAPICOM AUTHENTICATED ATTRIBUTE SIGNING \_ \_ \_ TIME,** el tipo de datos es **DATE**. Para todos los demás atributos, el valor de propiedad es una cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
