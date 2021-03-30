---
title: Propiedad IPropertyFilter IndexColumn (WdsSharedIDL. h)
description: Nombre de columna indizada de la propiedad por la que se va a filtrar.
ms.assetid: 18ce0c89-bdaa-4f83-bf03-c11b55a842f5
keywords:
- Propiedad IndexColumn características de entorno heredado de Windows
- Propiedad IndexColumn características de entorno heredado de Windows, interfaz IPropertyFilter
- Interfaz IPropertyFilter características del entorno heredado de Windows, propiedad IndexColumn
topic_type:
- apiref
api_name:
- IPropertyFilter.IndexColumn
- IPropertyFilter.get_IndexColumn
- IPropertyFilter.put_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e55a59b4615f4b6c19dcb5f07d16394d2531f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079322"
---
# <a name="ipropertyfilterindexcolumn-property"></a>IPropertyFilter:: IndexColumn (propiedad)

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Nombre de columna indizada de la propiedad por la que se va a filtrar.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_IndexColumn(
  [in]          BSTR column
);

HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Valor de propiedad

Establece la propiedad de columna.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





