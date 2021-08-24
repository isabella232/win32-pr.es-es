---
title: Método IWMDRMNetTransmitter GetRootLicenseResponse (Wmdrmsdk.h)
description: El método GetRootLicenseResponse genera un mensaje de respuesta de licencia raíz.
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- Formato de windows Media del método GetRootLicenseResponse
- Método GetRootLicenseResponse windows Media Format , interfaz IWMDRMNetTransmitter
- IWMDRMNetTransmitter interface windows Media Format , Método GetRootLicenseResponse
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
ms.openlocfilehash: de89389163a9eae66a0dcda14dd6b9699d3db9650140cceac6498b2ab77a4e44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707935"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a>Método IWMDRMNetTransmitter::GetRootLicenseResponse

El **método GetRootLicenseResponse** genera un mensaje de respuesta de licencia raíz.

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

*bstrKID* \[ En\]
</dt> <dd>

Identificador de clave codificado en Base64 que se usará para la nueva licencia raíz. El identificador de clave debe ser un valor GUID generado aleatoriamente.

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



 

## <a name="remarks"></a>Comentarios

La licencia raíz generada se crea con la información de los datos de desafío de licencia, que se procesa para la interfaz mediante una llamada a [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).

La licencia raíz se usa en la generación de licencias hoja, lo que se logra mediante una llamada al [**método GetLeafLicenseResponse.**](iwmdrmnettransmitter-getleaflicenseresponse.md) La **interfaz IWMDRMNetTransmitter** mantiene una copia de la licencia raíz para ese uso.

La licencia raíz creada mediante una llamada a este método no tiene ninguna directiva y está configurada para que no se pueda conservar en el dispositivo receptor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





