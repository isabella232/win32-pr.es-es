---
description: 'CTransformOutputPin::m_pPosition miembro: objeto auxiliar para pasar comandos seek ascendentes.'
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: CTransformOutputPin::m_pPosition miembro (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bfa565d38fa982ea457da13ee9cf08a1d0f2fe8d5ba52ef3c5b86379fc02b509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538165"
---
# <a name="ctransformoutputpinm_pposition-member"></a>Miembro CTransformOutputPin::m \_ pPosition

Objeto auxiliar para pasar comandos seek ascendentes.

## <a name="syntax"></a>Sintaxis


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a>Comentarios

Cuando el pin se consulta por primera vez para la interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) o [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) crea y agrega un objeto auxiliar [**CPosPassThru.**](cpospassthru.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




