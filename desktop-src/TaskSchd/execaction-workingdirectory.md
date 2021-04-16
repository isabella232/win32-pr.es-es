---
title: Propiedad ExecAction. WorkingDirectory
description: En el caso de scripting, obtiene o establece el directorio que contiene el archivo ejecutable o los archivos utilizados por el archivo ejecutable.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- Programador de tareas de la propiedad WorkingDirectory
- Programador de tareas de la propiedad WorkingDirectory, objeto ExecAction
- Programador de tareas de objeto ExecAction, propiedad WorkingDirectory
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d4755b6f760ed1af75c676ecb70074c3ea7c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676685"
---
# <a name="execactionworkingdirectory-property"></a>Propiedad ExecAction. WorkingDirectory

En el caso de scripting, obtiene o establece el directorio que contiene el archivo ejecutable o los archivos utilizados por el archivo ejecutable.

## <a name="syntax"></a>Sintaxis


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a>Valor de propiedad

El directorio que contiene el archivo ejecutable o los archivos utilizados por el archivo ejecutable.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML, el directorio de trabajo de la aplicación se especifica en el elemento [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) del esquema de programador de tareas.

La ruta de acceso se comprueba para asegurarse de que es válida cuando se registra la tarea, no cuando se establece esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





