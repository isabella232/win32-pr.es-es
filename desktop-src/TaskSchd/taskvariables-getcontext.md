---
title: Método TaskVariables.GetContext
description: Para el scripting, se usa para compartir el contexto entre diferentes pasos y tareas que se encuentran en la misma instancia de trabajo.
ms.assetid: c3f1245c-531b-43f4-a3e4-8cb5deedd375
keywords:
- Método GetContext Programador de tareas
- Método GetContext Programador de tareas , objeto TaskVariables
- Objeto TaskVariables Programador de tareas , método GetContext
topic_type:
- apiref
api_name:
- TaskVariables.GetContext
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c98714d92aba0cffce9d6410ac575c35ec1b7b3e683b954015caebd7719d72b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974705"
---
# <a name="taskvariablesgetcontext-method"></a>Método TaskVariables.GetContext

Para el scripting, se usa para compartir el contexto entre diferentes pasos y tareas que se encuentran en la misma instancia de trabajo. Este método no se implementa.

## <a name="syntax"></a>Sintaxis


```VB
TaskVariables.GetContext( _
  ByRef context _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*context* \[ out\]
</dt> <dd>

Contexto que se usa para compartir el contexto entre diferentes pasos y tareas que se encuentran en la misma instancia de trabajo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TaskVariables**](taskvariables.md)
</dt> </dl>

 

 





