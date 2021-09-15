---
description: Descodifica una cadena de base64.
ms.assetid: acf2dba6-a0e8-4b77-a5a6-93cfa6afe874
title: Método Utilities.Base64Decode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Decode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df0a0e2a0400ef2000ce5e54e1a76a1a4bd8eebd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127477643"
---
# <a name="utilitiesbase64decode-method"></a>Método Utilities.Base64Decode

\[El **método Base64Decode** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos.\]

El **método Base64Decode** descodifica una cadena de base64.

## <a name="syntax"></a>Sintaxis


```VB
Utilities.Base64Decode( _
  ByVal EncodedString _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EncodedString* \[ En\]
</dt> <dd>

Cadena codificada en base64 que se descodificará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La cadena descodificada.

## <a name="remarks"></a>Observaciones

La codificación Base64 es el esquema que se usa para transmitir datos binarios. Base64 procesa los datos como grupos de 24 bits, asignando estos datos a cuatro caracteres codificados. La codificación Base64 a veces se conoce como codificación de 3 a 4. Cada 6 bits del grupo de 24 bits se usa como índice en una tabla de asignación (el alfabeto base64) para obtener un carácter para los datos codificados. Los datos codificados tienen longitudes de línea limitadas a 76 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Sectores públicos**](utilities.md)
</dt> </dl>

 

 




