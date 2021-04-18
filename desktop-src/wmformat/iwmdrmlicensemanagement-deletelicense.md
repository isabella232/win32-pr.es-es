---
title: Método IWMDRMLicenseManagement DeleteLicense (wmdrmsdk. h)
description: El método DeleteLicense quita una licencia del almacén de licencias local temporal.
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- Método DeleteLicense formato de Windows Media
- Método DeleteLicense formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método DeleteLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.DeleteLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d5b52f6277459f147285f46fc791669e56061a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718803"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a>IWMDRMLicenseManagement::D método eleteLicense

El método **DeleteLicense** quita una licencia del almacén de licencias local temporal.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrKID* \[ de\]
</dt> <dd>

IDENTIFICADOR de clave (KID) de la licencia que se va a eliminar.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Marcas de opciones de eliminación de licencias. Establezca en uno de los valores de la tabla siguiente.



| Value                                    | Descripción                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| la \_ licencia de eliminación de WMDRM \_ \_ inmediatamente      | Especifica que la licencia se debe quitar del almacén de inmediato.                                                                                                                              |
| \_ \_ \_ marca \_ de eliminación de licencia de WMDRM para \_ purgar | Especifica que la licencia debe marcarse para su eliminación, pero no debe quitarse del almacén hasta que se llame al método [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) . |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                            | Descripción                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | El método se ha llevado a cabo de forma correcta.<br/>                                                                                    |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | La licencia especificada no existe en el almacén.<br/> O bien<br/> No se encontró el almacén.<br/> |



 

## <a name="remarks"></a>Observaciones

Para eliminar licencias del almacén de licencias local permanente, debe usar la revocación de licencias.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





