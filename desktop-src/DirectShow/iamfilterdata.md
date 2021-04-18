---
description: 'Nota: esta interfaz está en desuso.'
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Interfaz IAMFilterData (Fil \_ Data. h)
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
ms.openlocfilehash: 1ab5ea8e9c90c043c33cca4d9f8138dd7d9937ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679392"
---
# <a name="iamfilterdata-interface"></a>Interfaz IAMFilterData

> [!Note]  
> Esta interfaz está desusada. En su lugar, las nuevas aplicaciones deben usar la interfaz [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .

 

La `IAMFilterData` interfaz convierte información de filtro en datos binarios empaquetados, que se pueden almacenar en el registro. El objeto de asignador de filtros expone esta interfaz.

## <a name="members"></a>Miembros

La interfaz **IAMFilterData** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMFilterData** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAMFilterData** tiene estos métodos.



| Método                                                     | Descripción                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [**CreateFilterData**](iamfilterdata-createfilterdata.md) | Crea datos de registro binarios para un filtro.<br/>     |
| [**ParseFilterData**](iamfilterdata-parsefilterdata.md)   | Desempaqueta los datos de registro binarios para un filtro.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El encabezado Fil \_ Data. h se encuentra en el directorio de [ejemplo del asignador](mapper-sample.md) en el Windows SDK.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Fil \_ Data. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces desusadas](deprecated-interfaces.md)
</dt> </dl>

 

 
