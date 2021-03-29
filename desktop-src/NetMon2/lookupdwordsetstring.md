---
description: La función LookupDwordSetString devuelve la cadena correspondiente al valor especificado de un conjunto con etiqueta.
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: Función LookupDwordSetString (Netmon. h)
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
ms.openlocfilehash: 57688edab7421f939e03322b8b244219b00d31fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810291"
---
# <a name="lookupdwordsetstring-function"></a>LookupDwordSetString función)

La función **LookupDwordSetString** devuelve la cadena correspondiente al valor especificado de un conjunto con etiqueta.

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

Conjunto con etiqueta, desde el que puede extraer la etiqueta del valor.

</dd> <dt>

*Valor* 
</dt> <dd>

Valor de un conjunto con etiqueta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es la cadena que corresponde al valor especificado.

Si la función no es correcta, el valor especificado no está en el conjunto, el valor devuelto es **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Analizador. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




