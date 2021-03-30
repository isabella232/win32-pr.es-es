---
title: Propiedad IResultsViewer QueryText (WdsView. h)
description: Obtiene o establece el texto de la consulta actual.
ms.assetid: 3d6b31fa-3f17-45de-a91a-f24a6b076099
keywords:
- Propiedades de QueryText características de entorno heredado de Windows
- Propiedad QueryText características de entorno heredado de Windows, interfaz IResultsViewer
- Interfaz IResultsViewer características del entorno heredado de Windows, propiedad QueryText
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
ms.openlocfilehash: 98450114ad64ec0209b14041b8f2516dc6884b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150986"
---
# <a name="iresultsviewerquerytext-property"></a>IResultsViewer:: QueryText (propiedad)

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Obtiene o establece el texto de la consulta actual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


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



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                        |
| Redistribuible<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





