---
title: Propiedad SortProperty de IResultsViewer (WdsView. h)
description: Esta propiedad establece o devuelve el IndexColumn de la propiedad por la que se van a ordenar los resultados.
ms.assetid: 5b117f2e-52cc-43ef-9ebd-d7a800015465
keywords:
- Propiedad SortProperty características del entorno heredado de Windows
- Propiedad SortProperty características del entorno heredado de Windows, interfaz IResultsViewer
- Interfaz IResultsViewer características del entorno heredado de Windows, propiedad SortProperty
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
ms.openlocfilehash: 2cb75b98f1f0a726ef0d61b5c476df1485ba7189
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905210"
---
# <a name="iresultsviewersortproperty-property"></a>IResultsViewer:: SortProperty (propiedad)

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Esta propiedad establece o devuelve el IndexColumn de la propiedad por la que se van a ordenar los resultados.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


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



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                        |
| Redistribuible<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





