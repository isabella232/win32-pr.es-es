---
description: Nombre del pin.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: CBasePin::m_pName miembro (Amfilter.h)
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
ms.openlocfilehash: f2580b9aba379362c39e3d792504434fa18fe076
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973960"
---
# <a name="cbasepinm_pname-member"></a>Miembro PName de CBasePin::m \_

Nombre del pin.

## <a name="syntax"></a>Sintaxis


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a>Observaciones

El [**método CBasePin::QueryPinInfo**](cbasepin-querypininfo.md) devuelve esta cadena como nombre de pin y el método [**CBasePin::QueryId**](cbasepin-queryid.md) la devuelve como identificador de pin. En general, sin embargo, no es necesario que el nombre del pin y el identificador de pin sean iguales. El identificador de pin se usa para la persistencia del grafo. Para obtener más información, [**vea IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




