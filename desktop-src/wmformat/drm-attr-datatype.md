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
# <a name="drm_attr_datatype-enumeration"></a><span data-ttu-id="f4e1d-105">\_ \_ Enumeración de tipos de tipo de texto DRM ATTR</span><span class="sxs-lookup"><span data-stu-id="f4e1d-105">DRM\_ATTR\_DATATYPE enumeration</span></span>

<span data-ttu-id="f4e1d-106">La enumeración del **\_ \_ tipo de datos DRM ATTR** define los tipos de datos utilizados para los atributos y propiedades de DRM.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-106">The **DRM\_ATTR\_DATATYPE** enumeration defines the data types used for DRM attributes and properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4e1d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4e1d-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="f4e1d-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="f4e1d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f4e1d-109"><span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**tipo de DRM \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f4e1d-109"><span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**DRM\_TYPE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f4e1d-110">La propiedad es un valor **DWORD** de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-110">The property is a 4-byte **DWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="f4e1d-111"><span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**\_cadena de tipo DRM \_**</span><span class="sxs-lookup"><span data-stu-id="f4e1d-111"><span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**DRM\_TYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="f4e1d-112">La propiedad es una cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-112">The property is a null-terminated Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="f4e1d-113"><span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**tipo de DRM \_ \_ binario**</span><span class="sxs-lookup"><span data-stu-id="f4e1d-113"><span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**DRM\_TYPE\_BINARY**</span></span>
</dt> <dd>

<span data-ttu-id="f4e1d-114">La propiedad es una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-114">The property is an array of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f4e1d-115"><span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**tipo de DRM \_ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="f4e1d-115"><span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**DRM\_TYPE\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="f4e1d-116">La propiedad es un valor booleano de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-116">The property is a 4-byte Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="f4e1d-117"><span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**tipo de DRM \_ \_ QWord**</span><span class="sxs-lookup"><span data-stu-id="f4e1d-117"><span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**DRM\_TYPE\_QWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f4e1d-118">La propiedad es un valor **QWord** de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-118">The property is an 8-byte **QWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="f4e1d-119"><span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**tipo DRM de \_ \_ Word**</span><span class="sxs-lookup"><span data-stu-id="f4e1d-119"><span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**DRM\_TYPE\_WORD**</span></span>
</dt> <dd>

<span data-ttu-id="f4e1d-120">La propiedad es un valor de **palabra** de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-120">The property is a 2-byte **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="f4e1d-121"><span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**\_GUID de tipo DRM \_**</span><span class="sxs-lookup"><span data-stu-id="f4e1d-121"><span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**DRM\_TYPE\_GUID**</span></span>
</dt> <dd>

<span data-ttu-id="f4e1d-122">La propiedad es un valor de GUID de 128 bits (6 bytes).</span><span class="sxs-lookup"><span data-stu-id="f4e1d-122">The property is a 128-bit (6-byte) GUID value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4e1d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4e1d-123">Requirements</span></span>



| <span data-ttu-id="f4e1d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4e1d-124">Requirement</span></span> | <span data-ttu-id="f4e1d-125">Value</span><span class="sxs-lookup"><span data-stu-id="f4e1d-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e1d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4e1d-126">Header</span></span><br/> | <dl> <span data-ttu-id="f4e1d-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4e1d-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4e1d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4e1d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e1d-129">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="f4e1d-129">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





