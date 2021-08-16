---
title: Método IWMDRMNonSilentLicenseAquisition GetURL (Wmdrmsdk.h)
description: El método GetURL recupera la dirección URL en la que se debe publicar el desafío de licencia.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- Formato multimedia de windows del método GetURL
- Método GetURL windows Media Format , interfaz IWMDRMNonSilentLicenseAquisition
- IWMDRMNonSilentLicenseAquisition interface windows Media Format , Método GetURL
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
ms.openlocfilehash: b7979d82363b21b58563a606c31a99d069a60a3bc5b2da162a7339513c2867bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084712"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a>IWMDRMNonSilentLicenseAquisition::GetURL (método)

El **método GetURL** recupera la dirección URL en la que se debe publicar el desafío de licencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbstrURL* \[ out\]
</dt> <dd>

Dirección de una variable que recibe la dirección URL.

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
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMDRMNonSilentLicenseAquisition (Interfaz)**](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





