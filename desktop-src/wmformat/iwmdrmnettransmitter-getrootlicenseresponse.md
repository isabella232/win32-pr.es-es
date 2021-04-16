---
title: Método IWMDRMNetTransmitter GetRootLicenseResponse (wmdrmsdk. h)
description: El método GetRootLicenseResponse genera un mensaje de respuesta de licencia raíz.
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- Método GetRootLicenseResponse formato de Windows Media
- Método GetRootLicenseResponse formato de Windows Media, interfaz IWMDRMNetTransmitter
- Interfaz IWMDRMNetTransmitter formato de Windows Media, método GetRootLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetRootLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3497a3eaedb872b7d2c9eb5d7782d01f8b35462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679484"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a>IWMDRMNetTransmitter:: GetRootLicenseResponse (método)

El método **GetRootLicenseResponse** genera un mensaje de respuesta de licencia raíz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRootLicenseResponse(
  [in]  BSTR  bstrKID,
  [out] BYTE  **ppbLicenseResponse,
  [out] DWORD *pcbLicenseResponse
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrKID* \[ de\]
</dt> <dd>

Identificador de clave codificado en Base64 que se va a usar para la nueva licencia raíz. El identificador de clave debe ser un valor GUID generado aleatoriamente.

</dd> <dt>

*ppbLicenseResponse* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe la dirección de la respuesta de licencia generada. Cuando termine con estos datos, debe liberar la memoria mediante una llamada a **CoTaskMemFree**.

</dd> <dt>

*pcbLicenseResponse* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe el tamaño de la respuesta de la licencia, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                | Descripción                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV \_ demasiado \_ pequeño**</dt> </dl> | Se necesita una lista de revocación de contenido actualizada.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | El método se ha llevado a cabo de forma correcta.<br/>                         |



 

## <a name="remarks"></a>Observaciones

La licencia raíz generada se crea con la información de los datos del desafío de la licencia, que se procesa para la interfaz llamando a [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).

La licencia raíz se usa en la generación de licencias de hoja, lo que se logra mediante una llamada al método [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) . La interfaz **IWMDRMNetTransmitter** mantiene una copia de la licencia raíz para ese uso.

La licencia raíz creada mediante una llamada a este método no tiene directivas y está configurada para que no se pueda conservar en el dispositivo receptor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





