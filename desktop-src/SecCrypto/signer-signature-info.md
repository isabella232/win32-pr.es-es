---
description: Contiene información sobre una firma digital.
ms.assetid: 0b86fdf9-533f-4640-8c70-c3c8f4ef2c68
title: Estructura de SIGNER_SIGNATURE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SIGNATURE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8e2b1fa68da51a649a01d4356ebfb1519ceeffb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277009"
---
# <a name="signer_signature_info-structure"></a><span data-ttu-id="d425b-103">Estructura de \_ información de firma de firmante \_</span><span class="sxs-lookup"><span data-stu-id="d425b-103">SIGNER\_SIGNATURE\_INFO structure</span></span>

<span data-ttu-id="d425b-104">La estructura de **\_ \_ información de firma del firmante** contiene información sobre una firma digital.</span><span class="sxs-lookup"><span data-stu-id="d425b-104">The **SIGNER\_SIGNATURE\_INFO** structure contains information about a digital signature.</span></span>

> [!Note]  
> <span data-ttu-id="d425b-105">Esta estructura no está definida en ningún archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="d425b-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="d425b-106">Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.</span><span class="sxs-lookup"><span data-stu-id="d425b-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d425b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d425b-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SIGNATURE_INFO {
  DWORD             cbSize;
  ALG_ID            algidHash;
  DWORD             dwAttrChoice;
  union {
    SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
  };
  PCRYPT_ATTRIBUTES psAuthenticated;
  PCRYPT_ATTRIBUTES psUnauthenticated;
} SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
```



## <a name="members"></a><span data-ttu-id="d425b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d425b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d425b-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="d425b-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="d425b-110">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d425b-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="d425b-111">**algidHash**</span><span class="sxs-lookup"><span data-stu-id="d425b-111">**algidHash**</span></span>
</dt> <dd>

<span data-ttu-id="d425b-112">Algoritmo hash utilizado para la firma digital.</span><span class="sxs-lookup"><span data-stu-id="d425b-112">The hash algorithm used for the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="d425b-113">**dwAttrChoice**</span><span class="sxs-lookup"><span data-stu-id="d425b-113">**dwAttrChoice**</span></span>
</dt> <dd>

<span data-ttu-id="d425b-114">Especifica si la firma tiene atributos [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d425b-114">Specifies whether the signature has [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span> <span data-ttu-id="d425b-115">Este miembro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d425b-115">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="d425b-116">Value</span><span class="sxs-lookup"><span data-stu-id="d425b-116">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="d425b-117">Significado</span><span class="sxs-lookup"><span data-stu-id="d425b-117">Meaning</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_AUTHCODE_ATTR"></span><span id="signer_authcode_attr"></span><dl> <span data-ttu-id="d425b-118"><dt>**Firmante \_ FASES \_ ATTR**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d425b-118"><dt>**SIGNER\_AUTHCODE\_ATTR**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="d425b-119">La firma tiene atributos [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d425b-119">The signature has [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span><br/>           |
| <span id="SIGNER_NO_ATTR"></span><span id="signer_no_attr"></span><dl> <span data-ttu-id="d425b-120"><dt>**Firmante \_ SIN \_ ATTR**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d425b-120"><dt>**SIGNER\_NO\_ATTR**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="d425b-121">La firma no tiene atributos [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d425b-121">The signature does not have [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d425b-122">**pAttrAuthcode**</span><span class="sxs-lookup"><span data-stu-id="d425b-122">**pAttrAuthcode**</span></span>
</dt> <dd>

<span data-ttu-id="d425b-123">Especifica los atributos de una firma [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d425b-123">Specifies attributes for an [*Authenticode*](../secgloss/a-gly.md) signature.</span></span> <span data-ttu-id="d425b-124">Este miembro es obligatorio si el valor del miembro **dwAttrChoice** es **Signer \_ fases \_ ATTR**.</span><span class="sxs-lookup"><span data-stu-id="d425b-124">This member is required if the value of the **dwAttrChoice** member is **SIGNER\_AUTHCODE\_ATTR**.</span></span>

</dd> <dt>

<span data-ttu-id="d425b-125">**psAuthenticated**</span><span class="sxs-lookup"><span data-stu-id="d425b-125">**psAuthenticated**</span></span>
</dt> <dd>

<span data-ttu-id="d425b-126">Atributos proporcionados por el usuario autenticados agregados a la firma digital.</span><span class="sxs-lookup"><span data-stu-id="d425b-126">Authenticated user-supplied attributes added to the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="d425b-127">**psUnauthenticated**</span><span class="sxs-lookup"><span data-stu-id="d425b-127">**psUnauthenticated**</span></span>
</dt> <dd>

<span data-ttu-id="d425b-128">Atributos proporcionados por el usuario no autenticados agregados a la firma digital.</span><span class="sxs-lookup"><span data-stu-id="d425b-128">Unauthenticated user-supplied attributes added to the digital signature.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d425b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d425b-129">Requirements</span></span>



| <span data-ttu-id="d425b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d425b-130">Requirement</span></span> | <span data-ttu-id="d425b-131">Value</span><span class="sxs-lookup"><span data-stu-id="d425b-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d425b-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d425b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d425b-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d425b-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d425b-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d425b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d425b-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d425b-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d425b-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="d425b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d425b-137">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="d425b-137">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="d425b-138">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="d425b-138">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
