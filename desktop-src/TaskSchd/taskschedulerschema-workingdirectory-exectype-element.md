---
title: Elemento WorkingDirectory (execType)
description: Especifica el directorio donde existe el archivo ejecutable o los archivos utilizados por el ejecutable.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- Elemento WorkingDirectory Programador de tareas
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5a91908d5cd774f19f32a182934688dc899179d1abba967b7871a646efcfe042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513747"
---
# <a name="workingdirectory-exectype-element"></a>Elemento WorkingDirectory (execType)

Especifica el directorio donde existe el archivo ejecutable o los archivos utilizados por el ejecutable.

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

El tipo complejo [**execType**](taskschedulerschema-exectype-complextype.md) define el elemento **WorkingDirectory.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                      | Derivado de                                                 | Descripción                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Especifica una acción que ejecuta una operación de línea de comandos.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de scripts, la propiedad [**ExecAction.WorkingDirectory**](execaction-workingdirectory.md) especifica el directorio de trabajo.

Para el desarrollo de C++, la propiedad [**IExecAction::WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) especifica el directorio de trabajo.

## <a name="examples"></a>Ejemplos

El código XML siguiente define una acción de ejecución.


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





