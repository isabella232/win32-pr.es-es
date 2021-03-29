---
description: El método Connect completa una conexión con el terminal de salida.
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: Método CPullPin. Connect (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97e3b0b676e02dee0e3ebd82de9def56edc2ea28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680838"
---
# <a name="cpullpinconnect-method"></a>CPullPin. Connect (método)

El `Connect` método completa una conexión con el PIN de salida.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Connect(
   IUnknown      *pUnk,
   IMemAllocator *pAlloc,
   BOOL          bSync
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pUnk* 
</dt> <dd>

Puntero a la interfaz **IUnknown** del PIN de salida.

</dd> <dt>

*pAlloc* 
</dt> <dd>

Puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador preferido del PIN de entrada o **null**.

</dd> <dt>

*bSync* 
</dt> <dd>

Valor booleano que especifica si se van a utilizar lecturas sincrónicas. Si **es true**, el PIN realiza operaciones de lectura sincrónicas en el PIN de salida. Si **es false**, el PIN realiza solicitudes de lectura asincrónicas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT**. Estos son algunos de los valores posibles.



| Código devuelto                                                                                               | Descripción                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                      | Correcto.<br/>                                                             |
| <dl> <dt>**VFW \_ E \_ ya \_ conectado**</dt> </dl> | El PIN de entrada ya está conectado.<br/>                                  |
| <dl> <dt>**E \_ NOinterface**</dt> </dl>             | El PIN de salida no expone [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).<br/> |



 

## <a name="remarks"></a>Observaciones

Llame a este método durante el proceso de conexión del terminal de entrada. Si se produce un error en el método, el PIN debe producir un error en la conexión.

Este método consulta el PIN de salida de la interfaz **IAsyncReader** . Si se realiza correctamente, llama a [**CPullPin::D ecideallocator**](cpullpin-decideallocator.md) para negociar el asignador de la conexión. Si el PIN de entrada tiene un asignador preferido, especifíquelo en el parámetro *pAlloc* . el método **DecideAllocator** pasa este puntero al método [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) del terminal de salida. En caso contrario, establezca *pAlloc* en **null**.

Si el valor de *bSync* es **true**, el objeto **CPullPin** realiza solicitudes sincrónicas de lectura, llamando a [**IAsyncReader:: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)del terminal de salida. De lo contrario, llama al método [**IAsyncReader:: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) para realizar solicitudes de lectura superpuestas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> </dl>

 

 




