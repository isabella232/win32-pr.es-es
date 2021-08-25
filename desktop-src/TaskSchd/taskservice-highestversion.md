---
title: Propiedad TaskService.HighestVersion
description: Para el scripting, indica la versión más alta de Programador de tareas que admite un equipo.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- Propiedad HighestVersion Programador de tareas
- Propiedad HighestVersion Programador de tareas , objeto TaskService
- Objeto TaskService Programador de tareas propiedad , HighestVersion
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
ms.openlocfilehash: e27618490fcf404936532d272402bebc03d94eb72ba8156e897f344b708d90ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959495"
---
# <a name="taskservicehighestversion-property"></a>Propiedad TaskService.HighestVersion

Para el scripting, indica la versión más alta de Programador de tareas que admite un equipo.

## <a name="syntax"></a>Syntax


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a>Valor de propiedad

La versión más alta de Programador de tareas que admite un equipo. La versión más alta es un valor que se divide en MajorVersion/MinorVersion en el límite de 16 bits. El Programador de tareas servicio devuelve 1 para la versión principal y 2 para la versión secundaria. Use la [función CLng](/previous-versions//ck4c5842(v=vs.85)) para obtener el valor entero de la propiedad .

## <a name="examples"></a>Ejemplos

En el código siguiente se muestra cómo usar [la función CLng](/previous-versions//ck4c5842(v=vs.85)) para obtener el valor de la **propiedad HighestVersion.**


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



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

