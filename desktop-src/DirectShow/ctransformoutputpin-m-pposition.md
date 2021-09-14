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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255350"
---
# <a name="ctransformoutputpinm_pposition-member"></a>Miembro CTransformOutputPin::m \_ pPosition

Objeto auxiliar para pasar comandos seek ascendentes.

## <a name="syntax"></a>Sintaxis


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a>Observaciones

Cuando el pin se consulta por primera vez para la interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) o [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) crea y agrega un objeto auxiliar [**CPosPassThru.**](cpospassthru.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




