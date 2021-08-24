---
description: El monitor llama a la función LoadDWORD para establecer una variable DWORD con un valor tomado de una variable de cadena de configuración HTML.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: Función LoadDWORD (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8fa0477122548dad30911948a3581d269b22d8d6eb866273f32aa40a9b427545
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778765"
---
# <a name="loaddword-function"></a>Función LoadDWORD

El monitor llama a la función **LoadDWORD** para establecer una variable **DWORD** con un valor tomado de una variable de cadena de configuración HTML.

## <a name="syntax"></a>Sintaxis


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
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

*pValue* \[ En\]
</dt> <dd>

Puntero a la variable **DWORD** establecida en el valor de la variable de cadena de configuración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta (si se encontró el nombre de la variable y tenía una cadena de longitud no cero), se inserta **DWORD** y el valor devuelto es **TRUE.**

Si la función no se realiza correctamente, el valor devuelto es **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




