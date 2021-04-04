---
title: Propiedad principal. DisplayName
description: En el caso de scripting, obtiene o establece el nombre de la entidad de seguridad.
ms.assetid: 73caf263-f597-4bea-ae89-32f9919d7a70
keywords:
- Propiedad DisplayName Programador de tareas
- Propiedad DisplayName Programador de tareas, objeto principal
- Objeto de entidad de seguridad Programador de tareas, DisplayName (propiedad)
topic_type:
- apiref
api_name:
- Principal.DisplayName
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31a76ec9473bccb20ec484259ab8adfe26ad6441
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802557"
---
# <a name="principaldisplayname-property"></a>Propiedad principal. DisplayName

En el caso de scripting, obtiene o establece el nombre de la entidad de seguridad.

## <a name="syntax"></a>Sintaxis


```VB
Principal.DisplayName As String
```



## <a name="property-value"></a>Valor de propiedad

Nombre de la entidad de seguridad.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, el nombre para mostrar de una entidad de seguridad se especifica en el elemento [**displayName**](taskschedulerschema-displayname-principaltype-element.md) del esquema de programador de tareas.

Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un archivo resource. dll. Una cadena especializada se usa para hacer referencia al texto del archivo de recursos. El formato de la cadena es $ (@ \[ dll \] , \[ resourceId \] ), donde \[ dll \] es la ruta de acceso al archivo. dll que contiene el recurso y \[ resourceId \] es el identificador del texto del recurso. Por ejemplo, si se establece el valor de esta propiedad en $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101), la propiedad se establecerá en el valor del texto del recurso con un identificador igual a-101 en el archivo% SystemRoot% \\ system32 \\ResourceName.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**Principal**](principal.md)
</dt> </dl>

 

 





