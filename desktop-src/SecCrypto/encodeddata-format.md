---
description: Devuelve una representación de cadena de los datos codificados.
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: Método EncodedData.Format
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Format
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b3d4316a2de24410a14d496b71e46746ea580109f8d6ede10c4c1a0f57fc22f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874875"
---
# <a name="encodeddataformat-method"></a>Método EncodedData.Format

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase AsnEncodedData en**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) el espacio de nombres [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **método Format** devuelve una representación de cadena de los datos codificados.

## <a name="syntax"></a>Sintaxis


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bMultiLines* \[ in, opcional\]
</dt> <dd>

Valor booleano que indica si la cadena devuelta contiene varias líneas. Si **es True**, la cadena devuelta puede contener varias líneas separadas por **vbCrLf**. El valor predeterminado es **False**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cadena legible que representa los datos codificados. Si CAPICOM no entiende los datos codificados, se devuelve una representación hexadecimal de los datos.

## <a name="remarks"></a>Comentarios

El formato de la cadena devuelta puede cambiar entre diferentes versiones de CAPICOM. No se base en ningún formato concreto de la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EncodedData**](encodeddata.md)
</dt> </dl>

 

 
