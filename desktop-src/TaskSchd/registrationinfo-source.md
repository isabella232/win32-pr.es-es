---
title: RegistrationInfo.Source, propiedad
description: Para el scripting, obtiene o establece de dónde se originó la tarea. Por ejemplo, una tarea puede originarse en un componente, servicio, aplicación o usuario.
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Propiedades de origen Programador de tareas
- Propiedad de origen Programador de tareas , objeto RegistrationInfo
- Objeto RegistrationInfo Programador de tareas , propiedad Source
topic_type:
- apiref
api_name:
- RegistrationInfo.Source
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d360a20d1f0f4736db4dd6f136a579178a65ca70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172898"
---
# <a name="registrationinfosource-property"></a>RegistrationInfo.Source, propiedad

Para el scripting, obtiene o establece de dónde se originó la tarea. Por ejemplo, una tarea puede originarse en un componente, servicio, aplicación o usuario.

## <a name="syntax"></a>Sintaxis


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a>Valor de propiedad

Desde donde se originó la tarea. Por ejemplo, desde un componente, servicio, aplicación o usuario.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, la información de origen de la tarea se especifica mediante el [**elemento Source**](taskschedulerschema-source-registrationinfotype-element.md) del esquema Programador de tareas tarea.

Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un recurso .dll archivo. Se usa una cadena especializada para hacer referencia al texto del archivo de recursos. El formato de la cadena es $(@ Dll , ResourceID ), donde Dll es la ruta de acceso al archivo .dll que contiene el recurso y ResourceID es el identificador del texto \[ \] del \[ \] \[ \] \[ \] recurso. Por ejemplo, el establecimiento de este valor de propiedad en $(@ %SystemRoot% System32ResourceName.dll, -101) establecerá la propiedad en el valor del texto del recurso con un identificador igual a -101 en el archivo deResourceName.dll \\ \\ %SystemRoot% \\ \\ System32.

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
</dt> </dl>

 

 





