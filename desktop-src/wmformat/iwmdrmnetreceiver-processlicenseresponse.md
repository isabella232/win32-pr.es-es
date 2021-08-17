---
title: Método IWMDRMNetReceiver ProcessLicenseResponse (Wmdrmsdk.h)
description: El método ProcessLicenseResponse procesa la respuesta de licencia que envía el transmisor en respuesta a un desafío de licencia.
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- Formato multimedia de windows del método ProcessLicenseResponse
- Método ProcessLicenseResponse windows Media Format , interfaz IWMDRMNetReceiver
- IWMDRMNetReceiver interface windows Media Format , ProcessLicenseResponse method
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
ms.openlocfilehash: cb7ba84c7bf58091bb17500b0d35390062710a79a9a32b939ac8b9517cbcfaba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700829"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a>Método IWMDRMNetReceiver::P rocessLicenseResponse

El **método ProcessLicenseResponse** procesa la respuesta de licencia que envía el transmisor en respuesta a un desafío de licencia.

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

*pbLicenseResponse* \[ En\]
</dt> <dd>

Respuesta de licencia recibida del transmisor.

</dd> <dt>

*cbLicenseResponse* \[ En\]
</dt> <dd>

Tamaño de la respuesta en bytes.

</dd> <dt>

*ppbWMDRMNetLicenseRepresentation* \[ out\]
</dt> <dd>

Dirección de una variable que recibe la dirección de la representación interna de la licencia para la licencia contenida en el mensaje de respuesta de licencia. Cuando termine con estos datos, debe liberar la memoria llamando a **CoTaskMemFree**. Este parámetro puede establecerse en **NULL si** no se necesita la representación de licencia.

</dd> <dt>

*pwWMDRMNetLicenseRepresentation* \[ out\]
</dt> <dd>

Dirección de una variable que recibe el tamaño de la representación de licencia. Debe establecerse en **NULL si** *ppbWMDRMNetLicenseRepresentation* es **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                | Descripción                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV DEMASIADO \_ \_ PEQUEÑO**</dt> </dl> | Se necesita una lista de revocación de contenido actualizada.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | El método se ha llevado a cabo de forma correcta.<br/>                         |



 

## <a name="remarks"></a>Comentarios

La respuesta de licencia procesada mediante este método debe corresponder al último desafío de licencia generado en el equipo cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





