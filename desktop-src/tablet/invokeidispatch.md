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
ms.openlocfilehash: e4989e3ec23a1ffa97ba317831143ecf0920ef9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467989"
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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl> |



 

 




