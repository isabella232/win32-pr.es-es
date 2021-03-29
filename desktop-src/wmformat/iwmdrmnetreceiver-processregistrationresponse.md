---
title: Método IWMDRMNetReceiver ProcessRegistrationResponse (wmdrmsdk. h)
description: El método ProcessRegistrationResponse procesa una respuesta de registro enviada por el transmisor en respuesta a un desafío de registro.
ms.assetid: d0260e93-0a5e-494b-a723-bb62206ed55b
keywords:
- Método ProcessRegistrationResponse formato de Windows Media
- Método ProcessRegistrationResponse formato de Windows Media, interfaz IWMDRMNetReceiver
- Interfaz IWMDRMNetReceiver formato de Windows Media, método ProcessRegistrationResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessRegistrationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77b01f443d57825d82b7cf9556d7585745bb99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679142"
---
# <a name="iwmdrmnetreceiverprocessregistrationresponse-method"></a>IWMDRMNetReceiver::P método rocessRegistrationResponse

El método **ProcessRegistrationResponse** procesa una respuesta de registro enviada por el transmisor en respuesta a un desafío de registro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ProcessRegistrationResponse(
  [in]  BYTE     *pbRegistrationResponse,
  [in]  DWORD    cbRegistrationResponse,
  [out] IUnknown **ppunkCancellationCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbRegistrationResponse* \[ de\]
</dt> <dd>

Respuesta de registro recibida del transmisor.

</dd> <dt>

*cbRegistrationResponse* \[ de\]
</dt> <dd>

Tamaño de la respuesta de registro en bytes.

</dd> <dt>

*ppunkCancellationCookie* \[ enuncia\]
</dt> <dd>

Puntero que recibe un puntero a la interfaz **IUnknown** de un objeto que identifica esta llamada asincrónica. Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método se ejecuta de forma asincrónica; una vez completado el procesamiento, el evento MEProximityCompleted se envía a la interfaz **IMFMediaEventGenerator** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::GetRegistrationChallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)
</dt> </dl>

 

 





