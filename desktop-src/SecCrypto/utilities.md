---
description: Proporciona funcionalidad para la generación de números aleatorios, las conversiones y la codificación y descodificación de Base64.
ms.assetid: c0073361-5d0d-4915-8110-02f6e1e0714e
title: Objeto Utilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2f6000179b1752630f02d03aa5c87dea11364d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671403"
---
# <a name="utilities-object"></a>Objeto Utilities

\[El objeto **Utilities** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]

El objeto **Utilities** proporciona funcionalidad para la generación de números aleatorios, las conversiones y la codificación y descodificación de Base64.

## <a name="when-to-use"></a>Cuándo se usa

El objeto **Utilities** se usa para realizar las siguientes tareas:

-   Codifique una cadena como base64 o descodifique una cadena de Base64.
-   Convierte una cadena empaquetada en binaria en una matriz de bytes y viceversa.
-   Convierte una cadena empaquetada en binaria en una cadena hexadecimal y viceversa.
-   Generar un número aleatorio seguro.
-   Convertir la hora local en hora universal coordinada (hora del meridiano de Greenwich) y viceversa.

## <a name="members"></a>Miembros

El objeto **Utilities** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El objeto **Utilities** tiene estos métodos.



| Método                                                               | Descripción                                                                  |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Base64Decode**](utilities-base64decode.md)                       | Descodifica una cadena de Base64.<br/>                                     |
| [**Base64Encode**](utilities-base64encode.md)                       | Codifica una cadena como Base64.<br/>                                       |
| [**BinaryStringToByteArray**](utilities-binarystringtobytearray.md) | Convierte una cadena empaquetada en binaria en una matriz de bytes.<br/>             |
| [**BinaryToHex**](utilities-binarytohex.md)                         | Convierte una cadena empaquetada en binaria en una cadena hexadecimal.<br/>          |
| [**ByteArrayToBinaryString**](utilities-bytearraytobinarystring.md) | Convierte una matriz de bytes en una cadena empaquetada como binaria.<br/>             |
| [**GetRandom**](utilities-getrandom.md)                             | Genera un número aleatorio seguro.<br/>                                 |
| [**HexToBinary**](utilities-hextobinary.md)                         | Convierte una cadena hexadecimal en una cadena empaquetada como binaria.<br/>          |
| [**LocalTimeToUTCTime**](utilities-localtimetoutctime.md)           | Convierte la hora local del equipo en hora universal coordinada.<br/> |
| [**UTCTimeToLocalTime**](utilities-utctimetolocaltime.md)           | Convierte la hora universal coordinada en la hora local del equipo.<br/> |



 

## <a name="remarks"></a>Observaciones

Se puede crear el objeto **Utilities** y es seguro para el scripting. El ProgID del objeto **Utilities** es CAPICOM. Utilities. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




