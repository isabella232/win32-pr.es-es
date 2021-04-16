---
title: Método GetURL IWMDRMNonSilentLicenseAquisition (wmdrmsdk. h)
description: El método GetURL recupera la dirección URL a la que se debe publicar el desafío de licencia.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- Método GetURL formato de Windows Media
- Método GetURL formato de Windows Media, interfaz IWMDRMNonSilentLicenseAquisition
- Interfaz IWMDRMNonSilentLicenseAquisition formato de Windows Media, método GetURL
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetURL
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79212d19d7dbf4a66e2b72dcbdeba9262a9aeddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679139"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a>IWMDRMNonSilentLicenseAquisition:: GetURL (método)

El método **getURL** recupera la dirección URL a la que se debe publicar el desafío de licencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbstrURL* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe la dirección URL.

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
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





