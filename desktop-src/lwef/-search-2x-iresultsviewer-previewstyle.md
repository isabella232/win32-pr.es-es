---
title: Propiedad IResultsViewer PreviewStyle (WdsView.h)
description: Controla el modo de presentación del panel de vista previa.
ms.assetid: 750664ea-506a-4219-ade5-1c7f1ffbd0d7
keywords:
- PreviewStyle, propiedad Legacy Windows Environment Features
- PreviewStyle, propiedad Legacy Windows Environment Features , IResultsViewer (Interfaz IResultsViewer)
- IResultsViewer interface Legacy Windows Environment Features , PreviewStyle property
topic_type:
- apiref
api_name:
- IResultsViewer.PreviewStyle
- IResultsViewer.get_PreviewStyle
- IResultsViewer.put_PreviewStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b412c92ca82263481b83ce739d44f21c2d15d99e9e6e7c74502480e0d8fad1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753787"
---
# <a name="iresultsviewerpreviewstyle-property"></a>Propiedad IResultsViewer::P reviewStyle

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la API [Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Controla el modo de presentación del panel de vista previa.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PreviewStyle(
  [in]          PreviewDisplayStyle style
);

HRESULT get_PreviewStyle(
  [out, retval] PreviewDisplayStyle *style
);
```



## <a name="property-value"></a>Valor de propiedad

Establece la propiedad de estilo actual para el panel de vista previa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio sp1 \[\]<br/>                        |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





