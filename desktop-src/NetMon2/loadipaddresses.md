---
description: El monitor llama a la función LoadIPAddresses para rellenar una lista de direcciones IP con las direcciones tomadas de una variable de cadena de configuración HTML.
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: Función LoadIPAddresses (Netmon. h)
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
ms.openlocfilehash: 4a5c172117081777b2a89b875401ec0645dd643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678575"
---
# <a name="loadipaddresses-function"></a>LoadIPAddresses función)

El monitor llama a la función **LoadIPAddresses** para rellenar una lista de direcciones IP con las direcciones tomadas de una variable de cadena de configuración HTML.

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

Puntero a un puntero a una matriz de direcciones. Si se encuentra la variable especificada en *pVarName* y tiene una longitud distinta de cero, la función asigna espacio suficiente y almacena todas las direcciones IP como una matriz.

</dd> <dt>

*pNumAddresses* \[ enuncia\]
</dt> <dd>

Puntero a la variable **DWORD** que se establece en el número de direcciones IP tomadas de la cadena de configuración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta (se encontró el nombre de la variable y tenía una cadena que no es de longitud cero que representaba direcciones IP), el valor devuelto es **true**.

Si la función no se realiza correctamente, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

Las direcciones IP deben estar en formato x.x.x. x (por ejemplo, 127.0.0.1).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




