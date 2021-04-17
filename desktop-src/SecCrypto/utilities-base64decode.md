---
description: Descodifica una cadena de Base64.
ms.assetid: acf2dba6-a0e8-4b77-a5a6-93cfa6afe874
title: Utilities. Base64Decode (método)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690391"
---
# <a name="utilitiesbase64decode-method"></a>Utilities. Base64Decode (método)

\[El método **Base64Decode** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]

El método **Base64Decode** descodifica una cadena de Base64.

## <a name="syntax"></a>Sintaxis


```VB
Utilities.Base64Decode( _
  ByVal EncodedString _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EncodedString* \[ de\]
</dt> <dd>

Cadena codificada en Base64 que se va a descodificar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La cadena descodificada.

## <a name="remarks"></a>Observaciones

La codificación Base64 es el esquema que se usa para transmitir datos binarios. Base64 procesa los datos como grupos de 24 bits, asignando estos datos a cuatro caracteres codificados. La codificación Base64 a veces se conoce como codificación de 3 a 4. Cada 6 bits del grupo de 24 bits se utiliza como índice en una tabla de asignación (el alfabeto Base64) para obtener un carácter para los datos codificados. Los datos codificados tienen longitudes de línea que están limitadas a 76 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Sectores públicos**](utilities.md)
</dt> </dl>

 

 




