---
title: Propiedad IResultsViewer PreviewStyle (WdsView. h)
description: Controla el modo de presentación del panel de vista previa.
ms.assetid: 750664ea-506a-4219-ade5-1c7f1ffbd0d7
keywords:
- Propiedad PreviewStyle características de entorno heredado de Windows
- Propiedad PreviewStyle características de entorno heredado de Windows, interfaz IResultsViewer
- Interfaz IResultsViewer características del entorno heredado de Windows, propiedad PreviewStyle
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
ms.openlocfilehash: 9eb3cb2cfd94d5cf1e93080259257bb27fa4f086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714541"
---
# <a name="iresultsviewerpreviewstyle-property"></a>IResultsViewer::P propiedad reviewStyle

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Controla el modo de presentación del panel de vista previa.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


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



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                        |
| Redistribuible<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





