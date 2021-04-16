---
title: Elemento WorkingDirectory (execType)
description: Especifica el directorio donde existe el archivo ejecutable o los archivos utilizados por el archivo ejecutable.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- Programador de tareas del elemento WorkingDirectory
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8c382d0e60b16d85fbc86f7579a0e700d3dd30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686220"
---
# <a name="workingdirectory-exectype-element"></a>Elemento WorkingDirectory (execType)

Especifica el directorio donde existe el archivo ejecutable o los archivos utilizados por el archivo ejecutable.

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

El elemento **WorkingDirectory** se define mediante el tipo complejo de [**execType**](taskschedulerschema-exectype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                      | Derivado de                                                 | Descripción                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Ejec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Especifica una acción que ejecuta una operación de línea de comandos.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripts, el directorio de trabajo se especifica mediante la propiedad [**ExecAction. WorkingDirectory**](execaction-workingdirectory.md) .

En el desarrollo de C++, el directorio de trabajo se especifica mediante la propiedad [**IExecAction:: WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) .

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define una acción de ejecución.


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





