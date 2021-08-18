---
title: Propiedad QueryText de IResultsViewer (WdsView.h)
description: Obtiene o establece el texto de la consulta actual.
ms.assetid: 3d6b31fa-3f17-45de-a91a-f24a6b076099
keywords:
- Características heredadas del entorno de Windows querytext
- Propiedades queryText heredadas Windows environment features , IResultsViewer (interfaz)
- IResultsViewer interface Legacy Windows Environment Features , QueryText property
topic_type:
- apiref
api_name:
- IResultsViewer.QueryText
- IResultsViewer.get_QueryText
- IResultsViewer.put_QueryText
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5522419d14bf27a1e836c9caa16e9dabf5a122e4566fd19c868a1f72e3f61d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753590"
---
# <a name="iresultsviewerquerytext-property"></a>Propiedad IResultsViewer::QueryText

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la API [Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Obtiene o establece el texto de la consulta actual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_QueryText(
  [in]          BSTR query
);

HRESULT get_QueryText(
  [out, retval] BSTR *query
);
```



## <a name="property-value"></a>Valor de propiedad

Establece el texto de la consulta actual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio sp1 \[\]<br/>                        |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





