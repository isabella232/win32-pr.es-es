---
title: Método IWMDRMNetReceiver ProcessLicenseResponse (wmdrmsdk. h)
description: El método ProcessLicenseResponse procesa la respuesta de la licencia enviada por el transmisor en respuesta a un desafío de licencia.
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- Método ProcessLicenseResponse formato de Windows Media
- Método ProcessLicenseResponse formato de Windows Media, interfaz IWMDRMNetReceiver
- Interfaz IWMDRMNetReceiver formato de Windows Media, método ProcessLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09ebab81b71e21b9ef922423a7bbe67b20596
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679143"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a>IWMDRMNetReceiver::P método rocessLicenseResponse

El método **ProcessLicenseResponse** procesa la respuesta de la licencia enviada por el transmisor en respuesta a un desafío de licencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ProcessLicenseResponse(
  [in]  BYTE  *pbLicenseResponse,
  [in]  DWORD cbLicenseResponse,
  [out] BYTE  **ppbWMDRMNetLicenseRepresentation,
  [out] DWORD *pcbWMDRMNetLicenseRepresentation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbLicenseResponse* \[ de\]
</dt> <dd>

Respuesta de licencia recibida del transmisor.

</dd> <dt>

*cbLicenseResponse* \[ de\]
</dt> <dd>

Tamaño de la respuesta en bytes.

</dd> <dt>

*ppbWMDRMNetLicenseRepresentation* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe la dirección de la representación de la licencia interna para la licencia incluida en el mensaje de respuesta de la licencia. Cuando termine con estos datos, debe liberar la memoria mediante una llamada a **CoTaskMemFree**. Este parámetro se puede establecer en **null** si no se necesita la representación de la licencia.

</dd> <dt>

*pcbWMDRMNetLicenseRepresentation* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe el tamaño de la representación de la licencia. Debe establecerse en **null** si *ppbWMDRMNetLicenseRepresentation* es **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                | Descripción                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV \_ demasiado \_ pequeño**</dt> </dl> | Se necesita una lista de revocación de contenido actualizada.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | El método se ha llevado a cabo de forma correcta.<br/>                         |



 

## <a name="remarks"></a>Observaciones

La respuesta de licencia procesada mediante este método debe corresponder al último desafío de licencia generado en el equipo cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





