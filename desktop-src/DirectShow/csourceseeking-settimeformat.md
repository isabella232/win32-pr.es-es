---
description: 'Método CSourceSeeking.SetTimeFormat: el método SetTimeFormat establece el formato de hora. Este método implementa el método IMediaSeeking::SetTimeFormat.'
ms.assetid: dbc7c950-8cc2-4f8e-adfa-8f5cdc1b56c7
title: Método CSourceSeeking.SetTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4fc3e4fef02b5ed2a0d531c48d9503d4703d16e4353f46ff5b233bc12ebab16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526125"
---
# <a name="csourceseekingsettimeformat-method"></a>Método CSourceSeeking.SetTimeFormat

El `SetTimeFormat` método establece el formato de hora. Este método implementa el [**método IMediaSeeking::SetTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntero a un GUID de formato de hora. Consulte [**GUID de formato de hora.**](time-format-guids.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.



| Código devuelto                                                                                  | Descripción                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | No se admite el formato especificado.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | **Argumento de** puntero NULL.<br/>         |



 

## <a name="remarks"></a>Comentarios

El único formato de hora admitido por la clase base es TIME \_ FORMAT \_ MEDIA TIME \_ (unidades de 100 nanosegundos).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 




