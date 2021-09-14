---
description: El método SetNotify establece o quita una devolución de llamada en el asignador. El asignador llama al método de devolución de llamada cada vez que se llama al método IMemAllocator::ReleaseBuffer del asignador.
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: Método CBaseAllocator.SetNotify (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8269112325d470cae59cff6e615f04fbdfab91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070134"
---
# <a name="cbaseallocatorsetnotify-method"></a>CBaseAllocator.SetNotify (método)

\[[**SetNotify puede**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) modificarse o no estar disponible en versiones posteriores.\]

El `SetNotify` método establece o quita una devolución de llamada en el asignador. El asignador llama al método de devolución de llamada cada vez que se llama al método [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) del asignador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNotify* 
</dt> <dd>

Puntero a la [**interfaz IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) que se usará para la devolución de llamada. El autor de la llamada debe implementar la interfaz . Use el valor **NULL para** quitar la devolución de llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Este método implementa el [**método IMemAllocatorCallbackTemp::SetNotify.**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) El asignador no expone la interfaz [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) a menos que la marca *fEnableReleaseCallback* esté establecida en **TRUE** en el constructor [**CBaseAllocator.**](cbaseallocator.md)

Este método establece la variable [**miembro CBaseAllocator::m \_ pNotify**](cbaseallocator-m-pnotify.md) igual a *pNotify* e incrementa el recuento de referencias en la interfaz . Si *m \_ pNotify* no es **NULL,** el método **ReleaseBuffer** del asignador llama a [**IMemAllocatorNotifyCallbackTemp::NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease). Vea la sección Comentarios de ese método para obtener información sobre cómo implementar la devolución de llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




