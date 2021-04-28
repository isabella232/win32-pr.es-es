---
description: 'Método CSourceSeeking.SetPositions: el método SetPositions establece la posición actual y la posición de detenerse. Este método implementa el método IMediaSeeking::SetPositions.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Método CSourceSeeking.SetPositions (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b09dd92b97166b8d973328ec95e466abbda116bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085173"
---
# <a name="csourceseekingsetpositions-method"></a>Método CSourceSeeking.SetPositions

El `SetPositions` método establece la posición actual y la posición de detenerse. Este método implementa el [**método IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCurrent* 
</dt> <dd>

Puntero a una variable que especifica la posición actual.

</dd> <dt>

*CurrentFlags* 
</dt> <dd>

Combinación bit a bit de marcas. Vea la sección Comentarios.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntero a una variable que especifica la hora de detenerse, en unidades del formato de hora actual.

</dd> <dt>

*StopFlags* 
</dt> <dd>

Combinación bit a bit de marcas. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                  | Descripción                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Marcas no válidas<br/>             |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | **Argumento de** puntero NULL<br/> |



 

## <a name="remarks"></a>Comentarios

Se admiten las marcas siguientes:

-   NoPositioning de AM \_ SEEKING \_
-   AM \_ SEEKING \_ AbsolutePositioning
-   AM \_ SEEKING \_ RelativePositioning
-   AM \_ SEEKING \_ IncrementalPositioning *(solo pStop)*

Para obtener más información, [**vea IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

Este método actualiza los valores de las variables miembro [**CSourceSeeking::m \_ rtStart**](csourceseeking-m-rtstart.md) y [**CSourceSeeking::m \_ rtStop**](csourceseeking-m-rtstop.md) y, a continuación, llama a los métodos virtuales puros [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) y [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 




