---
description: El monitor llama a la función LoadMACAddresses para rellenar una lista de direcciones MAC con direcciones tomadas de una variable de cadena de configuración HTML.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: Función LoadMACAddresses (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadMACAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2de609ef0a1e820785ee7d62cbbe1e6af32c633aa29b133974f6f5f6f2a649b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742725"
---
# <a name="loadmacaddresses-function"></a>Función LoadMACAddresses

El monitor llama a la función **LoadMACAddresses** para rellenar una lista de direcciones MAC con direcciones tomadas de una variable de cadena de configuración HTML.

## <a name="syntax"></a>Sintaxis


```C++
BOOL LoadMACAddresses(
  _In_  const char   *pConfig,
  _In_  const char   *pVarName,
  _Out_       LPBYTE *ppAddresses,
  _Out_       DWORD  *pNumAddresses
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

Puntero a un puntero a una matriz de direcciones. Si se encuentra la variable especificada en *pVarName* y tiene una longitud que no es cero, la función asigna espacio suficiente (mediante **HeapAllocMemory)** y almacena todas las direcciones MAC como una matriz.

</dd> <dt>

*pNumAddresses* \[ out\]
</dt> <dd>

Puntero a la variable **DWORD** establecida en el número de direcciones MAC tomadas de la cadena de configuración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente (se encontró el nombre de la variable y tenía una cadena de longitud no cero que representaba direcciones MAC), el valor devuelto es **TRUE.**

Si la función no se realiza correctamente, el valor devuelto es **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




