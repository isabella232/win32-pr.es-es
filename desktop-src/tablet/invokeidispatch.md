---
description: Invoca la funcionalidad del asistente para la interfaz IDispatch.
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: Función InvokeIDispatch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InvokeIDispatch
api_type:
- LibDef
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 9708ebc5675d918c959be132d16037ac4e128650280b8243dcfe5c48834b602b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041875"
---
# <a name="invokeidispatch-function"></a>Función InvokeIDispatch

Invoca la funcionalidad del asistente para la interfaz IDispatch.

Esta función no está pensada para que la utilice el código de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI InvokeIDispatch(
        IDispatch  *pDispatch,
        DISPID     dispid,
        DISPPARAMS *pDisp,
  _Out_ VARIANT    *pVarResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDispatch* 
</dt> <dd>

Instancia de la interfaz IDispatch.

</dd> <dt>

*desaconsulte* 
</dt> <dd>

Método, propiedad o argumento que se pasa.

</dd> <dt>

*pDisp* 
</dt> <dd>

Parámetros que se pasan.

</dd> <dt>

*pVarResult* \[ out\]
</dt> <dd>

Estructura que recibe los valores recuperados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. Si se produce un error, los posibles códigos de retorno incluyen, entre otros, los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                                  | Descripción                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El valor de *pDispatch* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl> |



 

 




