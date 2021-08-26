---
description: El método GetCurrentPosition recupera la posición actual, en relación con la duración total de la secuencia. Este método implementa el método IMediaSeeking::GetCurrentPosition.
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: Método CPosPassThru.GetCurrentPosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a43477d019639b4e1de5c2aa40f18c99f7b902498c671f8106d5832c43b11584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084165"
---
# <a name="cpospassthrugetcurrentposition-method"></a>Método CPosPassThru.GetCurrentPosition

El `GetCurrentPosition` método recupera la posición actual, en relación con la duración total de la secuencia. Este método implementa el [**método IMediaSeeking::GetCurrentPosition.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCurrent* 
</dt> <dd>

Puntero a una variable que recibe la posición actual, en unidades del formato de hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto.<br/>                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | No se admite el método .<br/>   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Argumento de** puntero NULL.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método llama al [**método CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) para recuperar la posición más reciente. Si se produce un error **en GetMediaTime,** el método llama a **IMediaSeeking::GetCurrentPosition** en el pin conectado.

El **método GetMediaTime** produce un error de forma predeterminada en la clase base. Si el filtro almacena en caché la posición actual, invalide **GetMediaTime** para devolver el valor almacenado en caché.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 




