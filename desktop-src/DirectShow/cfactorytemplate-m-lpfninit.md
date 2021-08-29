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
ms.openlocfilehash: c9f4a12c03e7e001845437f57f9799c7b0861f4f8f9b6cfac56aaa2bb80e51a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566925"
---
# <a name="cfactorytemplatem_lpfninit-member"></a>Miembro CFactoryTemplate::m \_ lpfnInit

Puntero a una función a la que se llama desde el punto de entrada dll. Puede ser **NULL.**

## <a name="syntax"></a>Sintaxis


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a>Comentarios

El tipo de puntero de función [**es LPFNInitRoutine.**](lpfninitroutine.md) Si proporciona esta función en el archivo DLL, la función de punto de entrada dll la llama con los parámetros siguientes:

-   *bLoading:* **TRUE** cuando se carga el archivo DLL, **FALSE** cuando se descarga el archivo DLL.
-   *rclsid:* puntero al CLISD del objeto, especificado en la variable miembro [**CFactoryTemplate::m \_ ClsID.**](cfactorytemplate-m-clsid.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CFactoryTemplate (clase)**](cfactorytemplate.md)
</dt> </dl>

 

 




