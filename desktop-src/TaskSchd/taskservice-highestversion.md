---
title: Propiedad TaskService. HighestVersion
description: En scripting, indica la versión más alta de Programador de tareas que admite un equipo.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- Programador de tareas de la propiedad HighestVersion
- Programador de tareas de la propiedad HighestVersion, objeto TaskService
- Programador de tareas de objeto TaskService, propiedad HighestVersion
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4e381326ab901fcaf8657975ce3f8401facd44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803950"
---
# <a name="taskservicehighestversion-property"></a>Propiedad TaskService. HighestVersion

En scripting, indica la versión más alta de Programador de tareas que admite un equipo.

## <a name="syntax"></a>Sintaxis


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a>Valor de propiedad

La versión más alta de Programador de tareas que admite un equipo. La versión más alta es un valor que se divide en MajorVersion/MinorVersion en el límite de 16 bits. El servicio Programador de tareas devuelve 1 para la versión principal y 2 para la versión secundaria. Utilice la función [CLng](/previous-versions//ck4c5842(v=vs.85)) para obtener el valor entero de la propiedad.

## <a name="examples"></a>Ejemplos

En el código siguiente se muestra cómo usar la función [CLng](/previous-versions//ck4c5842(v=vs.85)) para obtener el valor de la propiedad **HighestVersion** .


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

