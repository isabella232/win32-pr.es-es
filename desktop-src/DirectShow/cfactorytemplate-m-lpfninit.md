---
description: Puntero a una función a la que se llama desde el punto de entrada de DLL. Puede ser NULL.
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: 'Miembro CFactoryTemplate:: m_lpfnInit (ComBase. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660848"
---
# <a name="cfactorytemplatem_lpfninit-member"></a>Miembro lpfnInit CFactoryTemplate:: m \_

Puntero a una función a la que se llama desde el punto de entrada de DLL. Puede ser **null**.

## <a name="syntax"></a>Sintaxis


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a>Observaciones

El tipo de puntero de función es [**LPFNInitRoutine**](lpfninitroutine.md). Si proporciona esta función en el archivo DLL, la función de punto de entrada del archivo DLL lo llama con los parámetros siguientes:

-   *bLoading*: **true** cuando se carga el archivo dll, **false** cuando se descarga el archivo dll.
-   *rclsid*: puntero a la CLISD del objeto, que se especifica en la variable miembro de [**\_ ClsID CFactoryTemplate:: m**](cfactorytemplate-m-clsid.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




