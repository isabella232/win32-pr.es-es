---
description: Especifica el firmante que se va a firmar.
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: Estructura de SIGNER_SUBJECT_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SUBJECT_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b5d780e50f8ea10fcf68cc90ae7092bbc2c473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666981"
---
# <a name="signer_subject_info-structure"></a><span data-ttu-id="3773f-103">Estructura de \_ información de asunto del firmante \_</span><span class="sxs-lookup"><span data-stu-id="3773f-103">SIGNER\_SUBJECT\_INFO structure</span></span>

<span data-ttu-id="3773f-104">La estructura de **\_ \_ información de asunto del firmante** especifica el firmante que se va a firmar.</span><span class="sxs-lookup"><span data-stu-id="3773f-104">The **SIGNER\_SUBJECT\_INFO** structure specifies a subject to sign.</span></span>

> [!Note]  
> <span data-ttu-id="3773f-105">Esta estructura no está definida en ningún archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="3773f-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="3773f-106">Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.</span><span class="sxs-lookup"><span data-stu-id="3773f-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3773f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3773f-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SUBJECT_INFO {
  DWORD cbSize;
  DWORD *pdwIndex;
  DWORD dwSubjectChoice;
  union {
    SIGNER_FILE_INFO *pSignerFileInfo;
    SIGNER_BLOB_INFO *pSignerBlobInfo;
  };
} SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
```



## <a name="members"></a><span data-ttu-id="3773f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3773f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3773f-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="3773f-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="3773f-110">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="3773f-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="3773f-111">**pdwIndex**</span><span class="sxs-lookup"><span data-stu-id="3773f-111">**pdwIndex**</span></span>
</dt> <dd>

<span data-ttu-id="3773f-112">Este miembro está reservado.</span><span class="sxs-lookup"><span data-stu-id="3773f-112">This member is reserved.</span></span> <span data-ttu-id="3773f-113">Debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="3773f-113">It must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="3773f-114">**dwSubjectChoice**</span><span class="sxs-lookup"><span data-stu-id="3773f-114">**dwSubjectChoice**</span></span>
</dt> <dd>

<span data-ttu-id="3773f-115">Especifica si el sujeto es un archivo o un [*BLOB*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3773f-115">Specifies whether the subject is a file or a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="3773f-116">Este miembro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3773f-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="3773f-117">Value</span><span class="sxs-lookup"><span data-stu-id="3773f-117">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="3773f-118">Significado</span><span class="sxs-lookup"><span data-stu-id="3773f-118">Meaning</span></span>                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <span data-ttu-id="3773f-119"><dt>**Firmante \_ \_BLOB de asunto**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="3773f-119"><dt>**SIGNER\_SUBJECT\_BLOB**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="3773f-120">El asunto es un BLOB.</span><span class="sxs-lookup"><span data-stu-id="3773f-120">The subject is a BLOB.</span></span><br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <span data-ttu-id="3773f-121"><dt>**Firmante \_ \_Archivo de asunto**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="3773f-121"><dt>**SIGNER\_SUBJECT\_FILE**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="3773f-122">El asunto es un archivo.</span><span class="sxs-lookup"><span data-stu-id="3773f-122">The subject is a file.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3773f-123">**pSignerFileInfo**</span><span class="sxs-lookup"><span data-stu-id="3773f-123">**pSignerFileInfo**</span></span>
</dt> <dd>

<span data-ttu-id="3773f-124">Puntero a una estructura de [**\_ \_ información del archivo del firmante**](signer-file-info.md) que especifica el archivo que se va a firmar.</span><span class="sxs-lookup"><span data-stu-id="3773f-124">A pointer to a [**SIGNER\_FILE\_INFO**](signer-file-info.md) structure that specifies the file to sign.</span></span>

</dd> <dt>

<span data-ttu-id="3773f-125">**pSignerBlobInfo**</span><span class="sxs-lookup"><span data-stu-id="3773f-125">**pSignerBlobInfo**</span></span>
</dt> <dd>

<span data-ttu-id="3773f-126">Puntero a una estructura de [**\_ \_ información del BLOB del firmante**](signer-blob-info.md) que especifica el BLOB que se va a firmar.</span><span class="sxs-lookup"><span data-stu-id="3773f-126">A pointer to a [**SIGNER\_BLOB\_INFO**](signer-blob-info.md) structure that specifies the BLOB to sign.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3773f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3773f-127">Requirements</span></span>



| <span data-ttu-id="3773f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3773f-128">Requirement</span></span> | <span data-ttu-id="3773f-129">Value</span><span class="sxs-lookup"><span data-stu-id="3773f-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3773f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3773f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3773f-131">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3773f-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3773f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3773f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3773f-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3773f-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3773f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3773f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3773f-135">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="3773f-135">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="3773f-136">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="3773f-136">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
