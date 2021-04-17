---
description: Método de constructor.
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Constructor CBaseVideoRenderer. CBaseVideoRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ed49be63d9c2c05e12a2ac92ae33f64705460b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680287"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a>Constructor CBaseVideoRenderer. CBaseVideoRenderer

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RenderClass* 
</dt> <dd>

Identificador de clase para este representador.

</dd> <dt>

*pName* 
</dt> <dd>

Puntero a una descripción que se usa para la depuración.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntero al objeto propietario agregado.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a un valor **HRESULT** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




