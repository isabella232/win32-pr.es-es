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
ms.openlocfilehash: 727aa28edf14a038ec4667d1705a82f6fd3a2c3bc4a4c4e5ba0e6bf743d143d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896634"
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

## <a name="remarks"></a>Comentarios

La codificación Base64 es el esquema utilizado para transmitir datos binarios. Base64 procesa los datos como grupos de 24 bits, asignando estos datos a cuatro caracteres codificados. La codificación Base64 a veces se conoce como codificación 3 a 4. Cada 6 bits del grupo de 24 bits se usa como índice en una tabla de asignación (el alfabeto base64) para obtener un carácter para los datos codificados. Los datos codificados tienen longitudes de línea limitadas a 76 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Utilidades**](utilities.md)
</dt> </dl>

 

 




