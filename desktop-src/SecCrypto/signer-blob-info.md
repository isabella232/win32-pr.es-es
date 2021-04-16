---
description: Especifica un BLOB que se va a firmar.
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: Estructura de SIGNER_BLOB_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_BLOB_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: a05e99cc4d7fa2eff196159bb449fa7dbfbf3026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547078"
---
# <a name="signer_blob_info-structure"></a><span data-ttu-id="18176-103">Estructura de \_ información del BLOB del firmante \_</span><span class="sxs-lookup"><span data-stu-id="18176-103">SIGNER\_BLOB\_INFO structure</span></span>

<span data-ttu-id="18176-104">\[La estructura de **\_ \_ información del BLOB del firmante** está disponible para su uso en los sistemas operativos especificados en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="18176-104">\[The **SIGNER\_BLOB\_INFO** structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="18176-105">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="18176-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="18176-106">La estructura de **\_ \_ información del BLOB del firmante** especifica el [*BLOB*](../secgloss/b-gly.md) que se va a firmar.</span><span class="sxs-lookup"><span data-stu-id="18176-106">The **SIGNER\_BLOB\_INFO** structure specifies a [*BLOB*](../secgloss/b-gly.md) to sign.</span></span>

> [!Note]  
> <span data-ttu-id="18176-107">Esta estructura no está definida en ningún archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="18176-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="18176-108">Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.</span><span class="sxs-lookup"><span data-stu-id="18176-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="18176-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18176-109">Syntax</span></span>


```C++
typedef struct _SIGNER_BLOB_INFO {
  DWORD   cbSize;
  GUID    *pGuidSubject;
  DWORD   cbBlob;
  BYTE    *pbBlob;
  LPCWSTR pwszDisplayName;
} SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
```



## <a name="members"></a><span data-ttu-id="18176-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="18176-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="18176-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="18176-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="18176-112">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="18176-112">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="18176-113">**pGuidSubject**</span><span class="sxs-lookup"><span data-stu-id="18176-113">**pGuidSubject**</span></span>
</dt> <dd>

<span data-ttu-id="18176-114">Un puntero a un **GUID** que especifica el paquete de interfaz de sujeto (SIP) que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="18176-114">A pointer to a **GUID** that specifies the Subject Interface Package (SIP) to load.</span></span>

</dd> <dt>

<span data-ttu-id="18176-115">**cbBlob**</span><span class="sxs-lookup"><span data-stu-id="18176-115">**cbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="18176-116">Tamaño, en bytes, del BLOB que se va a firmar.</span><span class="sxs-lookup"><span data-stu-id="18176-116">The size, in bytes, of the BLOB to sign.</span></span>

</dd> <dt>

<span data-ttu-id="18176-117">**pbBlob**</span><span class="sxs-lookup"><span data-stu-id="18176-117">**pbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="18176-118">Puntero al BLOB que se va a firmar.</span><span class="sxs-lookup"><span data-stu-id="18176-118">A pointer to the BLOB to sign.</span></span>

</dd> <dt>

<span data-ttu-id="18176-119">**pwszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="18176-119">**pwszDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="18176-120">Nombre para mostrar del BLOB.</span><span class="sxs-lookup"><span data-stu-id="18176-120">The display name of the BLOB.</span></span> <span data-ttu-id="18176-121">Este miembro se puede establecer en **null**.</span><span class="sxs-lookup"><span data-stu-id="18176-121">This member can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18176-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18176-122">Requirements</span></span>



| <span data-ttu-id="18176-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="18176-123">Requirement</span></span> | <span data-ttu-id="18176-124">Value</span><span class="sxs-lookup"><span data-stu-id="18176-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="18176-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18176-125">Minimum supported client</span></span><br/> | <span data-ttu-id="18176-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="18176-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="18176-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18176-127">Minimum supported server</span></span><br/> | <span data-ttu-id="18176-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="18176-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="18176-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="18176-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18176-130">**información de \_ asunto del firmante \_**</span><span class="sxs-lookup"><span data-stu-id="18176-130">**SIGNER\_SUBJECT\_INFO**</span></span>](signer-subject-info.md)
</dt> </dl>

 

 
