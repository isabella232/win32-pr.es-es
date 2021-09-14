---
title: Propiedad Principal.DisplayName
description: Para el scripting, obtiene o establece el nombre de la entidad de seguridad.
ms.assetid: 73caf263-f597-4bea-ae89-32f9919d7a70
keywords:
- Propiedad DisplayName Programador de tareas
- Propiedad DisplayName Programador de tareas , objeto Principal
- Objeto principal Programador de tareas , propiedad DisplayName
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173042"
---
# <a name="principaldisplayname-property"></a>Propiedad Principal.DisplayName

Para el scripting, obtiene o establece el nombre de la entidad de seguridad.

## <a name="syntax"></a>Sintaxis


```VB
Principal.DisplayName As String
```



## <a name="property-value"></a>Valor de propiedad

Nombre de la entidad de seguridad.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, el nombre para mostrar de una entidad de seguridad se especifica en el [**elemento DisplayName**](taskschedulerschema-displayname-principaltype-element.md) del Programador de tareas esquema.

Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un recurso .dll archivo. Se usa una cadena especializada para hacer referencia al texto del archivo de recursos. El formato de la cadena es $(@ Dll , ResourceID ), donde Dll es la ruta de acceso al archivo .dll que contiene el recurso y ResourceID es el identificador del texto \[ \] del \[ \] \[ \] \[ \] recurso. Por ejemplo, al establecer este valor de propiedad en $(@ %SystemRoot% \\ System32ResourceName.dll, -101) se establecerá la propiedad en el valor del texto del recurso con un identificador igual a -101 en el archivo deResourceName.dll \\ %SystemRoot%. \\ \\

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**Principal**](principal.md)
</dt> </dl>

 

 





