---
title: Propiedad RegistrationInfo. URI
description: En el caso de scripting, obtiene o establece el URI de la tarea.
ms.assetid: 49085ee4-65e1-412c-ac1c-9c0f9efe5679
keywords:
- Propiedad URI Programador de tareas
- Propiedad URI Programador de tareas, objeto RegistrationInfo
- Programador de tareas de objeto RegistrationInfo, propiedad URI
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534881"
---
# <a name="registrationinfouri-property"></a>Propiedad RegistrationInfo. URI

En el caso de scripting, obtiene o establece el URI de la tarea.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
RegistrationInfo.URI As String
```



## <a name="property-value"></a>Valor de propiedad

El URI de la tarea.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, el URI de la tarea se especifica mediante el elemento [**URI**](taskschedulerschema-uri-registrationinfotype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





