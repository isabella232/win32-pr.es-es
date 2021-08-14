---
title: Propiedad IPropertyFilter UID (WdsSharedIDL.h)
description: UID de la propiedad por la que filtrar.
ms.assetid: a9dfb34c-a161-4d5f-8d01-695b2f9346e6
keywords:
- Características heredadas del entorno de Windows UID
- Propiedades de UID heredadas Windows environment features , IPropertyFilter (interfaz)
- IPropertyFilter interface Legacy Windows Environment Features , UID property
topic_type:
- apiref
api_name:
- IPropertyFilter.UID
- IPropertyFilter.get_UID
- IPropertyFilter.put_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d0e96fc2c207a3dc7e11d751cb2e545f6d917036b3ce8f184280807c71f55e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963785"
---
# <a name="ipropertyfilteruid-property"></a>Propiedad IPropertyFilter::UID

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use Windows [Search API](../search/-search-reference-entry-page.md) en su lugar. 

UID de la propiedad por la que filtrar.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_UID(
  [in]          long uid
);

HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a>Valor de propiedad

Establece la propiedad UID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio sp1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





