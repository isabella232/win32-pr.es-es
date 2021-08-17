---
description: La función LookupWordSetString devuelve la cadena correspondiente al valor solicitado de un conjunto etiquetado.
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: Función LookupWordSetString (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupWordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 15b529076660eec093df370df47823fb21aa13e53cce61565fe82de7fbb7e017
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364723"
---
# <a name="lookupwordsetstring-function"></a>Función LookupWordSetString

La **función LookupWordSetString** devuelve la cadena correspondiente al valor solicitado de un conjunto etiquetado.

## <a name="syntax"></a>Sintaxis


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpSet* 
</dt> <dd>

Conjunto etiquetado del que se extrae la etiqueta del valor.

</dd> <dt>

*Valor* 
</dt> <dd>

Valor de un conjunto etiquetado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es una cadena que corresponde al valor solicitado.

Si la función no se realiza correctamente, el valor especificado no está en el conjunto, el valor devuelto es **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




