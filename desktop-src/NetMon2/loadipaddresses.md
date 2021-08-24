---
description: El monitor llama a la función LoadIPAddresses para rellenar una lista de direcciones IP con direcciones tomadas de una variable de cadena de configuración HTML.
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: Función LoadIPAddresses (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2f56517fd0caf4762be2848ac9a6f3094ed5e3194b2eb84123bf2fcc2bf67bcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742677"
---
# <a name="loadipaddresses-function"></a>Función LoadIPAddresses

El monitor llama a la función **LoadIPAddresses** para rellenar una lista de direcciones IP con direcciones tomadas de una variable de cadena de configuración HTML.

## <a name="syntax"></a>Sintaxis


```C++
BOOL LoadIPAddresses(
  _In_  const char  *pConfig,
  _In_  const char  *pVarName,
  _Out_       DWORD **ppAddresses,
  _Out_       DWORD *pNumAddresses
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

Puntero a un puntero a una matriz de direcciones. Si se encuentra la variable especificada en *pVarName* y tiene una longitud que no es cero, la función asigna espacio suficiente y almacena todas las direcciones IP como una matriz.

</dd> <dt>

*pNumAddresses* \[ out\]
</dt> <dd>

Puntero a la variable **DWORD** que se establece en el número de direcciones IP tomadas de la cadena de configuración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente (se encontró el nombre de la variable y tenía una cadena de longitud no cero que representara direcciones IP), el valor devuelto es **TRUE.**

Si la función no se realiza correctamente, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Comentarios

Las direcciones IP deben estar en formato x.x.x.x (por ejemplo, 127.0.0.1).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




