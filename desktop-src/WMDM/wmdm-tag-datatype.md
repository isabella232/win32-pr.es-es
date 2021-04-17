---
title: Enumeración WMDM_TAG_DATATYPE
description: El \_ tipo de enumeración de tipo de datos de la etiqueta WMDM \_ define un tipo de datos.
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- Enumeración WMDM_TAG_DATATYPE Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_TAG_DATATYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad04f0d220809f6bd13d8ae29cc36d52ff6e599
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698694"
---
# <a name="wmdm_tag_datatype-enumeration"></a><span data-ttu-id="53cc7-104">\_Enumeración de tipos de tipo de texto de etiqueta WMDM \_</span><span class="sxs-lookup"><span data-stu-id="53cc7-104">WMDM\_TAG\_DATATYPE enumeration</span></span>

<span data-ttu-id="53cc7-105">El tipo de enumeración de **\_ \_ tipo** de datos de la etiqueta WMDM define un tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="53cc7-105">The **WMDM\_TAG\_DATATYPE** enumeration type defines a data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="53cc7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53cc7-106">Syntax</span></span>


```C++
typedef enum tagWMDM_TAG_DATATYPE { 
  WMDM_TYPE_DWORD,
  WMDM_TYPE_STRING,
  WMDM_TYPE_BINARY,
  WMDM_TYPE_BOOL,
  WMDM_TYPE_QWORD,
  WMDM_TYPE_WORD,
  WMDM_TYPE_GUID,
  WMDM_TYPE_DATE
} WMDM_TAG_DATATYPE;
```



## <a name="constants"></a><span data-ttu-id="53cc7-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="53cc7-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="53cc7-108"><span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="53cc7-108"><span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM\_TYPE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="53cc7-109">Especifica un valor **DWORD** de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="53cc7-109">Specifies a 4-byte **DWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="53cc7-110"><span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**\_cadena de tipo WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="53cc7-110"><span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**WMDM\_TYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="53cc7-111">Especifica una cadena Unicode terminada en null (2 bytes por carácter).</span><span class="sxs-lookup"><span data-stu-id="53cc7-111">Specifies a null-terminated Unicode string (2 bytes per character).</span></span>

</dd> <dt>

<span data-ttu-id="53cc7-112"><span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**tipo de WMDM \_ \_ binario**</span><span class="sxs-lookup"><span data-stu-id="53cc7-112"><span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**WMDM\_TYPE\_BINARY**</span></span>
</dt> <dd>

<span data-ttu-id="53cc7-113">Especifica una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="53cc7-113">Specifies an array of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="53cc7-114"><span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**WMDM \_ tipo \_ bool**</span><span class="sxs-lookup"><span data-stu-id="53cc7-114"><span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**WMDM\_TYPE\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="53cc7-115">Especifica un valor booleano de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="53cc7-115">Specifies a 4-byte Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="53cc7-116"><span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**tipo de WMDM de WMDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="53cc7-116"><span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM\_TYPE\_QWORD**</span></span>
</dt> <dd>

<span data-ttu-id="53cc7-117">Especifica un valor **QWord** de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="53cc7-117">Specifies an 8-byte **QWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="53cc7-118"><span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM \_ Escriba \_ Word**</span><span class="sxs-lookup"><span data-stu-id="53cc7-118"><span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM\_TYPE\_WORD**</span></span>
</dt> <dd>

<span data-ttu-id="53cc7-119">Especifica un valor de **palabra** de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="53cc7-119">Specifies a 2-byte **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="53cc7-120"><span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**\_GUID de tipo de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="53cc7-120"><span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**WMDM\_TYPE\_GUID**</span></span>
</dt> <dd>

<span data-ttu-id="53cc7-121">Especifica un GUID de 128 bits (16 bytes).</span><span class="sxs-lookup"><span data-stu-id="53cc7-121">Specifies a 128-bit (16-byte) GUID.</span></span>

</dd> <dt>

<span data-ttu-id="53cc7-122"><span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**\_fecha de tipo de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="53cc7-122"><span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**WMDM\_TYPE\_DATE**</span></span>
</dt> <dd>

<span data-ttu-id="53cc7-123">Especifica una fecha.</span><span class="sxs-lookup"><span data-stu-id="53cc7-123">Specifies a date.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53cc7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53cc7-124">Requirements</span></span>



| <span data-ttu-id="53cc7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="53cc7-125">Requirement</span></span> | <span data-ttu-id="53cc7-126">Value</span><span class="sxs-lookup"><span data-stu-id="53cc7-126">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="53cc7-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53cc7-127">Header</span></span><br/> | <dl> <span data-ttu-id="53cc7-128"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="53cc7-128"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53cc7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="53cc7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53cc7-130">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="53cc7-130">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





