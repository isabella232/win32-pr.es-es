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
ms.openlocfilehash: d03e52a15e6689b7f1ea98a2f1021874cab6a8967dd148b7eaf685ff3984e8cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773655"
---
# <a name="taskcompletionclient-interface"></a>Interfaz TaskCompletionClient

Habilita la finalización de tareas.

## <a name="members"></a>Miembros

La **interfaz TaskCompletionClient** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **TaskCompletionClient también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz TaskCompletionClient** tiene estos métodos.



| Método                                                                    | Descripción                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [**ApplyTaskCompletion**](taskcompletionclient-applytaskcompletion.md)   | Comienza la finalización de la tarea.<br/> |
| [**RevokeTaskCompletion**](taskcompletionclient-revoketaskcompletion.md) | Finaliza la finalización de la tarea.<br/>   |



 

## <a name="remarks"></a>Comentarios

El GUID de esta interfaz es "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".

Esta API está en desuso y es posible que no esté disponible en versiones futuras de Windows. Las aplicaciones deben usar las API de la [**Windows. En su lugar, el espacio de nombres ApplicationModel.ExtendedExecution.**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                           |
| Archivo DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



 

 
