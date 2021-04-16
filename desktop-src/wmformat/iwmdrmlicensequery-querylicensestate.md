---
title: Método IWMDRMLicenseQuery QueryLicenseState (wmdrmsdk. h)
description: El método QueryLicenseState consulta el almacén de licencias local para obtener la información de licencia que se aplica a un identificador de clave para uno o más derechos específicos.
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- Método QueryLicenseState formato de Windows Media
- Método QueryLicenseState formato de Windows Media, interfaz IWMDRMLicenseQuery
- Interfaz IWMDRMLicenseQuery formato de Windows Media, método QueryLicenseState
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryLicenseState
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e101d4ad9b5405906d05ba5e5f230326a1a3f13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699338"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a>IWMDRMLicenseQuery:: QueryLicenseState (método)

El método **QueryLicenseState** consulta el almacén de licencias local para obtener la información de licencia que se aplica a un identificador de clave para uno o más derechos específicos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryLicenseState(
  [in]  BSTR                   bstrKID,
  [in]  DWORD                  cActionsToQuery,
  [in]  BSTR                   rgbstrActionsToQuery[],
  [out] DRM_LICENSE_STATE_DATA rgResultStateData[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrKID* \[ de\]
</dt> <dd>

IDENTIFICADOR de clave que se va a consultar. Solo se evaluarán las licencias que se apliquen a este ID. de clave.

</dd> <dt>

*cActionsToQuery* \[ de\]
</dt> <dd>

Número de acciones que se van a consultar. Este valor debe establecerse en el número de elementos de las matrices que se pasan para los parámetros *rgbstrActionsToQuery* y *rgResultStateData* .

</dd> <dt>

*\[ rgbstrActionsToQuery \]* \[en\]
</dt> <dd>

Matriz de uno o más derechos que se van a consultar. Esta matriz debe contener tantos elementos como especifique el *cActionsToQuery*. Cada elemento debe establecerse en una de las siguientes constantes.



| Constante                                        | Descripción                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ LicenseState \_ backup               | Incluir para consultar los detalles sobre el derecho a realizar una copia de seguridad y restaurar la licencia.                                                               |
| g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay    | Incluir para consultar los detalles sobre el derecho a compartir el contenido con un grupo de usuarios como parte de un escenario de reproducción colaborativa.          |
| g \_ wszWMDRM \_ LicenseState \_                 | Incluir para consultar los detalles sobre el derecho a copiar el contenido en dispositivos o medios externos.                                                 |
| g \_ wszWMDRM \_ LicenseState \_ CopyToCD             | Incluir para consultar los detalles sobre la derecha para copiar el contenido en un CD.                                                                        |
| g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice  | Incluir para consultar los detalles sobre la derecha para copiar el contenido en un dispositivo que no admita la iniciativa de medios digitales seguros (SDMI). |
| g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice     | Incluir para consultar los detalles sobre la derecha para copiar el contenido en un dispositivo compatible con SDMI.                                           |
| g \_ wszWMDRM \_ LicenseState \_ CreateThumbnailImage | Incluir para consultar los detalles sobre la derecha para crear una imagen en miniatura a partir del contenido.                                                     |
| g \_ wszWMDRM \_ LicenseState \_ reproducción             | Incluir para consultar los detalles sobre el derecho a reproducir el contenido.                                                                              |
| g \_ wszWMDRM \_ LicenseState \_ PlaylistBurn         | Incluir para consultar los detalles sobre la derecha para copiar el contenido en CD como parte de una lista de reproducción.                                                  |



 

</dd> <dt>

*\[ rgResultStateData \]* \[fuera de\]
</dt> <dd>

Matriz de una o varias estructuras de datos de estado de la [**\_ licencia \_ \_ DRM**](drmdrm-license-state-data.md) que reciben la información de estado de la licencia que se aplica a la derecha en el elemento correspondiente del parámetro *rgbstrActionsToQuery* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Se buscarán y evaluarán todas las licencias que se aplican al identificador de clave especificado. Los resultados se agregan, por lo que cada estructura de **\_ datos de \_ estado \_ de licencia DRM** puede contener información de varias licencias.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> </dl>

 

 





