---
title: Método IWMDRMLicenseQuery QueryLicenseState (Wmdrmsdk.h)
description: El método QueryLicenseState consulta al almacén de licencias local la información de licencia que se aplica a un identificador de clave para uno o varios derechos específicos.
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- QueryLicenseState, método windows Media Format
- Método QueryLicenseState windows Media Format , interfaz IWMDRMLicenseQuery
- IWMDRMLicenseQuery interfaz windows Media Format , método QueryLicenseState
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262135"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a>IWMDRMLicenseQuery::QueryLicenseState (método)

El **método QueryLicenseState** consulta al almacén de licencias local la información de licencia que se aplica a un identificador de clave para uno o varios derechos específicos.

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

*bstrKID* \[ En\]
</dt> <dd>

Identificador de clave para el que se va a consultar. Solo se evaluarán las licencias que se aplican a este identificador de clave.

</dd> <dt>

*cActionsToQuery* \[ En\]
</dt> <dd>

Número de acciones para las que se va a consultar. Este valor debe establecerse en el número de elementos de las matrices pasadas para los parámetros *rgbstrActionsToQuery* y *rgResultStateData.*

</dd> <dt>

*rgbstrActionsToQuery \[ \]* \[en\]
</dt> <dd>

Matriz de uno o varios derechos para los que se va a consultar. Esta matriz debe contener tantos elementos como haya especificado *cActionsToQuery.* Cada elemento debe establecerse en una de las siguientes constantes.



| Constante                                        | Descripción                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ LicenseState \_ Backup               | Incluya para consultar los detalles sobre el derecho de copia de seguridad y restauración de la licencia.                                                               |
| g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay    | Incluir para consultar los detalles sobre el derecho a compartir el contenido con un grupo de usuarios como parte de un escenario de reproducción colaborativa.          |
| g \_ wszWMDRM \_ LicenseState \_ Copy                 | Incluya para consultar los detalles sobre el derecho a copiar el contenido en dispositivos o medios externos.                                                 |
| g \_ wszWMDRM \_ LicenseState \_ CopyToCD             | Incluya para consultar los detalles sobre el derecho a copiar el contenido en CD.                                                                        |
| g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice  | Incluya para consultar los detalles sobre el derecho a copiar el contenido en un dispositivo que no admita la iniciativa de medios digitales seguros (SDMI). |
| g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice     | Incluya para consultar los detalles sobre el derecho a copiar el contenido en un dispositivo que admita sdmi.                                           |
| g \_ wszWMDRM \_ LicenseState \_ CreateThumbnailImage | Incluya para consultar los detalles sobre el derecho a crear una imagen en miniatura a partir del contenido.                                                     |
| g \_ wszWMDRM \_ LicenseState \_ Playback             | Incluya para consultar los detalles sobre el derecho a reproducir el contenido.                                                                              |
| g \_ wszWMDRM LicenseState Playlist Playlist Playlist (Lista de reproducción de wszWMDRM \_ \_ LicenseState)         | Incluya para consultar los detalles sobre el derecho a copiar el contenido en CD como parte de una lista de reproducción.                                                  |



 

</dd> <dt>

*rgResultStateData \[ \]* \[out\]
</dt> <dd>

Matriz de una o varias estructuras [**DRM \_ LICENSE STATE \_ \_ DATA**](drmdrm-license-state-data.md) que reciben la información de estado de licencia que se aplica a la derecha en el elemento correspondiente del *parámetro rgbstrActionsToQuery.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Se buscarán y evaluarán todas las licencias que se aplican al identificador de clave especificado. Los resultados se agregan, por lo que cada **estructura DRM LICENSE STATE \_ \_ \_ DATA** puede contener información de varias licencias.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMDRMLicenseQuery (interfaz)**](iwmdrmlicensequery.md)
</dt> </dl>

 

 





