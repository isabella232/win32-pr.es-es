---
description: La función ExpertSubmitEvent indica que existe una condición de evento y proporciona una estructura de datos que describe la condición.
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: Función ExpertSubmitEvent (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertSubmitEvent
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 448d77e9cb009b8aced0aba752526dc08b503066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360151"
---
# <a name="expertsubmitevent-function"></a>ExpertSubmitEvent función)

La función **ExpertSubmitEvent** indica que existe una condición de evento y proporciona una estructura de datos que describe la condición.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hExpertKey* \[ de\]
</dt> <dd>

Identificador único del experto. Monitor de red pasa *hExpertKey* al experto cuando llama a la función [Run](run.md) .

</dd> <dt>

*pExpertEvent* \[ de\]
</dt> <dd>

Puntero a una estructura **NMEVENTDATA** que describe la condición del evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no se realiza correctamente, el valor devuelto indica la razón del error. Si el valor devuelto es NMERR \_ Expert \_ Terminate, el experto limpia y devuelve inmediatamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




