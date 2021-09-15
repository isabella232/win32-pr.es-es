---
title: Método GetChallenge de IWMDRMNonSilentLicenseAquisition (Wmdrmsdk.h)
description: El método GetChallenge recupera el desafío de licencia que se debe publicar en el servidor de licencias.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- Método GetChallenge windows Media Format
- Método GetChallenge windows Media Format , IWMDRMNonSilentLicenseAquisition (interfaz)
- IWMDRMNonSilentLicenseAquisition interface windows Media Format , Método GetChallenge
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetChallenge
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0dc63c63e5d7a62c06cbe791d9a5e5e8d09c5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247275"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a>IWMDRMNonSilentLicenseAquisition::GetChallenge (método)

El **método GetChallenge** recupera el desafío de licencia que se debe publicar en el servidor de licencias.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbstrChallenge* \[ out\]
</dt> <dd>

Dirección de una variable que recibe el desafío de licencia.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMNonSilentLicenseAquisition (Interfaz)**](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





