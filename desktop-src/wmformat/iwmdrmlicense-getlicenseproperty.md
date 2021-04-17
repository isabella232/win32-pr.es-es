---
title: Método IWMDRMLicense GetLicenseProperty (wmdrmsdk. h)
description: El método GetLicenseProperty recupera una propiedad de la licencia actual.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- Método GetLicenseProperty formato de Windows Media
- Método GetLicenseProperty formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método GetLicenseProperty
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708265"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a>IWMDRMLicense:: GetLicenseProperty (método)

El método **GetLicenseProperty** recupera una propiedad de la licencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrName* \[ de\]
</dt> <dd>

Nombre de la propiedad que se va a recuperar. Establezca en una de las constantes de la tabla siguiente:



| Constante                   | Descripción                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| g \_ \_ revocación de wszWMDRMNet | Use para obtener la lista de revocación de Windows Media DRM para dispositivos de red para la licencia actual.                        |
| g \_ wszWMDRM \_ SAPLEVEL      | Use para obtener el nivel de la ruta de acceso de audio seguro (SAP) necesario para reproducir el contenido incluido en la licencia actual.                |
| g \_ wszWMDRM \_ SAPRequired   | Use para determinar si la licencia actual requiere que SAP se use para reproducir el contenido.                               |
| g \_ wszWMDRM \_ SOURCEID      | Use para obtener el identificador de origen de la licencia actual.                                                            |
| prioridad de g \_ wszWMDRM \_      | Utilice para obtener la prioridad de la licencia actual. Las licencias de prioridad más alta se aplican antes que las licencias de menor prioridad. |
| g \_ wszWMDRM \_ UplinkID      | Use para obtener el identificador de clave de la licencia raíz en la cadena de licencias a la que pertenece la licencia actual.                  |



 

</dd> <dt>

*ppropVariant* \[ enuncia\]
</dt> <dd>

Recibe el valor de la propiedad.

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

[**GetLicense**](iwmdrmlicense-getlicense.md)
</dt> <dt>

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





