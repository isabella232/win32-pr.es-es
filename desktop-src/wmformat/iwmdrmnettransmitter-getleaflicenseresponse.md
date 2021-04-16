---
title: Método IWMDRMNetTransmitter GetLeafLicenseResponse (wmdrmsdk. h)
description: El método GetLeafLicenseResponse genera un mensaje de respuesta de licencia de hoja.
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- Método GetLeafLicenseResponse formato de Windows Media
- Método GetLeafLicenseResponse formato de Windows Media, interfaz IWMDRMNetTransmitter
- Interfaz IWMDRMNetTransmitter formato de Windows Media, método GetLeafLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetLeafLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf2374966abfae4353a72755313c1cbbdfb7287
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679141"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a>IWMDRMNetTransmitter:: GetLeafLicenseResponse (método)

El método **GetLeafLicenseResponse** genera un mensaje de respuesta de licencia de hoja.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLeafLicenseResponse(
  [in]  BSTR            bstrKID,
  [in]  WMDRMNET_POLICY *pPolicy,
  [out] IWMDRMEncrypt   **ppIWMDRMEncrypt,
  [out] BYTE            **ppbLicenseResponse,
  [out] DWORD           *pcbLicenseResponse
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrKID* \[ de\]
</dt> <dd>

Identificador de clave codificado en Base64 que se va a usar para la nueva licencia de hoja. El identificador de clave debe ser un valor GUID generado aleatoriamente.

</dd> <dt>

*pPolicy* \[ de\]
</dt> <dd>

Puntero a la estructura de [**\_ Directiva WMDRMNET**](wmdrmnet-policy.md) que define la Directiva que se va a usar para la licencia de hoja.

</dd> <dt>

*ppIWMDRMEncrypt* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IWMDRMEncrypt**](iwmdrmencrypt.md) que se puede usar para cifrar los datos de la nueva licencia de hoja.

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

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





