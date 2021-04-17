---
title: Método IWMDRMLicenseManagement CreateLicenseEnumeration (wmdrmsdk. h)
description: El método CreateLicenseEnumeration crea un objeto de enumerador de licencia con el que puede obtener información sobre las licencias en el almacén de licencias local.
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- Método CreateLicenseEnumeration formato de Windows Media
- Método CreateLicenseEnumeration formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método CreateLicenseEnumeration
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb75d21cc640da39c3679ac118ead629b24f719
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718641"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a>IWMDRMLicenseManagement:: CreateLicenseEnumeration (método)

El método **CreateLicenseEnumeration** crea un objeto de enumerador de licencia con el que puede obtener información sobre las licencias en el almacén de licencias local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pLicenseFilter* \[ de\]
</dt> <dd>

Puntero a una estructura de [**\_ \_ filtro de licencias de WMDRM**](wmdrm-license-filter.md) que contiene los parámetros de filtrado para la lista de licencias en el enumerador.

</dd> <dt>

*pEnumerator* \[ enuncia\]
</dt> <dd>

Puntero que recibe la dirección de la interfaz [**IWMDRMLicense**](iwmdrmlicense.md) del objeto enumerador de licencia recién creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                | Descripción                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV \_ demasiado \_ pequeño**</dt> </dl> | Se necesita una lista de revocación de contenido actualizada.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | El método se ha llevado a cabo de forma correcta.<br/>                         |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Enumerar licencias en el almacén de licencias local**](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[**Interfaz IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





