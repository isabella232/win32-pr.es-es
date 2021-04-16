---
description: El monitor llama a la función LoadMACAddresses para rellenar una lista de direcciones MAC con las direcciones tomadas de una variable de cadena de configuración HTML.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: Función LoadMACAddresses (Netmon. h)
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
ms.openlocfilehash: 62c9422469d7acf061578d1ec093676f6e1d8386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542382"
---
# <a name="loadmacaddresses-function"></a>LoadMACAddresses función)

El monitor llama a la función **LoadMACAddresses** para rellenar una lista de direcciones MAC con las direcciones tomadas de una variable de cadena de configuración HTML.

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

*pConfig* \[ de\]
</dt> <dd>

Puntero a la cadena de configuración HTML que el método [IMonitor::D oconfigure](imonitor-doconfigure.md) pasa al monitor.

</dd> <dt>

*pVarName* \[ de\]
</dt> <dd>

Puntero al nombre de la variable en la cadena de configuración.

</dd> <dt>

*ppAddresses* \[ enuncia\]
</dt> <dd>

Puntero a un puntero a una matriz de direcciones. Si se encuentra la variable especificada en *pVarName* y tiene una longitud distinta de cero, la función asigna espacio suficiente (mediante **HeapAllocMemory**) y almacena todas las direcciones MAC como una matriz.

</dd> <dt>

*pNumAddresses* \[ enuncia\]
</dt> <dd>

Puntero a la variable **DWORD** que se establece en el número de direcciones MAC tomadas de la cadena de configuración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, se encontró el nombre de la variable y tenía una cadena que no es de longitud cero que representaba direcciones MAC), el valor devuelto es **true**.

Si la función no se realiza correctamente, el valor devuelto es **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




