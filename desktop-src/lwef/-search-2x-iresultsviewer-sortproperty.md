---
title: Propiedad SortProperty de IResultsViewer (WdsView.h)
description: Esta propiedad establecerá o devolverá la indexcolumna de la propiedad por la que ordenar los resultados.
ms.assetid: 5b117f2e-52cc-43ef-9ebd-d7a800015465
keywords:
- Características heredadas del entorno de Windows propiedad SortProperty
- Propiedad SortProperty Legacy Windows Environment Features , IResultsViewer (interfaz)
- IResultsViewer interface Legacy Windows Environment Features , SortProperty property
topic_type:
- apiref
api_name:
- IResultsViewer.SortProperty
- IResultsViewer.get_SortProperty
- IResultsViewer.put_SortProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99ab912dde6bdc87b2e9d05496f25de497b6fdc9c8fde4e65e3d2cb89549b1e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610935"
---
# <a name="iresultsviewersortproperty-property"></a>IResultsViewer::SortProperty, propiedad

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Esta propiedad establecerá o devolverá la indexcolumna de la propiedad por la que ordenar los resultados.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SortProperty(
  [in]          BSTR column
);

HRESULT get_SortProperty(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Valor de propiedad

Establece la propiedad IndexColumn.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/>                        |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





