---
title: Método IWMDRMNetReceiver ProcessRegistrationResponse (Wmdrmsdk.h)
description: El método ProcessRegistrationResponse procesa una respuesta de registro enviada por el transmisor en respuesta a un desafío de registro.
ms.assetid: d0260e93-0a5e-494b-a723-bb62206ed55b
keywords:
- ProcessRegistrationResponse, método windows Media Format
- Método ProcessRegistrationResponse windows Media Format , interfaz IWMDRMNetReceiver
- IWMDRMNetReceiver interface windows Media Format , ProcessRegistrationResponse method
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
ms.openlocfilehash: 4a0461bc19aa1f3de2751516aedc8e76a0201417fe017881fb0fbd8da8156b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930815"
---
# <a name="iwmdrmnetreceiverprocessregistrationresponse-method"></a>Método IWMDRMNetReceiver::P rocessRegistrationResponse

El **método ProcessRegistrationResponse** procesa una respuesta de registro enviada por el transmisor en respuesta a un desafío de registro.

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

*pbRegistrationResponse* \[ En\]
</dt> <dd>

Respuesta de registro recibida del transmisor.

</dd> <dt>

*cbRegistrationResponse* \[ En\]
</dt> <dd>

Tamaño de la respuesta de registro en bytes.

</dd> <dt>

*piqueCancellationCookie* \[ out\]
</dt> <dd>

Puntero que recibe un puntero a la **interfaz IUnknown** de un objeto que identifica esta llamada asincrónica. Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al [**método IWMDRMEventGenerator::CancelAsyncOperation.**](iwmdrmeventgenerator-cancelasyncoperation.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método se ejecuta de forma asincrónica; Una vez completado el procesamiento, el evento MEProximityCompleted se envía a la interfaz **DEERMEDIAEventGenerator.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::GetRegistrationChallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)
</dt> </dl>

 

 





