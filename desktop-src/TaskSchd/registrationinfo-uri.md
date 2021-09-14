---
title: RegistrationInfo.URI, propiedad
description: Para el scripting, obtiene o establece el URI de la tarea.
ms.assetid: 49085ee4-65e1-412c-ac1c-9c0f9efe5679
keywords:
- Identificador de propiedad URI Programador de tareas
- Propiedad URI Programador de tareas , objeto RegistrationInfo
- Objeto RegistrationInfo Programador de tareas , propiedad URI
topic_type:
- apiref
api_name:
- RegistrationInfo.URI
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77598d556fdec29f41004529471c8098314a6faf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172897"
---
# <a name="registrationinfouri-property"></a>RegistrationInfo.URI, propiedad

Para el scripting, obtiene o establece el URI de la tarea.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
RegistrationInfo.URI As String
```



## <a name="property-value"></a>Valor de propiedad

URI de la tarea.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, el URI de la tarea se especifica mediante el elemento [**URI**](taskschedulerschema-uri-registrationinfotype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





