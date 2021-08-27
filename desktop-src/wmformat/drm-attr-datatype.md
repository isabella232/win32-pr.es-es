---
title: DRM_ATTR_DATATYPE enumeración (Wmdrmsdk.h)
description: La \_ enumeración \_ DATATYPE DE ATTR de DRM define los tipos de datos usados para los atributos y propiedades de DRM.
ms.assetid: ccad16e2-475d-4cc7-b773-f17038d2754a
keywords:
- DRM_ATTR_DATATYPE enumeración windows Media Format
- enumeración windows Media Format
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
ms.openlocfilehash: 09f55c3d218aa86c33f699d4cb762e752a0bf4e1029e8ca42eee797aaf8ac721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110535"
---
# <a name="drm_attr_datatype-enumeration"></a>Enumeración \_ DATATYPE de ATTR de DRM \_

La **\_ enumeración \_ DATATYPE DE ATTR de DRM** define los tipos de datos usados para los atributos y propiedades de DRM.

## <a name="syntax"></a>Syntax


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

<span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**DRM \_ TYPE \_ DWORD**
</dt> <dd>

La propiedad es un valor **DWORD** de 4 bytes.

</dd> <dt>

<span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**CADENA \_ DE TIPO \_ DRM**
</dt> <dd>

La propiedad es una cadena Unicode terminada en NULL.

</dd> <dt>

<span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**DRM \_ TYPE \_ BINARY**
</dt> <dd>

La propiedad es una matriz de bytes.

</dd> <dt>

<span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**DRM \_ TYPE \_ BOOL**
</dt> <dd>

La propiedad es un valor booleano de 4 bytes.

</dd> <dt>

<span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**TIPO DRM \_ \_ QWORD**
</dt> <dd>

La propiedad es un valor **QWORD** de 8 bytes.

</dd> <dt>

<span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**PALABRA \_ DE TIPO \_ DRM**
</dt> <dd>

La propiedad es un valor **WORD** de 2 bytes.

</dd> <dt>

<span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**GUID \_ DE TIPO \_ DRM**
</dt> <dd>

La propiedad es un valor GUID de 128 bits (6 bytes).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> </dl>

 

 





