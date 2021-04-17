---
title: Propiedad IResultsViewer ItemStore (WdsView. h)
description: Esta propiedad establece o devuelve el nombre del almacén en el que se van a filtrar los resultados.
ms.assetid: c2a60485-c8f7-4951-a75e-2e6f6dcc2e4f
keywords:
- Propiedad ItemStore características de entorno heredado de Windows
- Propiedad ItemStore características de entorno heredado de Windows, interfaz IResultsViewer
- Interfaz IResultsViewer características del entorno heredado de Windows, propiedad ItemStore
topic_type:
- apiref
api_name:
- IResultsViewer.ItemStore
- IResultsViewer.get_ItemStore
- IResultsViewer.put_ItemStore
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99abd4ef7ee36a0c76efa391d98a9fdb1d75f34e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490397"
---
# <a name="iresultsvieweritemstore-property"></a>IResultsViewer:: ItemStore (propiedad)

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Esta propiedad establece o devuelve el nombre del almacén en el que se van a filtrar los resultados.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_ItemStore(
  [in]          BSTR name
);

HRESULT get_ItemStore(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valor de propiedad

Establece los nombres del almacén.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                        |
| Redistribuible<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





