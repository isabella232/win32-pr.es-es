---
title: Propiedad IResultsViewer HeaderStyle (WdsView.h)
description: Estilo de encabezado que se muestra en la vista.
ms.assetid: 092a2ff2-eb88-4347-a81c-6a8005971ca9
keywords:
- Características heredadas del entorno de Windows HeaderStyle
- Propiedad HeaderStyle Legacy Windows Environment Features , IResultsViewer (interfaz)
- IResultsViewer interface Legacy Windows Environment Features , HeaderStyle property
topic_type:
- apiref
api_name:
- IResultsViewer.HeaderStyle
- IResultsViewer.get_HeaderStyle
- IResultsViewer.put_HeaderStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7c60687c3d306c3f9c3fcbb551f2d746723c7223b1964d42386464729b4069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753896"
---
# <a name="iresultsviewerheaderstyle-property"></a>IResultsViewer::HeaderStyle, propiedad

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Estilo de encabezado que se muestra en la vista.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HeaderStyle(
  [in]          HeaderDisplayStyle style
);

HRESULT get_HeaderStyle(
  [out, retval] HeaderDisplayStyle *style
);
```



## <a name="property-value"></a>Valor de propiedad

Establece el estilo del encabezado mostrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/>                        |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





