---
description: La función LookupByteSetString devuelve la cadena correspondiente al valor especificado de un conjunto etiquetado.
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: Función LookupByteSetString (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupByteSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 208f7cef1a658ae321d7ce03aaee763e5387b5a45985d59134418a4d136e0b56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742505"
---
# <a name="lookupbytesetstring-function"></a>Función LookupByteSetString

La **función LookupByteSetString** devuelve la cadena correspondiente al valor especificado de un conjunto etiquetado.

## <a name="syntax"></a>Sintaxis


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpSet* 
</dt> <dd>

Puntero a un conjunto etiquetado, del que puede extraer la etiqueta del valor.

</dd> <dt>

*Valor* 
</dt> <dd>

Valor de un conjunto etiquetado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es una cadena correspondiente al valor proporcionado.

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




