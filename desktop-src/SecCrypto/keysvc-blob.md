---
description: La \_ estructura de blobs KEYSVC define un BLOB de servicio de claves. La función RKeyPFXInstall usa esta estructura.
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: KEYSVC_BLOB estructura (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_BLOB
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 801be5f5a0d431f488da6e13e1f3082d147c5974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669887"
---
# <a name="keysvc_blob-structure"></a><span data-ttu-id="ff6cd-104">KEYSVC \_ estructura de BLOB</span><span class="sxs-lookup"><span data-stu-id="ff6cd-104">KEYSVC\_BLOB structure</span></span>

<span data-ttu-id="ff6cd-105">La estructura de **\_ blobs KEYSVC** define un BLOB de servicio de claves.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-105">The **KEYSVC\_BLOB** structure defines a key service BLOB.</span></span> <span data-ttu-id="ff6cd-106">La función [**RKeyPFXInstall**](rkeypfxinstall.md) usa esta estructura.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-106">This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff6cd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff6cd-107">Syntax</span></span>


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a><span data-ttu-id="ff6cd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ff6cd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ff6cd-109">**CB**</span><span class="sxs-lookup"><span data-stu-id="ff6cd-109">**cb**</span></span>
</dt> <dd>

<span data-ttu-id="ff6cd-110">Valor **ULong** que especifica el tamaño, en bytes, de **PB**.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-110">A **ULONG** value that specifies the size, in bytes, of **pb**.</span></span>

</dd> <dt>

<span data-ttu-id="ff6cd-111">**PB**</span><span class="sxs-lookup"><span data-stu-id="ff6cd-111">**pb**</span></span>
</dt> <dd>

<span data-ttu-id="ff6cd-112">Un puntero a un **byte** que contiene el BLOB, en formato [*PKCS \# 12*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ff6cd-112">A pointer to a **BYTE** that contains the BLOB, in [*PKCS \#12*](../secgloss/p-gly.md) format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff6cd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff6cd-113">Requirements</span></span>



| <span data-ttu-id="ff6cd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff6cd-114">Requirement</span></span> | <span data-ttu-id="ff6cd-115">Value</span><span class="sxs-lookup"><span data-stu-id="ff6cd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff6cd-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff6cd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ff6cd-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ff6cd-117">None supported</span></span><br/>                                                             |
| <span data-ttu-id="ff6cd-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff6cd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ff6cd-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff6cd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ff6cd-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff6cd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff6cd-121"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff6cd-121"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff6cd-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff6cd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff6cd-123">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="ff6cd-123">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> <dt>

[<span data-ttu-id="ff6cd-124">**KEYSVC \_ cadena UNIcode \_**</span><span class="sxs-lookup"><span data-stu-id="ff6cd-124">**KEYSVC\_UNICODE\_STRING**</span></span>](keysvc-unicode-string.md)
</dt> </dl>

 

 
