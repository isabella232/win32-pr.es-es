---
description: Habilita la finalización de tareas.
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: Interfaz TaskCompletionClient
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: a823dc528ea189c70f44689ab69795eb3a430e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278490"
---
# <a name="taskcompletionclient-interface"></a>Interfaz TaskCompletionClient

Habilita la finalización de tareas.

## <a name="members"></a>Miembros

La interfaz **TaskCompletionClient** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **TaskCompletionClient** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **TaskCompletionClient** tiene estos métodos.



| Método                                                                    | Descripción                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [**ApplyTaskCompletion**](taskcompletionclient-applytaskcompletion.md)   | Comienza la finalización de la tarea.<br/> |
| [**RevokeTaskCompletion**](taskcompletionclient-revoketaskcompletion.md) | Finaliza la finalización de la tarea.<br/>   |



 

## <a name="remarks"></a>Observaciones

El GUID para esta interfaz es "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".

Esta API está en desuso y puede que no esté disponible en versiones futuras de Windows. En su lugar, las aplicaciones deben usar las API en el espacio de nombres [**Windows. ApplicationModel. ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                           |
| Archivo DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



 

 
