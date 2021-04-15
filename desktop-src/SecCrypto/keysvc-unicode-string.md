---
description: La \_ estructura de cadena Unicode KEYSVC \_ define una cadena Unicode y una longitud máxima para la cadena. La función RKeyPFXInstall usa esta estructura.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: KEYSVC_UNICODE_STRING estructura (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_UNICODE_STRING
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5424fa103b2bbbadd735dbda0bb92f9dea21787b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688672"
---
# <a name="keysvc_unicode_string-structure"></a><span data-ttu-id="c9dc2-104">KEYSVC \_ estructura de \_ cadena Unicode</span><span class="sxs-lookup"><span data-stu-id="c9dc2-104">KEYSVC\_UNICODE\_STRING structure</span></span>

<span data-ttu-id="c9dc2-105">La estructura de **\_ \_ cadena Unicode KEYSVC** define una cadena [*Unicode*](../secgloss/u-gly.md) y una longitud máxima para la cadena.</span><span class="sxs-lookup"><span data-stu-id="c9dc2-105">The **KEYSVC\_UNICODE\_STRING** structure defines a [*Unicode*](../secgloss/u-gly.md) string and a maximum length for the string.</span></span> <span data-ttu-id="c9dc2-106">La función [**RKeyPFXInstall**](rkeypfxinstall.md) usa esta estructura.</span><span class="sxs-lookup"><span data-stu-id="c9dc2-106">This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9dc2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9dc2-107">Syntax</span></span>


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## <a name="members"></a><span data-ttu-id="c9dc2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c9dc2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c9dc2-109">**Duración**</span><span class="sxs-lookup"><span data-stu-id="c9dc2-109">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="c9dc2-110">Valor **USHORT** que especifica la longitud, en bytes, que se usa para el **búfer**.</span><span class="sxs-lookup"><span data-stu-id="c9dc2-110">A **USHORT** value that specifies the length, in bytes, used for **Buffer**.</span></span>

</dd> <dt>

<span data-ttu-id="c9dc2-111">**MaximumLength**</span><span class="sxs-lookup"><span data-stu-id="c9dc2-111">**MaximumLength**</span></span>
</dt> <dd>

<span data-ttu-id="c9dc2-112">Valor **USHORT** que especifica la longitud máxima, en bytes, permitida para el **búfer**.</span><span class="sxs-lookup"><span data-stu-id="c9dc2-112">A **USHORT** value that specifies the maximum length, in bytes, allowed for **Buffer**.</span></span>

</dd> <dt>

<span data-ttu-id="c9dc2-113">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="c9dc2-113">**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="c9dc2-114">Un puntero a un valor **USHORT** que representa la cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="c9dc2-114">A pointer to a **USHORT** that represents the Unicode string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9dc2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9dc2-115">Requirements</span></span>



| <span data-ttu-id="c9dc2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9dc2-116">Requirement</span></span> | <span data-ttu-id="c9dc2-117">Value</span><span class="sxs-lookup"><span data-stu-id="c9dc2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9dc2-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9dc2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c9dc2-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c9dc2-119">None supported</span></span><br/>                                                             |
| <span data-ttu-id="c9dc2-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9dc2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c9dc2-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9dc2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9dc2-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9dc2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9dc2-123"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9dc2-123"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9dc2-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9dc2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9dc2-125">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="c9dc2-125">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> <dt>

[<span data-ttu-id="c9dc2-126">**\_BLOB KEYSVC**</span><span class="sxs-lookup"><span data-stu-id="c9dc2-126">**KEYSVC\_BLOB**</span></span>](keysvc-blob.md)
</dt> </dl>

 

 
