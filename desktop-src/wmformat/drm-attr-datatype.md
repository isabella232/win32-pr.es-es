---
title: Enumeración DRM_ATTR_DATATYPE (wmdrmsdk. h)
description: La \_ \_ enumeración del tipo de datos DRM ATTR define los tipos de datos utilizados para los atributos y propiedades de DRM.
ms.assetid: ccad16e2-475d-4cc7-b773-f17038d2754a
keywords:
- DRM_ATTR_DATATYPE enumeración formato de Windows Media
- enumeración Windows Media Format
topic_type:
- apiref
api_name:
- DRM_ATTR_DATATYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e684ba1c09a86c65a13adbd189bb185f65598b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709166"
---
# <a name="drm_attr_datatype-enumeration"></a>\_ \_ Enumeración de tipos de tipo de texto DRM ATTR

La enumeración del **\_ \_ tipo de datos DRM ATTR** define los tipos de datos utilizados para los atributos y propiedades de DRM.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum DRM_ATTR_DATATYPE { 
  DRM_TYPE_DWORD   = 0,
  DRM_TYPE_STRING  = 1,
  DRM_TYPE_BINARY  = 2,
  DRM_TYPE_BOOL    = 3,
  DRM_TYPE_QWORD   = 4,
  DRM_TYPE_WORD    = 5,
  DRM_TYPE_GUID    = 6
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**tipo de DRM \_ \_ DWORD**
</dt> <dd>

La propiedad es un valor **DWORD** de 4 bytes.

</dd> <dt>

<span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**\_cadena de tipo DRM \_**
</dt> <dd>

La propiedad es una cadena Unicode terminada en NULL.

</dd> <dt>

<span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**tipo de DRM \_ \_ binario**
</dt> <dd>

La propiedad es una matriz de bytes.

</dd> <dt>

<span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**tipo de DRM \_ \_ bool**
</dt> <dd>

La propiedad es un valor booleano de 4 bytes.

</dd> <dt>

<span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**tipo de DRM \_ \_ QWord**
</dt> <dd>

La propiedad es un valor **QWord** de 8 bytes.

</dd> <dt>

<span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**tipo DRM de \_ \_ Word**
</dt> <dd>

La propiedad es un valor de **palabra** de 2 bytes.

</dd> <dt>

<span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**\_GUID de tipo DRM \_**
</dt> <dd>

La propiedad es un valor de GUID de 128 bits (6 bytes).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> </dl>

 

 





