---
description: El monitor llama a la función LoadIPXAddresses para rellenar una lista de direcciones IPX tomada de una variable de cadena de configuración HTML.
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: Función LoadIPXAddresses (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPXAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ed8bb6948102e8d28150edf102fa261c9c7f7adfcf105e377352054304b352df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677315"
---
# <a name="loadipxaddresses-function"></a>Función LoadIPXAddresses

El monitor llama a la función **LoadIPXAddresses** para rellenar una lista de direcciones IPX tomada de una variable de cadena de configuración HTML.

## <a name="syntax"></a>Sintaxis


```C++
BOOL LoadIPXAddresses(
  _In_  const char        *pConfig,
  _In_  const char        *pVarName,
  _Out_       IPX_ADDRESS **ppAddresses,
  _Out_       DWORD       *pNumAddresses
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pConfig* \[ En\]
</dt> <dd>

Puntero a la cadena de configuración HTML pasada al monitor por el [método IMonitor::D oConfigure.](imonitor-doconfigure.md)

</dd> <dt>

*pVarName* \[ En\]
</dt> <dd>

Puntero al nombre de la variable en la cadena de configuración.

</dd> <dt>

*ppAddresses* \[ out\]
</dt> <dd>

Puntero a un puntero a una matriz de direcciones. Si se encuentra la variable especificada en *pVarName* y tiene una longitud que no es cero, se asigna suficiente espacio (mediante **HeapAllocMemory)** y todas las direcciones IPX se almacenan como una matriz.

</dd> <dt>

*pNumAddresses* \[ out\]
</dt> <dd>

Puntero a la variable **DWORD** que se establece en el número de direcciones IPX tomadas de la cadena de configuración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente (se encontró el nombre de la variable y tenía una cadena de longitud no cero que representara direcciones IPX), el valor devuelto es **TRUE.**

Si la función no se realiza correctamente, el valor devuelto es **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




