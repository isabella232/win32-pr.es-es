---
description: Contiene un BLOB firmado.
ms.assetid: c12d9007-c779-4363-8e28-6387a665a0d6
title: Estructura de SIGNER_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CONTEXT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4ebc7d5380438fc6cd28a43136273387c1919713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669647"
---
# <a name="signer_context-structure"></a><span data-ttu-id="433b3-103">Estructura de \_ contexto del firmante</span><span class="sxs-lookup"><span data-stu-id="433b3-103">SIGNER\_CONTEXT structure</span></span>

<span data-ttu-id="433b3-104">La estructura de **\_ contexto del firmante** contiene un [*BLOB*](../secgloss/b-gly.md)firmado.</span><span class="sxs-lookup"><span data-stu-id="433b3-104">The **SIGNER\_CONTEXT** structure contains a signed [*BLOB*](../secgloss/b-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="433b3-105">Esta estructura no está definida en ningún archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="433b3-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="433b3-106">Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.</span><span class="sxs-lookup"><span data-stu-id="433b3-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="433b3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="433b3-107">Syntax</span></span>


```C++
typedef struct _SIGNER_CONTEXT {
  DWORD cbSize;
  DWORD cbBlob;
  BYTE  *pbBlob;
} SIGNER_CONTEXT, *PSIGNER_CONTEXT;
```



## <a name="members"></a><span data-ttu-id="433b3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="433b3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="433b3-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="433b3-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="433b3-110">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="433b3-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="433b3-111">**cbBlob**</span><span class="sxs-lookup"><span data-stu-id="433b3-111">**cbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="433b3-112">Tamaño, en bytes, del miembro **pbBlob** .</span><span class="sxs-lookup"><span data-stu-id="433b3-112">The size, in bytes, of the **pbBlob** member.</span></span>

</dd> <dt>

<span data-ttu-id="433b3-113">**pbBlob**</span><span class="sxs-lookup"><span data-stu-id="433b3-113">**pbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="433b3-114">Puntero al BLOB firmado.</span><span class="sxs-lookup"><span data-stu-id="433b3-114">A pointer to the signed BLOB.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="433b3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="433b3-115">Requirements</span></span>



| <span data-ttu-id="433b3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="433b3-116">Requirement</span></span> | <span data-ttu-id="433b3-117">Value</span><span class="sxs-lookup"><span data-stu-id="433b3-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="433b3-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="433b3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="433b3-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="433b3-119">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="433b3-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="433b3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="433b3-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="433b3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="433b3-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="433b3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="433b3-123">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="433b3-123">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="433b3-124">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="433b3-124">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
