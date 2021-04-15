---
title: Propiedad de sugerencia IResultProperty (WdsSharedIDL. h)
description: Valor especial que se usa para ayudar a la recuperación de datos.
ms.assetid: fa888c5e-898e-4f48-b87e-2d0d078fd1fe
keywords:
- Propiedad Hint características heredadas del entorno de Windows
- Propiedad Hint características de entorno de Windows heredadas, interfaz IResultProperty
- Interfaz IResultProperty características de entorno heredado de Windows, propiedad Hint
topic_type:
- apiref
api_name:
- IResultProperty.Hint
- IResultProperty.get_Hint
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3edfed528ab6a6833cced99c113c33e7e2f859d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695892"
---
# <a name="iresultpropertyhint-property"></a>IResultProperty:: Hint (propiedad)

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Valor especial que se usa para ayudar a la recuperación de datos.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Hint(
  [out, retval] ling *hint
);
```



## <a name="property-value"></a>Valor de propiedad

Devuelve un puntero a la sugerencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





