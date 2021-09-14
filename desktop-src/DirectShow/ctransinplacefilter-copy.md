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
ms.openlocfilehash: 3063427611cd3a5aae74fecf6be273c07fdb917c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255302"
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

## <a name="remarks"></a>Observaciones

Este método recupera un búfer vacío del asignador de nivel inferior. Copia todas las propiedades de ejemplo de *pSource* en el nuevo ejemplo, junto con los datos reales del ejemplo. Si el filtro usa dos asignadores, llama a este método para copiar datos entre búferes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 




