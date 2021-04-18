---
description: Método de constructor.
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Constructor CBaseControlVideo. CBaseControlVideo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dea0548079f8eb703f0c17557cab6a5e634cf242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690352"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a>Constructor CBaseControlVideo. CBaseControlVideo

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFilter* 
</dt> <dd>

Puntero al objeto de filtro multimedia propietario.

</dd> <dt>

*pInterfaceLock* 
</dt> <dd>

Puntero a la sección crítica que se va a usar para el bloqueo.

</dd> <dt>

*pName* 
</dt> <dd>

Puntero a la descripción del objeto.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntero a la interfaz **IUnknown** de control, si el objeto forma parte de un agregado; de lo contrario, debe ser **null**.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a una variable que recibe un valor HRESULT que indica si el método de constructor se ha ejecutado correctamente o no.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El objeto implementa la interfaz de control [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .

Todos los métodos de interfaz de [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) que esta clase implementa requieren que el filtro se conecte correctamente. Por esta razón, se pasa a la clase un código PIN con el que se debe sincronizar. Siempre que se llama a un método de interfaz, el objeto determina que el PIN sigue conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




