---
description: Nombre del PIN.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: 'Miembro CBasePin:: m_pName (Amfilter. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661067"
---
# <a name="cbasepinm_pname-member"></a>Miembro pName CBasePin:: m \_

Nombre del PIN.

## <a name="syntax"></a>Sintaxis


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a>Observaciones

El método [**CBasePin:: QueryPinInfo**](cbasepin-querypininfo.md) devuelve esta cadena como el nombre del PIN y el método [**CBasePin:: queryId**](cbasepin-queryid.md) la devuelve como identificador de PIN. Sin embargo, en general, el nombre del PIN y el identificador del PIN no deben ser iguales. El identificador del PIN se usa para la persistencia del gráfico. Para obtener más información, vea [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




