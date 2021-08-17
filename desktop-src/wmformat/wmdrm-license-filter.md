---
title: WMDRM_LICENSE_FILTER estructura (Wmdrmsdk.h)
description: La estructura WMDRM \_ LICENSE FILTER define parámetros de filtrado para su uso al crear una \_ enumeración de licencias.
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- WMDRM_LICENSE_FILTER windows Media Format de estructura
- estructura windows Formato multimedia
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
ms.openlocfilehash: 94dc65758c7c5a25d31dd9fdb2d0fcd5cfa65debfff3defab4b88280a5ff3b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698150"
---
# <a name="wmdrm_license_filter-structure"></a>Estructura DE FILTRO \_ DE LICENCIA DE WMDRM \_

La **estructura WMDRM \_ LICENSE \_ FILTER** define parámetros de filtrado para su uso al crear una enumeración de licencias.

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

Especifica un identificador de clave para el que filtrar las licencias. En la enumeración solo se incluirán las licencias con el identificador de clave especificado.

</dd> <dt>

**bstrRights**
</dt> <dd>

Especifica un conjunto de derechos para filtrar licencias. Solo se incluirán en la enumeración las licencias que proporcionan todos los derechos especificados.

</dd> <dt>

**bstrAllowedSourceIDs**
</dt> <dd>

Especifica los orígenes de contenido protegido que se incluirán en la búsqueda de licencias.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El método [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) usa esta estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





