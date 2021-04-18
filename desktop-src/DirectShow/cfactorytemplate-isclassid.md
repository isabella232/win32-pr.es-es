---
description: El método IsClassID determina si un CLSID coincide con esta plantilla de clase.
ms.assetid: de560f7a-2ccb-44e2-ac32-3b0fea0d80b8
title: Método CFactoryTemplate. IsClassID (ComBase. h)
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
ms.openlocfilehash: 94564d7e9db52f8be22717a10f73fffb7fb6fa14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660854"
---
# <a name="cfactorytemplateisclassid-method"></a>CFactoryTemplate. IsClassID, método

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

Devuelve **true** si el *parámetro rclsid* es el mismo CLSID que la variable miembro [**CFactoryTemplate:: m \_ CLSID**](cfactorytemplate-m-clsid.md) ; de lo contrario, devuelve **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




