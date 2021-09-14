---
description: El método GetFlags recupera las marcas de contexto asociadas al comando aplazado.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: Método CDeferredCommand.GetFlags (Ctlutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061313"
---
# <a name="cdeferredcommandgetflags-method"></a>Método CDeferredCommand.GetFlags

El `GetFlags` método recupera las marcas de contexto asociadas al comando aplazado.

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
| <dl> <dt>**DISPATCH \_ (MÉTODO)**</dt> </dl>         | Ejecute el miembro como un método. Si una propiedad tiene el mismo nombre, se pueden establecer tanto esta como la marca DISPATCH \_ PROPERTYGET.<br/>                                               |
| <dl> <dt>**DISPATCH \_ PROPERTYGET**</dt> </dl>    | El miembro se recupera como una propiedad o un miembro de datos.<br/>                                                                                                         |
| <dl> <dt>**DISPATCH \_ PROPERTYPUT**</dt> </dl>    | El miembro se está cambiando como una propiedad o un miembro de datos.<br/>                                                                                                           |
| <dl> <dt>**DISPATCH \_ PROPERTYPUTREF**</dt> </dl> | El miembro se cambia a través de una asignación de referencia, en lugar de una asignación de valor. Esta marca solo es válida cuando la propiedad acepta una referencia a un objeto .<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDeferredCommand (clase)**](cdeferredcommand.md)
</dt> </dl>

 

 




