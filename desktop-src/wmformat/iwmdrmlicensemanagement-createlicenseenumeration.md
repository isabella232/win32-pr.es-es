---
title: Método IWMDRMLicenseManagement CreateLicenseEnumeration (Wmdrmsdk.h)
description: El método CreateLicenseEnumeration crea un objeto enumerador de licencias con el que puede obtener información sobre las licencias en el almacén de licencias local.
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- Método CreateLicenseEnumeration windows Media Format
- Método CreateLicenseEnumeration windows Media Format , IWMDRMLicenseManagement (interfaz)
- IWMDRMLicenseManagement interface windows Media Format , CreateLicenseEnumeration method
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
ms.openlocfilehash: 2e442870961735d09c786a21ed1ea8be765e8f0c59b3f760278be9316daa0bb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881085"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a>IWMDRMLicenseManagement::CreateLicenseEnumeration (método)

El **método CreateLicenseEnumeration** crea un objeto enumerador de licencias con el que puede obtener información sobre las licencias en el almacén de licencias local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pLicenseFilter* \[ En\]
</dt> <dd>

Puntero a una [**estructura WMDRM \_ LICENSE \_ FILTER**](wmdrm-license-filter.md) que contiene los parámetros de filtrado de la lista de licencias del enumerador.

</dd> <dt>

*pEnumerator* \[ out\]
</dt> <dd>

Puntero que recibe la dirección de la [**interfaz IWMDRMLicense**](iwmdrmlicense.md) del objeto enumerador de licencias recién creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                | Descripción                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV \_ TOO \_ SMALL**</dt> </dl> | Se necesita una lista de revocación de contenido actualizada.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | El método se ha llevado a cabo de forma correcta.<br/>                         |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Enumeración de licencias en el almacén de licencias local**](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[**IWMDRMLicenseManagement (interfaz)**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





