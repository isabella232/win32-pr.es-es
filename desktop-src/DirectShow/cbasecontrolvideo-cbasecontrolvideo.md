---
description: 'Constructor CBaseControlVideo.CBaseControlVideo: método constructor.'
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Constructor CBaseControlVideo.CBaseControlVideo (Ctlutil.h)
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
ms.openlocfilehash: bbd9ed452dbf0c0091c3f1813f6f671c476dfa52e31b402440a3b1d19db2d3d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057375"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a>Constructor CBaseControlVideo.CBaseControlVideo

Método constructor.

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

Puntero al objeto de filtro de medios propietario.

</dd> <dt>

*pInterfaceLock* 
</dt> <dd>

Puntero a la sección crítica que se usará para el bloqueo.

</dd> <dt>

*pName* 
</dt> <dd>

Puntero a la descripción del objeto.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero a la **interfaz IUnknown de control,** si el objeto forma parte de un agregado; de lo contrario, debe ser **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a una variable que recibe un valor HRESULT que indica el éxito o error del método constructor.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El objeto implementa la interfaz de control [**IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo)

Todos los métodos de interfaz [**de IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) que implementa esta clase requieren que el filtro esté conectado correctamente. Por este motivo, a la clase se le pasa un pin con el que debe sincronizarse. Cada vez que se llama a un método de interfaz, el objeto determina que el pin sigue conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




