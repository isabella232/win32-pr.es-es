---
description: Devuelve una representación de cadena de los datos codificados.
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: EncodedData. Format (método)
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
ms.openlocfilehash: 435d0fdcd6e2bbd8c446c38f97012d820dbe5c7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650053"
---
# <a name="encodeddataformat-method"></a>EncodedData. Format (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El método **Format** devuelve una representación de cadena de los datos codificados.

## <a name="syntax"></a>Sintaxis


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bMultiLines* \[ en, opcional\]
</dt> <dd>

Valor booleano que indica si la cadena devuelta contiene varias líneas. Si **es true**, la cadena devuelta puede contener varias líneas separadas por **vbCrLf**. El valor predeterminado es **False**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cadena legible que representa los datos codificados. Si CAPICOM no entiende los datos codificados, se devuelve una representación hexadecimal de los datos.

## <a name="remarks"></a>Observaciones

El formato de la cadena devuelta puede cambiar entre las distintas versiones de CAPICOM. No confíe en ningún formato determinado en la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EncodedData**](encodeddata.md)
</dt> </dl>

 

 
