---
description: 'Método CRendererPosPassThru.GetMediaTime: el método GetMediaTime recupera las marcas de tiempo en el ejemplo actual.'
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Método CRendererPosPassThru.GetMediaTime (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3b8eb4bdd9426d589476265133234bdf3c2d5cfc691bfaced743cc4e75769c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084125"
---
# <a name="crendererpospassthrugetmediatime-method"></a>Método CRendererPosPassThru.GetMediaTime

El `GetMediaTime` método recupera las marcas de tiempo en el ejemplo actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStartTime* 
</dt> <dd>

Puntero a una variable que recibe la hora de inicio, en unidades del formato de hora actual.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntero a una variable que recibe la hora de finalización, en unidades del formato de hora actual. Puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                  | Descripción                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | No se admite la conversión a este formato.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | **Argumento de** puntero NULL.<br/>                  |



 

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CPosPassThru::GetMediaTime.**](cpospassthru-getmediatime.md) Los valores de marca de tiempo se convierten al formato de hora actual llamando al método [**CPosPassThru::ConvertTimeFormat.**](cpospassthru-converttimeformat.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




