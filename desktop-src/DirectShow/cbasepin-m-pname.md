---
description: Nombre del pin.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: Miembro CBasePin::m_pName (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pName
api_type:
- HeaderDef
api_location:
- Amfilter.h
ms.openlocfilehash: d118ed76650b9ea580c0143ff4334a480d110c4a9d9531a23dda60c05c614630
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052685"
---
# <a name="cbasepinm_pname-member"></a>Miembro CBasePin::m \_ pName

Nombre del pin.

## <a name="syntax"></a>Sintaxis


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a>Comentarios

El [**método CBasePin::QueryPinInfo**](cbasepin-querypininfo.md) devuelve esta cadena como nombre del pin y el método [**CBasePin::QueryId**](cbasepin-queryid.md) la devuelve como identificador de pin. Sin embargo, en general, no es necesario que el nombre del pin y el identificador de pin sean iguales. El identificador de pin se usa para la persistencia del grafo. Para obtener más información, [**vea IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




