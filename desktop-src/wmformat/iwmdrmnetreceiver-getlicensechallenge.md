---
title: Método IWMDRMNetReceiver GetLicenseChallenge (wmdrmsdk. h)
description: El método GetLicenseChallenge genera un desafío de licencia de DRM de Windows Media para dispositivos de red que se puede enviar a un transmisor al solicitar contenido protegido.
ms.assetid: c13b9e9e-b076-411b-a106-b602544faaba
keywords:
- Método GetLicenseChallenge formato de Windows Media
- Método GetLicenseChallenge formato de Windows Media, interfaz IWMDRMNetReceiver
- Interfaz IWMDRMNetReceiver formato de Windows Media, método GetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f58b85b8dc5edd6c23e809dda8c18bf30137f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679144"
---
# <a name="iwmdrmnetreceivergetlicensechallenge-method"></a>IWMDRMNetReceiver:: GetLicenseChallenge (método)

El método **GetLicenseChallenge** genera un desafío de licencia de DRM de Windows Media para dispositivos de red que se puede enviar a un transmisor al solicitar contenido protegido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLicenseChallenge(
  [in]  BSTR  bstrAction,
  [out] BYTE  **ppbLicenseChallenge,
  [out] DWORD *pcbLicenseChallenge
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrAction* \[ de\]
</dt> <dd>

Acción para la que se va a generar el desafío.

</dd> <dt>

*ppbLicenseChallenge* \[ enuncia\]
</dt> <dd>

Dirección de un puntero que se establece en la dirección del desafío generado. Cuando termine con estos datos, debe liberar la memoria mediante una llamada a **CoTaskMemFree**.

</dd> <dt>

*pcbLicenseChallenge* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe el tamaño del desafío de la licencia en bytes.

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

[**IWMDRMNetReceiver::P rocessLicenseResponse**](iwmdrmnetreceiver-processlicenseresponse.md)
</dt> </dl>

 

 





