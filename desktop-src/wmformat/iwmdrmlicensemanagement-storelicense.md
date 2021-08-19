---
title: Método IWMDRMLicenseManagement StoreLicense (Wmdrmsdk.h)
description: El método StoreLicense incluye una licencia que se generó fuera del subsistema DRM local en el almacén de licencias local.
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- Formato multimedia de windows del método StoreLicense
- Método StoreLicense windows Media Format , IWMDRMLicenseManagement (interfaz)
- IWMDRMLicenseManagement interfaz windows Media Format , StoreLicense (método)
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
ms.openlocfilehash: c509fdbc89acfd2d31ad5ead7ce63cd7f3b501b304d82240475c845c013e03b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655053"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a>IWMDRMLicenseManagement::StoreLicense (método)

El **método StoreLicense** incluye una licencia que se generó fuera del subsistema DRM local en el almacén de licencias local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrLicenseResponse* \[ En\]
</dt> <dd>

Cadena de respuesta de licencia que se va a descodificar y agregar al almacén de licencias local.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Puede usar este método para agregar licencias XMR que ha creado al almacén de licencias local.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMLicenseManagement (interfaz)**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





