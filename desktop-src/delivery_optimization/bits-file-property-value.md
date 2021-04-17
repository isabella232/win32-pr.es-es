---
title: BITS_FILE_PROPERTY_VALUE estructura (Deliveryoptimization. h)
description: La Unión BITS_FILE_PROPERTY_VALUE proporciona el valor de propiedad del archivo DO basado en un valor de la enumeración BITS_FILE_PROPERTY_ID.
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- Estructura de BITS_FILE_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 639ea0523c5b92d9764671cb573497223ef968fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714549"
---
# <a name="bits_file_property_value-structure"></a><span data-ttu-id="6de18-104">Estructura de BITS_FILE_PROPERTY_VALUE</span><span class="sxs-lookup"><span data-stu-id="6de18-104">BITS_FILE_PROPERTY_VALUE structure</span></span>

<span data-ttu-id="6de18-105">La Unión **BITS_FILE_PROPERTY_VALUE** proporciona el valor de propiedad del archivo do basado en un valor de la enumeración [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) .</span><span class="sxs-lookup"><span data-stu-id="6de18-105">The **BITS_FILE_PROPERTY_VALUE** union provides the property value of the DO file based on a value from the [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="6de18-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6de18-106">Syntax</span></span>


```C++
typedef struct {
  LPWSTR String;
} BITS_FILE_PROPERTY_VALUE;
```



## <a name="members"></a><span data-ttu-id="6de18-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6de18-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6de18-108">**String**</span><span class="sxs-lookup"><span data-stu-id="6de18-108">**String**</span></span>
</dt> <dd>

<span data-ttu-id="6de18-109">Este valor se usa cuando se usa el valor de enumeración de ID. de propiedad **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.</span><span class="sxs-lookup"><span data-stu-id="6de18-109">This value is used when using the property ID enum value **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6de18-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6de18-110">Requirements</span></span>



| <span data-ttu-id="6de18-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="6de18-111">Requirement</span></span> | <span data-ttu-id="6de18-112">Value</span><span class="sxs-lookup"><span data-stu-id="6de18-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de18-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6de18-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6de18-114">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="6de18-114">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6de18-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6de18-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6de18-116">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="6de18-116">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6de18-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6de18-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="6de18-118"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="6de18-118"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de18-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="6de18-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de18-120">**BITS_FILE_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="6de18-120">**BITS_FILE_PROPERTY_ID**</span></span>](bits-file-property-id-.md)
</dt> <dt>

[<span data-ttu-id="6de18-121">**IBackgroundCopyFile5. GetProperty**</span><span class="sxs-lookup"><span data-stu-id="6de18-121">**IBackgroundCopyFile5.GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[<span data-ttu-id="6de18-122">**IBackgroundCopyFile5. SetProperty**</span><span class="sxs-lookup"><span data-stu-id="6de18-122">**IBackgroundCopyFile5.SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





