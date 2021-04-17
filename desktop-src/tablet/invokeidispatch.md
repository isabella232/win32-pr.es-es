---
description: Invoca la funcionalidad auxiliar para la interfaz IDispatch.
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: InvokeIDispatch función)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706573"
---
# <a name="invokeidispatch-function"></a>InvokeIDispatch función)

Invoca la funcionalidad auxiliar para la interfaz IDispatch.

Esta función no está pensada para ser utilizada por el código de la aplicación.

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

*DISPID* 
</dt> <dd>

Método, propiedad o argumento que se va a pasar.

</dd> <dt>

*pDisp* 
</dt> <dd>

Parámetros que se van a pasar.

</dd> <dt>

*pVarResult* \[ enuncia\]
</dt> <dd>

Estructura que recibe los valores recuperados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error, los códigos de retorno posibles incluyen, entre otros, los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                                  | Descripción                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El valor de *pDispatch* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl> |



 

 




