---
description: Recupera los datos codificados.
ms.assetid: 8e07ac14-6859-410f-ab30-84b8d60a94ad
title: Propiedad EncodedData.Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 57137e91418cc0804fb694c90f4439a0c9acfd105e3d9e5a936675c5e078665f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766710"
---
# <a name="encodeddatavalue-property"></a>Propiedad EncodedData.Value

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase AsnEncodedData en**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) el espacio de nombres [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **propiedad Value** recupera los datos codificados. Esta es la propiedad predeterminada.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
EncodedData.Value( _
  [ ByVal EncodingType ] _
) As String
```



## <a name="property-value"></a>Valor de propiedad

Cadena que contiene los datos codificados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
