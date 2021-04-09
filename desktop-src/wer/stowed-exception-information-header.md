---
title: Estructura de STOWED_EXCEPTION_INFORMATION_HEADER
description: Contiene información que identifica la estructura primaria.
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- Estructura de STOWED_EXCEPTION_INFORMATION_HEADER Informe de errores de Windows
- PSTOWED_EXCEPTION_INFORMATION_HEADER puntero de estructura Informe de errores de Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_HEADER
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101bb1fb1555c829622a42c17fdfb01488c57636
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079680"
---
# <a name="stowed_exception_information_header-structure"></a><span data-ttu-id="e2932-105">Estructura de \_ \_ encabezado de información de excepción estibada \_</span><span class="sxs-lookup"><span data-stu-id="e2932-105">STOWED\_EXCEPTION\_INFORMATION\_HEADER structure</span></span>

<span data-ttu-id="e2932-106">Contiene información que identifica la estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="e2932-106">Contains info that identifies the parent structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2932-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2932-107">Syntax</span></span>


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a><span data-ttu-id="e2932-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e2932-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e2932-109">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="e2932-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="e2932-110">Tipo: **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e2932-110">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e2932-111">Tamaño, en bytes, de la estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="e2932-111">Size, in bytes, of the parent structure.</span></span>

</dd> <dt>

<span data-ttu-id="e2932-112">**Signature**</span><span class="sxs-lookup"><span data-stu-id="e2932-112">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="e2932-113">Tipo: **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e2932-113">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e2932-114">Valor de 32 bits que especifica la firma de la estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="e2932-114">A 32-bit value that specifies the signature of the parent structure.</span></span>



| <span data-ttu-id="e2932-115">Value</span><span class="sxs-lookup"><span data-stu-id="e2932-115">Value</span></span>                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="e2932-116">Significado</span><span class="sxs-lookup"><span data-stu-id="e2932-116">Meaning</span></span>                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> <span data-ttu-id="e2932-117"><dt>**\_ Estibada \_ \_ \_ Firma de la información de excepción v1**</dt> <dt>' SE01 '</dt></span><span class="sxs-lookup"><span data-stu-id="e2932-117"><dt>**STOWED\_EXCEPTION\_INFORMATION\_V1\_SIGNATURE**</dt> <dt>'SE01'</dt></span></span> </dl> | <span data-ttu-id="e2932-118">Este valor indica que el elemento primario es una estructura de **información de excepción de estibada \_ \_ \_ v1** .</span><span class="sxs-lookup"><span data-stu-id="e2932-118">This value indicates that the parent is a **STOWED\_EXCEPTION\_INFORMATION\_V1** structure.</span></span><br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> <span data-ttu-id="e2932-119"><dt>**\_ Estibada Firma de información de la \_ \_ versión V2 \_**</dt> <dt>' SE02 '</dt></span><span class="sxs-lookup"><span data-stu-id="e2932-119"><dt>**STOWED\_EXCEPTION\_INFORMATION\_V2\_SIGNATURE**</dt> <dt>'SE02'</dt></span></span> </dl> | <span data-ttu-id="e2932-120">Este valor indica que el elemento primario es una estructura de [**\_ información de excepción \_ \_ 2 estibada**](stowed-exception-information-v2.md) .</span><span class="sxs-lookup"><span data-stu-id="e2932-120">This value indicates that the parent is a [**STOWED\_EXCEPTION\_INFORMATION\_V2**](stowed-exception-information-v2.md) structure.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2932-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2932-121">Remarks</span></span>

<span data-ttu-id="e2932-122">[**\_ Estibada La \_ información \_ de excepción V2**](stowed-exception-information-v2.md) y el **\_ encabezado de \_ información \_ de excepción estibada** no se definen actualmente en un encabezado que está disponible públicamente, por lo que debe definirlos en el código fuente antes de usarlos.</span><span class="sxs-lookup"><span data-stu-id="e2932-122">[**STOWED\_EXCEPTION\_INFORMATION\_V2**](stowed-exception-information-v2.md) and **STOWED\_EXCEPTION\_INFORMATION\_HEADER** currently aren't defined in a header that is publicly available so you need to define them in your source code before you use them.</span></span>

<span data-ttu-id="e2932-123">La estructura V1 de la **\_ información de excepción \_ \_ estibada** es idéntica a esta estructura, salvo que no contiene los miembros **NestedExceptionType** y **NestedException** .</span><span class="sxs-lookup"><span data-stu-id="e2932-123">The **STOWED\_EXCEPTION\_INFORMATION\_V1** structure is identical to this structure except it doesn't contain the **NestedExceptionType** and **NestedException** members.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2932-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2932-124">Requirements</span></span>



| <span data-ttu-id="e2932-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2932-125">Requirement</span></span> | <span data-ttu-id="e2932-126">Value</span><span class="sxs-lookup"><span data-stu-id="e2932-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e2932-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2932-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e2932-128">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2932-128">Windows 8 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e2932-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2932-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e2932-130">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2932-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e2932-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2932-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2932-132"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="e2932-132"><dt>None</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2932-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2932-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2932-134">**Información de \_ excepción estibada \_ \_ V2**</span><span class="sxs-lookup"><span data-stu-id="e2932-134">**STOWED\_EXCEPTION\_INFORMATION\_V2**</span></span>](stowed-exception-information-v2.md)
</dt> </dl>

 

