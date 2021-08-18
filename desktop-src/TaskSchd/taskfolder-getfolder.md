---
title: Propiedad TaskFolder.GetFolder
description: Para el scripting, obtiene una carpeta que contiene tareas en una ubicación especificada.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- Propiedad GetFolder Programador de tareas
- Propiedad GetFolder Programador de tareas , objeto TaskFolder
- Objeto TaskFolder Programador de tareas , propiedad GetFolder
topic_type:
- apiref
api_name:
- TaskFolder.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7668b2486a316fe2bf799762401459ec7da2602ff52a4d5d3dc9ddb4dd888e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758988"
---
# <a name="taskfoldergetfolder-property"></a>Propiedad TaskFolder.GetFolder

Para el scripting, obtiene una carpeta que contiene tareas en una ubicación especificada.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a>Valor de propiedad

Ruta de acceso (ubicación) a la carpeta. No use una barra diagonal inversa después del nombre de la última carpeta en la ruta de acceso. La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \\ ). Un ejemplo de una ruta de acceso de carpeta de tareas, en la carpeta de tareas raíz, \\ es MyTaskFolder. No se puede usar el carácter '.' para especificar la carpeta de tareas actual y '..'. no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.

## <a name="error-codes"></a>Códigos de error

Carpeta en la ubicación especificada. La carpeta es un [**objeto TaskFolder.**](taskfolder.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





