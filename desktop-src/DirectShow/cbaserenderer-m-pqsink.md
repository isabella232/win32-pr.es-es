---
description: Puntero al objeto que recibe mensajes de control de calidad.
ms.assetid: bf4fd84c-9522-4686-9fb1-17a2ce3e5a16
title: CBaseRenderer::m_pQSink miembro (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pQSink
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bb365c0af23868f05c624144de239828ce7c1d6cabacd3bf774c59d566348ff5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502725"
---
# <a name="cbaserendererm_pqsink-member"></a>Miembro CBaseRenderer::m \_ pQSink

Puntero al objeto que recibe mensajes de control de calidad.

## <a name="syntax"></a>Sintaxis


```C++
IQualityControl *m_pQSink;
```



## <a name="remarks"></a>Comentarios

La clase base no implementa el control de calidad. El valor predeterminado de esta variable miembro **es NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




