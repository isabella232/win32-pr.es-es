---
description: El Conectar método completa una conexión al pin de salida.
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: CPullPin. Conectar método (Pullpin.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063327"
---
# <a name="cpullpinconnect-method"></a>CPullPin. Conectar método

El `Connect` método completa una conexión a la patilla de salida.

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

*Punk* 
</dt> <dd>

Puntero a la **interfaz IUnknown** del pin de salida.

</dd> <dt>

*pAlloc* 
</dt> <dd>

Puntero a la [**interfaz IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador preferido del pin de entrada, o **NULL.**

</dd> <dt>

*bSync* 
</dt> <dd>

Valor booleano que especifica si se deben usar lecturas sincrónicas. Si **es TRUE,** el pin realiza operaciones de lectura sincrónicas en el pin de salida. Si **es FALSE,** el pin realiza solicitudes de lectura asincrónicas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                               | Descripción                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Correcto.<br/>                                                             |
| <dl> <dt>**VFW \_ E \_ YA \_ CONECTADO**</dt> </dl> | El pin de entrada ya está conectado.<br/>                                  |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>             | El pin de salida no expone [**IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)<br/> |



 

## <a name="remarks"></a>Observaciones

Llame a este método durante el proceso de conexión del pin de entrada. Si se produce un error en el método , el pin debería producir un error en la conexión.

Este método consulta el pin de salida de la **interfaz IAsyncReader.** Si se realiza correctamente, llama a [**CPullPin::D ecideAllocator**](cpullpin-decideallocator.md) para negociar el asignador de la conexión. Si el pin de entrada tiene un asignador preferido, esfírcallo en el *parámetro pAlloc;* El **método DecideAllocator** pasa este puntero al método [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) del pin de salida. De lo contrario, *establezca pAlloc* en **NULL.**

Si el valor de *bSync* es **TRUE**, el objeto **CPullPin** realiza solicitudes de lectura sincrónicas, llamando a [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)del pin de salida. De lo contrario, llama al [**método IAsyncReader::Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) para realizar solicitudes de lectura superpuestas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




