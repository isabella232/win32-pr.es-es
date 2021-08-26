---
title: Propiedad IResultVerb Enabled (WdsSharedIDL.h)
description: Esta propiedad devuelve TRUE si el verbo está habilitado.
ms.assetid: 27e3dbb8-678e-46c7-82e5-40b86cb157a7
keywords:
- Características del entorno de Windows propiedad habilitada
- Propiedad habilitada Características heredadas Windows entorno, interfaz IResultVerb
- IResultVerb interface Legacy Windows Environment Features , Enabled property
topic_type:
- apiref
api_name:
- IResultVerb.Enabled
- IResultVerb.get_Enabled
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c96a4c40252bf6b5ab74d3d4ec96e2568dffeed624ae2b5126059192dd72d9e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014325"
---
# <a name="iresultverbenabled-property"></a>Propiedad IResultVerb::Enabled

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use Windows [Search API](../search/-search-reference-entry-page.md) en su lugar. 

Esta propiedad devuelve TRUE si el verbo está habilitado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *flag
);
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad devuelve True si el verbo está habilitado o False si no es así.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio sp1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





