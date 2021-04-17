---
description: La función LookupWordSetString devuelve la cadena correspondiente al valor solicitado de un conjunto con etiqueta.
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: Función LookupWordSetString (Netmon. h)
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
ms.openlocfilehash: 7487becb195571e1eb88044195293b2c0b226e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542374"
---
# <a name="lookupwordsetstring-function"></a>LookupWordSetString función)

La función **LookupWordSetString** devuelve la cadena correspondiente al valor solicitado de un conjunto con etiqueta.

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

Conjunto con etiqueta del que se extrae la etiqueta del valor.

</dd> <dt>

*Valor* 
</dt> <dd>

Valor de un conjunto con etiqueta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es una cadena que corresponde al valor solicitado.

Si la función no es correcta, el valor especificado no está en el conjunto, el valor devuelto es **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Analizador. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




