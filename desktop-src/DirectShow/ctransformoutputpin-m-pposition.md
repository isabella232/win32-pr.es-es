---
description: Objeto auxiliar para pasar comandos de búsqueda ascendentes.
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: 'Miembro CTransformOutputPin:: m_pPosition (Transfrm. h)'
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
ms.openlocfilehash: dc98e439d7f6a2d6c6392ffb665b04e502047eb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661004"
---
# <a name="ctransformoutputpinm_pposition-member"></a>Miembro pPosition CTransformOutputPin:: m \_

Objeto auxiliar para pasar comandos de búsqueda ascendentes.

## <a name="syntax"></a>Sintaxis


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a>Observaciones

Cuando el PIN se consulta por primera vez para la interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) o [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , crea y agrega un objeto auxiliar [**CPosPassThru**](cpospassthru.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




