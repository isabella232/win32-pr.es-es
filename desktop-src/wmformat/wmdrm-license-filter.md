---
title: WMDRM_LICENSE_FILTER estructura (wmdrmsdk. h)
description: La \_ estructura del \_ filtro de licencias de WMDRM define los parámetros de filtrado para su uso al crear una enumeración de licencias.
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- WMDRM_LICENSE_FILTER estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRM_LICENSE_FILTER
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200bea0d74b7c9a84c5731072e2e65bca81b6cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699526"
---
# <a name="wmdrm_license_filter-structure"></a>Estructura del filtro de \_ licencias de WMDRM \_

La estructura del **\_ \_ filtro de licencias de WMDRM** define los parámetros de filtrado para su uso al crear una enumeración de licencias.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRM_LICENSE_FILTER {
  DWORD dwVersion;
  BSTR  bstrKID;
  BSTR  bstrRights;
  BSTR  bstrAllowedSourceIDs;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwVersion**
</dt> <dd>

Especifica un número de versión mínimo para las licencias devueltas.

</dd> <dt>

**bstrKID**
</dt> <dd>

Especifica un identificador de clave para el que filtrar licencias. Solo se incluirán en la enumeración las licencias con el identificador de clave especificado.

</dd> <dt>

**bstrRights**
</dt> <dd>

Especifica un conjunto de derechos para filtrar licencias. En la enumeración solo se incluirán las licencias que proporcionen todos los derechos especificados.

</dd> <dt>

**bstrAllowedSourceIDs**
</dt> <dd>

Especifica los orígenes de contenido protegido que se incluirán en la búsqueda de licencias.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El método [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) usa esta estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





