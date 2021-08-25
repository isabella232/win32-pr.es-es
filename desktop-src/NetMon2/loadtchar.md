---
description: Los monitores llaman a la función LoadTCHAR para establecer una variable de cadena en una cadena tomada de una cadena de configuración HTML.
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: Función LoadTCHAR (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadTCHAR
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2d85419485e2442f82c94948b832914fa30e44396f266eed10cd1545b4cc28ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890291"
---
# <a name="loadtchar-function"></a>Función LoadTCHAR

Los monitores llaman a la función **LoadTCHAR** para establecer una variable de cadena en una cadena tomada de una cadena de configuración HTML.

## <a name="syntax"></a>Sintaxis


```C++
BOOL LoadTCHAR(
  _In_  const char *pConfig,
  _In_  const char *pVarName,
  _Out_       char **ppszString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pConfig* \[ En\]
</dt> <dd>

Puntero a la cadena de configuración HTML que el método [IMonitor::D oConfigure](imonitor-doconfigure.md) pasa al monitor.

</dd> <dt>

*pVarName* \[ En\]
</dt> <dd>

Puntero al nombre de la variable en la cadena de configuración.

</dd> <dt>

*ppszString* \[ out\]
</dt> <dd>

Puntero a un puntero de cadena. Si se encuentra el nombre de variable solicitado, la cadena se asigna a este puntero. Es responsabilidad del usuario liberar la memoria asociada a la cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente (si se encontró el nombre de la variable y tenía una cadena de longitud no cero), el valor devuelto es **TRUE.**

Si la función no se realiza correctamente, el valor devuelto es **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




