---
description: 'Constructor CBaseVideoRenderer.CBaseVideoRenderer: método constructor.'
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Constructor CBaseVideoRenderer.CBaseVideoRenderer (Renbase.h)
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
ms.openlocfilehash: c0ae558238b94402150e5cb15373d202065e485e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095843"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a>Constructor CBaseVideoRenderer.CBaseVideoRenderer

Método constructor.

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

Puntero a una descripción utilizada con fines de depuración.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero al objeto propietario agregado.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a un **valor HRESULT.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




