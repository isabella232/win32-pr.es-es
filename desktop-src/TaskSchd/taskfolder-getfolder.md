---
title: Propiedad TaskFolder. GetFolder
description: En el caso de scripting, obtiene una carpeta que contiene tareas en una ubicación especificada.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- Propiedad GetFolder Programador de tareas
- Propiedad GetFolder Programador de tareas, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, propiedad GetFolder
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
ms.openlocfilehash: 308173660ffff7d2062febd087c89cb63bcd8d99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150046"
---
# <a name="taskfoldergetfolder-property"></a>Propiedad TaskFolder. GetFolder

En el caso de scripting, obtiene una carpeta que contiene tareas en una ubicación especificada.

## <a name="syntax"></a>Sintaxis


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a>Valor de propiedad

La ruta de acceso (ubicación) de la carpeta. No use una barra diagonal inversa después del nombre de la última carpeta en la ruta de acceso. La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \) . Un ejemplo de una ruta de carpeta de tareas, en la carpeta de tareas raíz, es \\ MyTaskFolder. No se puede usar el carácter '. ' para especificar la carpeta de tareas actual y '.. ' no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.

## <a name="error-codes"></a>Códigos de error

Carpeta en la ubicación especificada. La carpeta es un objeto [**TaskFolder**](taskfolder.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





