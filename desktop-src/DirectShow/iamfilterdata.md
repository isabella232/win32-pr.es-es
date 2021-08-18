---
description: Obtenga información sobre la interfaz IAMFilterData, que convierte la información de filtro en datos binarios empaquetados. Esta interfaz está desusada.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Interfaz IAMFilterData (Fil \_ data.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData
api_type:
- COM
api_location:
- fil_data.h
ms.openlocfilehash: 9174549c93a76f94ccb7f039343a8eab5e75ece252871d11d60221df03aabe87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823605"
---
# <a name="iamfilterdata-interface"></a>Interfaz IAMFilterData

> [!Note]  
> Esta interfaz está desusada. Las nuevas aplicaciones deben usar la [**interfaz IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) en su lugar.

 

La `IAMFilterData` interfaz convierte la información de filtro en datos binarios empaquetados, que se pueden almacenar en el Registro. El objeto Filter Mapper expone esta interfaz.

## <a name="members"></a>Miembros

La **interfaz IAMFilterData** hereda de [**la interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMFilterData** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMFilterData** tiene estos métodos.



| Método                                                     | Descripción                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [**CreateFilterData**](iamfilterdata-createfilterdata.md) | Crea datos binarios del Registro para un filtro.<br/>     |
| [**ParseFilterData**](iamfilterdata-parsefilterdata.md)   | Desempaquete los datos binarios del Registro para un filtro.<br/> |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> El encabezado Fil \_ data.h se encuentra en el directorio [Mapper Sample (Ejemplo](mapper-sample.md) del asignador) en Windows SDK.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Fil \_ data.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces en desuso](deprecated-interfaces.md)
</dt> </dl>

 

 
