---
description: 'Constructor CBaseRenderer.CBaseRenderer: método constructor.'
ms.assetid: df5efbb3-6bce-4e30-b1b1-d69bf64fa87d
title: Constructor CBaseRenderer.CBaseRenderer (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b7041444e40aa926efbeebd074d8e8bb736bdd1005c35730dac86a87303927f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044005"
---
# <a name="cbaserenderercbaserenderer-constructor"></a>Constructor CBaseRenderer.CBaseRenderer

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RenderClass* 
</dt> <dd>

Identificador de clase del representador.

</dd> <dt>

*pName* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del filtro, con fines de depuración.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero al propietario de este objeto. Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Recibe un **valor HRESULT.**

</dd> <dt>

*TimerResolution* 
</dt> <dd>

Resolución del temporizador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




