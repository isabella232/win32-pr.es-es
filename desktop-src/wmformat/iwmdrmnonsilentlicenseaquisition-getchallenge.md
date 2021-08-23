---
title: Método IWMDRMNonSilentLicenseAquisition GetChallenge (Wmdrmsdk.h)
description: El método GetChallenge recupera el desafío de licencia que se debe publicar en el servidor de licencias.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- Método GetChallenge windows Media Format
- Método GetChallenge windows Media Format , interfaz IWMDRMNonSilentLicenseAquisition
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
ms.openlocfilehash: cf495652033bdb5201f2b4e5bd9dc1d6a222cc3ebdf4ec6438fe391ed06fac85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027523"
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

[**Interfaz IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





