---
description: 'El método SetPositions establece la posición actual y la posición de detención. Este método implementa el método IMediaSeeking:: SetPositions.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Método CSourceSeeking. SetPositions (Ctlutil. h)
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
ms.openlocfilehash: 342ca7d85fe9358b914709b7887216b62e03521d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660640"
---
# <a name="csourceseekingsetpositions-method"></a>CSourceSeeking. SetPositions, método

El `SetPositions` método establece la posición actual y la posición de detención. Este método implementa el método [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

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

Puntero a una variable que especifica la hora de detención, en unidades del formato de hora actual.

</dd> <dt>

*StopFlags* 
</dt> <dd>

Combinación bit a bit de marcas. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                                  | Descripción                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Marcas no válidas<br/>             |
| <dl> <dt>**\_puntero E**</dt> </dl>    | Argumento de puntero **nulo**<br/> |



 

## <a name="remarks"></a>Observaciones

Se admiten las marcas siguientes:

-   \_Busca \_ nopositioning
-   \_Búsqueda de \_ AbsolutePositioning
-   \_Búsqueda de \_ RelativePositioning
-   AM \_ Buscar \_ IncrementalPositioning (solo *pStop* )

Para obtener más información, vea [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

Este método actualiza los valores de las variables de miembro [**CSourceSeeking:: m \_ RtStart**](csourceseeking-m-rtstart.md) y [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) y, a continuación, llama a los métodos virtuales puros [**CSourceSeeking:: cambie las**](csourceseeking-changestart.md) y [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




