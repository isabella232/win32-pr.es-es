---
title: Método IWMDRMNetReceiver GetRegistrationChallenge (wmdrmsdk. h)
description: El método GetRegistrationChallenge genera un mensaje de desafío de registro de DRM de Windows Media para dispositivos de red.
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- Método GetRegistrationChallenge formato de Windows Media
- Método GetRegistrationChallenge formato de Windows Media, interfaz IWMDRMNetReceiver
- Interfaz IWMDRMNetReceiver formato de Windows Media, método GetRegistrationChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetRegistrationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a292749e95ca6ba2dabc8f3829eae827dbdd8325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680908"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a>IWMDRMNetReceiver:: GetRegistrationChallenge (método)

El método **GetRegistrationChallenge** genera un mensaje de desafío de registro de DRM de Windows Media para dispositivos de red.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppbRegistrationChallenge* \[ enuncia\]
</dt> <dd>

Dirección de un puntero que recibe la dirección del desafío generado. Cuando termine con estos datos, debe liberar la memoria mediante una llamada a **CoTaskMemFree**.

</dd> <dt>

*pcbRegistrationChallenge* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe el tamaño del desafío de registro en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::P rocessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





