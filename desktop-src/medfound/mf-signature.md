---
description: Contiene una firma de lista de revocación global (GRL).
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: Estructura de MF_SIGNATURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_SIGNATURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4827fea8e4259609cbb54f2b58a3d1c88ad6c23e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278923"
---
# <a name="mf_signature-structure"></a><span data-ttu-id="6ffa9-103">\_Estructura de firma MF</span><span class="sxs-lookup"><span data-stu-id="6ffa9-103">MF\_SIGNATURE structure</span></span>

<span data-ttu-id="6ffa9-104">Contiene una firma de lista de revocación global (GRL).</span><span class="sxs-lookup"><span data-stu-id="6ffa9-104">Contains a global revocation list (GRL) signature.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ffa9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ffa9-105">Syntax</span></span>


```C++
typedef struct _MF_SIGNATURE {
  DWORD dwSignVer;
  DWORD cbSign;
  BYTE  rgSign[1];
} MF_SIGNATURE;
```



## <a name="members"></a><span data-ttu-id="6ffa9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ffa9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6ffa9-107">**dwSignVer**</span><span class="sxs-lookup"><span data-stu-id="6ffa9-107">**dwSignVer**</span></span>
</dt> <dd>

<span data-ttu-id="6ffa9-108">Número de versión de la firma.</span><span class="sxs-lookup"><span data-stu-id="6ffa9-108">The signature version number.</span></span>

</dd> <dt>

<span data-ttu-id="6ffa9-109">**cbSign**</span><span class="sxs-lookup"><span data-stu-id="6ffa9-109">**cbSign**</span></span>
</dt> <dd>

<span data-ttu-id="6ffa9-110">Tamaño de la firma en bytes.</span><span class="sxs-lookup"><span data-stu-id="6ffa9-110">The size of the signature in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6ffa9-111">**rgSign**</span><span class="sxs-lookup"><span data-stu-id="6ffa9-111">**rgSign**</span></span>
</dt> <dd>

<span data-ttu-id="6ffa9-112">Matriz de bytes de tamaño **cbSign** que contiene la firma.</span><span class="sxs-lookup"><span data-stu-id="6ffa9-112">A byte array of size **cbSign** that contains the signature.</span></span> <span data-ttu-id="6ffa9-113">El tamaño real de la matriz es mayor que el tamaño especificado en la declaración de la estructura.</span><span class="sxs-lookup"><span data-stu-id="6ffa9-113">The actual array size is larger than the size given in the structure declaration.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ffa9-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ffa9-114">Remarks</span></span>

<span data-ttu-id="6ffa9-115">Esta estructura no se declara en un encabezado de SDK.</span><span class="sxs-lookup"><span data-stu-id="6ffa9-115">This structure is not declared in an SDK header.</span></span> <span data-ttu-id="6ffa9-116">Para usar esta estructura, agregue la declaración que se muestra aquí al código fuente.</span><span class="sxs-lookup"><span data-stu-id="6ffa9-116">To use this structure, add the declaration shown here to your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ffa9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ffa9-117">Requirements</span></span>



| <span data-ttu-id="6ffa9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ffa9-118">Requirement</span></span> | <span data-ttu-id="6ffa9-119">Value</span><span class="sxs-lookup"><span data-stu-id="6ffa9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6ffa9-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ffa9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6ffa9-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6ffa9-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6ffa9-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ffa9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6ffa9-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ffa9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ffa9-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ffa9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ffa9-125">Revocación de certificados OPM</span><span class="sxs-lookup"><span data-stu-id="6ffa9-125">OPM Certificate Revocation</span></span>](opm-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="6ffa9-126">Estructuras OPM</span><span class="sxs-lookup"><span data-stu-id="6ffa9-126">OPM Structures</span></span>](opm-structures.md)
</dt> </dl>

 

 




