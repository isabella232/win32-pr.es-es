---
title: Método IWMDRMLicenseManagement StoreLicense (wmdrmsdk. h)
description: El método StoreLicense incluye una licencia que se generó fuera del subsistema DRM local en el almacén de licencias local.
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- Método StoreLicense formato de Windows Media
- Método StoreLicense formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método StoreLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.StoreLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcfde6347e099ceb9fc168e1183cbd62c90f9b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718673"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a>IWMDRMLicenseManagement:: StoreLicense (método)

El método **StoreLicense** incluye una licencia que se generó fuera del subsistema DRM local en el almacén de licencias local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrLicenseResponse* \[ de\]
</dt> <dd>

Cadena de respuesta de licencia que se va a descodificar y agregar al almacén de licencias local.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Puede usar este método para agregar licencias de XMR que haya creado al almacén de licencias local.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





