---
description: La función LookupDwordSetString devuelve la cadena correspondiente al valor especificado de un conjunto etiquetado.
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: Función LookupDwordSetString (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b72f21d47001e2060c3b27daa80a584dcad77b55fd1df289a5bdb5476549cf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677235"
---
# <a name="lookupdwordsetstring-function"></a>Función LookupDwordSetString

La **función LookupDwordSetString** devuelve la cadena correspondiente al valor especificado de un conjunto etiquetado.

## <a name="syntax"></a>Sintaxis


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpSet* 
</dt> <dd>

Conjunto etiquetado, del que puede extraer la etiqueta del valor.

</dd> <dt>

*Valor* 
</dt> <dd>

Valor de un conjunto etiquetado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es la cadena que corresponde al valor especificado.

Si la función no se realiza correctamente, el valor especificado no está en el conjunto, el valor devuelto es **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




