---
description: El monitor llama a la función LoadDWORD para establecer una variable DWORD con un valor tomado de una variable de cadena de configuración HTML.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: Función LoadDWORD (Netmon. h)
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
ms.openlocfilehash: 1c66566090e38fc936a5616c8782284ad795df29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678457"
---
# <a name="loaddword-function"></a>LoadDWORD función)

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

*pConfig* \[ de\]
</dt> <dd>

Puntero a la cadena de configuración HTML que el método [IMonitor::D oconfigure](imonitor-doconfigure.md) pasa al monitor.

</dd> <dt>

*pVarName* \[ de\]
</dt> <dd>

Puntero al nombre de la variable en la cadena de configuración.

</dd> <dt>

*pValue* \[ de\]
</dt> <dd>

Puntero a la variable **DWORD** que se establece en el valor de la variable de cadena de configuración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta (si se ha encontrado el nombre de la variable y tiene una cadena de longitud distinta de cero), se inserta el valor **DWORD** y el valor devuelto es **true**.

Si la función no se realiza correctamente, el valor devuelto es **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




