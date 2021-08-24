---
description: El método GetFlags recupera las marcas de contexto asociadas al comando diferido.
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
ms.openlocfilehash: 9c3ee5826c1b4ff81f90c86a6db4517aafc41313e53672486c41ab4847e82674
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910195"
---
# <a name="cdeferredcommandgetflags-method"></a>Método CDeferredCommand.GetFlags

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
| <dl> <dt>**DISPATCH \_ (MÉTODO)**</dt> </dl>         | Ejecute el miembro como método. Si una propiedad tiene el mismo nombre, se pueden establecer tanto este como la marca DISPATCH \_ PROPERTYGET.<br/>                                               |
| <dl> <dt>**DISPATCH \_ PROPERTYGET**</dt> </dl>    | El miembro se recupera como una propiedad o un miembro de datos.<br/>                                                                                                         |
| <dl> <dt>**DISPATCH \_ PROPERTYPUT**</dt> </dl>    | El miembro se está cambiando como una propiedad o un miembro de datos.<br/>                                                                                                           |
| <dl> <dt>**DISPATCH \_ PROPERTYPUTREF**</dt> </dl> | El miembro se cambia a través de una asignación de referencia, en lugar de una asignación de valor. Esta marca solo es válida cuando la propiedad acepta una referencia a un objeto .<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDeferredCommand (clase)**](cdeferredcommand.md)
</dt> </dl>

 

 




