---
description: La función ExpertSubmitEvent indica que existe una condición de evento y proporciona una estructura de datos que describe la condición.
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: Función ExpertSubmitEvent (Netmon.h)
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
ms.openlocfilehash: b6ce73d378e4d8432459a23a76b30ebf4d558a5f82ec230e6841eeeb621aed13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744225"
---
# <a name="expertsubmitevent-function"></a>Función ExpertSubmitEvent

La **función ExpertSubmitEvent** indica que existe una condición de evento y proporciona una estructura de datos que describe la condición.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hExpertKey* \[ En\]
</dt> <dd>

Identificador único del experto. Monitor de red pasa *hExpertKey* al experto cuando llama a la [función Run.](run.md)

</dd> <dt>

*pEiqueEvent* \[ En\]
</dt> <dd>

Puntero a una **estructura NMEVENTDATA** que describe la condición de evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto indica el motivo del error. Si el valor devuelto es NMERR EXPERT TERMINATE, el experto limpia inmediatamente \_ \_ y devuelve.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




