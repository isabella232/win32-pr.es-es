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
ms.openlocfilehash: b9c5a1b5d5ced7a9f3985ceebdd2bdcb8e491d2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084863"
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
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




