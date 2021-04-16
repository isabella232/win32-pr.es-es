---
description: Los monitores llaman a la función LoadTCHAR para establecer una variable de cadena en una cadena tomada de una cadena de configuración HTML.
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: Función LoadTCHAR (Netmon. h)
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
ms.openlocfilehash: 25437ae5ad6c23209540194f8c658e275c7041b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677413"
---
# <a name="loadtchar-function"></a>LoadTCHAR función)

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

*pConfig* \[ de\]
</dt> <dd>

Puntero a la cadena de configuración HTML que el método [IMonitor::D oconfigure](imonitor-doconfigure.md) pasa al monitor.

</dd> <dt>

*pVarName* \[ de\]
</dt> <dd>

Puntero al nombre de la variable en la cadena de configuración.

</dd> <dt>

*ppszString* \[ enuncia\]
</dt> <dd>

Puntero a un puntero de cadena. Si se encuentra el nombre de la variable solicitada, la cadena se asigna y se asigna a este puntero. Es responsable del usuario la liberación de la memoria asociada a la cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta (si se ha encontrado el nombre de la variable y tiene una cadena de longitud distinta de cero), el valor devuelto es **true**.

Si la función no se realiza correctamente, el valor devuelto es **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




