---
title: Propiedad IResultsViewer SortOrderProperty (WdsView.h)
description: Esta propiedad establecerá o devolverá el orden de las columnas por las que ordenar los resultados.
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- Características heredadas del entorno de Windows sortOrderProperty
- Propiedades SortOrderProperty Heredadas Windows Environment Features , IResultsViewer (interfaz)
- IResultsViewer interface Legacy Windows Environment Features , SortOrderProperty property
topic_type:
- apiref
api_name:
- IResultsViewer.SortOrderProperty
- IResultsViewer.get_SortOrderProperty
- IResultsViewer.put_SortOrderProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01680ac46592887cf4f321b771ff0e46039c775c4e9e9d8ed1edbc893ab45977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829175"
---
# <a name="iresultsviewersortorderproperty-property"></a>Propiedad IResultsViewer::SortOrderProperty

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use Windows [Search API](../search/-search-reference-entry-page.md) en su lugar. 

Esta propiedad establecerá o devolverá el orden de las columnas por las que ordenar los resultados.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SortOrderProperty(
  [in]          ColumnSortOrder order
);

HRESULT get_SortOrderProperty(
  [out, retval] ColumnSortOrder *order
);
```



## <a name="property-value"></a>Valor de propiedad

Establece la [**propiedad ColumnSortOrder.**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio sp1 \[\]<br/>                        |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





