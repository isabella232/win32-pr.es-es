---
title: Propiedad HelpText de IResultVerb (WdsSharedIDL.h)
description: Esta propiedad devuelve un puntero a la cadena de ayuda localizada para el verbo.
ms.assetid: 14e91101-5ee2-459a-97d7-35c76d3ba990
keywords:
- Propiedad HelpText Características heredadas Windows entorno de trabajo
- Propiedad HelpText Legacy Windows Environment Features , IResultVerb (Interfaz IResultVerb)
- IResultVerb interface Legacy Windows Environment Features , HelpText property
topic_type:
- apiref
api_name:
- IResultVerb.HelpText
- IResultVerb.get_HelpText
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d314e9cd84382449273ddbfb0ee54ae9b6c7aa1fdb528cc33db4a85abd5ce02d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014315"
---
# <a name="iresultverbhelptext-property"></a>IResultVerb::HelpText, propiedad

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Esta propiedad devuelve un puntero a la cadena de ayuda localizada para el verbo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_HelpText(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un puntero a la cadena de ayuda localizada para este verbo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





