---
title: IBasicDevice remove_ConnectionStatusChanged método
description: Anula el registro de un controlador de eventos para el evento ConnectionStatusChanged. | IBasicDevice remove_ConnectionStatusChanged método
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- remove_ConnectionStatusChanged media streaming API
- remove_ConnectionStatusChanged media streaming API, interfaz IBasicDevice
- IBasicDevice interface Media Streaming API , remove_ConnectionStatusChanged método
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35b2f08b6df25f57d77f5c3677a4c6499370d9472202b6808073c5a75d1e2c34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599805"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a>IBasicDevice::remove \_ ConnectionStatusChanged (método)

Anula el registro de un controlador de eventos [**para el evento ConnectionStatusChanged.**](connectionstatuschanged.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*token* \[ En\]
</dt> <dd>

Referencia a un token obtenido del método [**\_ add ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) cuando se registró el controlador de eventos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





