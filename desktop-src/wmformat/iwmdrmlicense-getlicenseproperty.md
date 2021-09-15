---
title: Método IWMDRMLicense GetLicenseProperty (Wmdrmsdk.h)
description: El método GetLicenseProperty recupera una propiedad de la licencia actual.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- Método GetLicenseProperty windows Media Format
- Método GetLicenseProperty windows Media Format , interfaz IWMDRMLicense
- IWMDRMLicense interface windows Media Format , GetLicenseProperty (método)
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicenseProperty
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf7fe91c57b9c69934f093cdd504b5e6d35efb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466482"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a>IWMDRMLicense::GetLicenseProperty (Método)

El **método GetLicenseProperty** recupera una propiedad de la licencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrName* \[ En\]
</dt> <dd>

Nombre de la propiedad que se recuperará. Establezca en una de las constantes de la tabla siguiente:



| Constante                   | Descripción                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRMNet \_ Revocation | Use para obtener la lista Windows revocación de DRM multimedia para dispositivos de red para la licencia actual.                        |
| g \_ wszWMDRM \_ SAPLEVEL      | Use para obtener el nivel de Secure Audio Path (SAP) necesario para reproducir contenido cubierto por la licencia actual.                |
| g \_ wszWMDRM \_ SAPRequired   | Use para determinar si la licencia actual requiere que SAP se use para reproducir el contenido.                               |
| g \_ wszWMDRM \_ SOURCEID      | Use para obtener el identificador de origen de la licencia actual.                                                            |
| g \_ wszWMDRM \_ PRIORITY      | Use para obtener la prioridad de la licencia actual. Las licencias de prioridad más alta se aplican antes que las licencias de prioridad inferior. |
| g \_ wszWMDRM \_ UplinkID      | Use para obtener el identificador de clave de la licencia raíz en la cadena de licencias a la que pertenece la licencia actual.                  |



 

</dd> <dt>

*ppropVariant* \[ out\]
</dt> <dd>

Recibe el valor de propiedad.

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

[**GetLicense**](iwmdrmlicense-getlicense.md)
</dt> <dt>

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





