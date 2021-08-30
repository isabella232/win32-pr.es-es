---
description: El método IsClassID determina si un CLSID coincide con esta plantilla de clase.
ms.assetid: de560f7a-2ccb-44e2-ac32-3b0fea0d80b8
title: Método CFactoryTemplate.IsClassID (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.IsClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38714c6c6a97c46a14d1e381fdf49ddbc723d04ee217a09c9554b39d4eb22491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055795"
---
# <a name="cfactorytemplateisclassid-method"></a>CFactoryTemplate.IsClassID (método)

El `IsClassID` método determina si un CLSID coincide con esta plantilla de clase.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsClassID(
   REFCLSID rclsid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rclsid* 
</dt> <dd>

Referencia a un CLSID.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el *parámetro rclsid* es el mismo CLSID que la variable miembro [**CFactoryTemplate::m \_ ClsID**](cfactorytemplate-m-clsid.md) o devuelve **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CFactoryTemplate (clase)**](cfactorytemplate.md)
</dt> </dl>

 

 




