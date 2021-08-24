---
title: Método IWMDRMNetTransmitter GetLeafLicenseResponse (Wmdrmsdk.h)
description: El método GetLeafLicenseResponse genera un mensaje de respuesta de licencia hoja.
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- Formato de windows Media del método GetLeafLicenseResponse
- Método GetLeafLicenseResponse windows Media Format , interfaz IWMDRMNetTransmitter
- IWMDRMNetTransmitter interface windows Media Format , Método GetLeafLicenseResponse
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
ms.openlocfilehash: aff470341c3227782d0d34cbdd2ca2a4a51a4cb1b6214b81ea2ea9a384b29ee2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084835"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a>Método IWMDRMNetTransmitter::GetLeafLicenseResponse

El **método GetLeafLicenseResponse** genera un mensaje de respuesta de licencia hoja.

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

*bstrKID* \[ En\]
</dt> <dd>

Identificador de clave codificado en Base64 que se usará para la nueva licencia hoja. El identificador de clave debe ser un valor GUID generado aleatoriamente.

</dd> <dt>

*pPolicy* \[ En\]
</dt> <dd>

Puntero a la [**estructura WMDRMNET \_ POLICY**](wmdrmnet-policy.md) que define la directiva que se usará para la licencia hoja.

</dd> <dt>

*ppIWMDRMEncrypt* \[ out\]
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IWMDRMEncrypt**](iwmdrmencrypt.md) que se puede usar para cifrar los datos de la nueva licencia de hoja.

</dd> <dt>

*ppbLicenseResponse* \[ out\]
</dt> <dd>

Dirección de una variable que recibe la dirección de la respuesta de licencia generada. Cuando termine con estos datos, debe liberar la memoria llamando a **CoTaskMemFree**.

</dd> <dt>

*pwLicenseResponse* \[ out\]
</dt> <dd>

Dirección de una variable que recibe el tamaño de la respuesta de licencia, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                | Descripción                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV DEMASIADO \_ \_ PEQUEÑO**</dt> </dl> | Se necesita una lista de revocación de contenido actualizada.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | El método se ha llevado a cabo de forma correcta.<br/>                         |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





