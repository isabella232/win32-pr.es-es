---
title: Método IWMDRMLicenseManagement DeleteLicense (Wmdrmsdk.h)
description: El método DeleteLicense quita una licencia del almacén de licencias local temporal.
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- Método DeleteLicense windows Media Format
- Método DeleteLicense windows Media Format , IWMDRMLicenseManagement (interfaz)
- IWMDRMLicenseManagement interface windows Media Format , DeleteLicense method
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
ms.openlocfilehash: 977f7eaef1d6c8a505ce55d7d1683d7c9f4dabff5e59df7d8845773eefdff696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707945"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a>IWMDRMLicenseManagement::D eleteLicense (método)

El **método DeleteLicense** quita una licencia del almacén de licencias local temporal.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrKID* \[ En\]
</dt> <dd>

Identificador de clave (KID) de la licencia que se va a eliminar.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Marcas de opciones de eliminación de licencias. Establezca en uno de los valores de la tabla siguiente.



| Value                                    | Descripción                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ELIMINACIÓN DE LICENCIA DE WMDRM \_ \_ \_ INMEDIATAMENTE      | Especifica que la licencia se debe quitar de la tienda inmediatamente.                                                                                                                              |
| WMDRM \_ DELETE \_ LICENSE \_ MARK \_ FOR \_ PURGE | Especifica que la licencia debe marcarse para su eliminación, pero no debe quitarse del almacén hasta que se llame al método [**CleanLicenseStore.**](iwmdrmlicensemanagement-cleanlicensestore.md) |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                            | Descripción                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | El método se ha llevado a cabo de forma correcta.<br/>                                                                                    |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | La licencia especificada no existe en el almacén.<br/> O bien<br/> No se encontró el almacén.<br/> |



 

## <a name="remarks"></a>Comentarios

Para eliminar licencias del almacén de licencias local permanente, debe usar la revocación de licencias.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMLicenseManagement (interfaz)**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





