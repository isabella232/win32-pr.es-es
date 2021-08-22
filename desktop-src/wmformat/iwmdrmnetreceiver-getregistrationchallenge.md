---
title: Método IWMDRMNetReceiver GetRegistrationChallenge (Wmdrmsdk.h)
description: El método GetRegistrationChallenge genera un mensaje Windows desafío de registro de DRM multimedia para dispositivos de red.
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- Método GetRegistrationChallenge windows Media Format
- Método GetRegistrationChallenge windows Media Format , interfaz IWMDRMNetReceiver
- IWMDRMNetReceiver interface windows Media Format , Método GetRegistrationChallenge
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
ms.openlocfilehash: 7f6c066de9c455006bfa7e500a30ac290299956ba03a6b4d8df6652a60a75a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701040"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a>IWMDRMNetReceiver::GetRegistrationChallenge (método)

El **método GetRegistrationChallenge** genera un mensaje Windows desafío de registro de DRM multimedia para dispositivos de red.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppbRegistrationChallenge* \[ out\]
</dt> <dd>

Dirección de un puntero que recibe la dirección del desafío generado. Cuando termine con estos datos, debe liberar la memoria llamando a **CoTaskMemFree**.

</dd> <dt>

*pwRegistrationChallenge* \[ out\]
</dt> <dd>

Dirección de una variable que recibe el tamaño del desafío de registro en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::P rocessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





