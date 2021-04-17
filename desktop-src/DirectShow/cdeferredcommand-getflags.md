---
description: El método GetFlags recupera las marcas de contexto asociadas al comando diferido.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: CDeferredCommand. GetFlags (método) (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetFlags
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec9b97e42534d34c5033b3b86edb9c33366d639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681196"
---
# <a name="cdeferredcommandgetflags-method"></a>CDeferredCommand. GetFlags (método)

El `GetFlags` método recupera las marcas de contexto asociadas al comando diferido.

## <a name="syntax"></a>Sintaxis


```C++
short GetFlags();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve una de las siguientes opciones:



| Código devuelto                                                                                             | Descripción                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DISPATCH ( \_ método)**</dt> </dl>         | Ejecute el miembro como un método. Si una propiedad tiene el mismo nombre, se pueden establecer tanto esta marca como la de envío \_ PropertyGet (.<br/>                                               |
| <dl> <dt>**ENVIAR \_ PropertyGet (**</dt> </dl>    | El miembro se recupera como una propiedad o miembro de datos.<br/>                                                                                                         |
| <dl> <dt>**ENVIAR \_ PROPERTYPUT**</dt> </dl>    | El miembro se está cambiando como una propiedad o un miembro de datos.<br/>                                                                                                           |
| <dl> <dt>**ENVIAR \_ PROPERTYPUTREF**</dt> </dl> | El miembro se está cambiando a través de una asignación de referencia, en lugar de una asignación de valores. Esta marca solo es válida cuando la propiedad acepta una referencia a un objeto.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




