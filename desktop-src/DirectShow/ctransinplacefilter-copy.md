---
description: El método Copy copia un ejemplo multimedia.
ms.assetid: 3fbc6925-6e9c-4419-ab0d-0bbdbdf9bb8e
title: Método CTransInPlaceFilter.Copy (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Copy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10a7a2927789ffe49d37912862580222f0ed06d9648b6312cbb044e357d6e61c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053525"
---
# <a name="ctransinplacefiltercopy-method"></a>Método CTransInPlaceFilter.Copy

El `Copy` método copia un ejemplo multimedia.

## <a name="syntax"></a>Sintaxis


```C++
IMediaSample* Copy(
   IMediaSample *pSource
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSource* 
</dt> <dd>

Puntero a la [**interfaz IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a la **interfaz IMediaSample** del nuevo ejemplo.

## <a name="remarks"></a>Comentarios

Este método recupera un búfer vacío del asignador de bajada. Copia todas las propiedades de ejemplo de *pSource* en el nuevo ejemplo, junto con los datos reales del ejemplo. Si el filtro usa dos asignadores, llama a este método para copiar datos entre búferes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 




