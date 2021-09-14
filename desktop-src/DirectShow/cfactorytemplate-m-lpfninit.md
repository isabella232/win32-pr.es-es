---
description: Puntero a una función a la que se llama desde el punto de entrada dll. Puede ser NULL.
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: CFactoryTemplate::m_lpfnInit miembro (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnInit
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b44181f926f77ecc7cc22673622d4a0d3dcb7d26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266583"
---
# <a name="cfactorytemplatem_lpfninit-member"></a>Miembro CFactoryTemplate::m \_ lpfnInit

Puntero a una función a la que se llama desde el punto de entrada dll. Puede ser **NULL.**

## <a name="syntax"></a>Sintaxis


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a>Observaciones

El tipo de puntero de función [**es LPFNInitRoutine.**](lpfninitroutine.md) Si proporciona esta función en el archivo DLL, la función de punto de entrada dll la llama con los parámetros siguientes:

-   *bLoading:* **TRUE** cuando se carga el archivo DLL, **FALSE** cuando se descarga el archivo DLL.
-   *rclsid:* puntero al CLISD del objeto, especificado en la variable miembro [**CFactoryTemplate::m \_ ClsID.**](cfactorytemplate-m-clsid.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CFactoryTemplate (clase)**](cfactorytemplate.md)
</dt> </dl>

 

 




