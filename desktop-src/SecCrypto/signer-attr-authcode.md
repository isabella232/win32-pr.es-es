---
description: Especifica los atributos de una firma Authenticode.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: Estructura de SIGNER_ATTR_AUTHCODE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_ATTR_AUTHCODE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 952ed0f55a185d9a7ef9eeed3366f64c84423ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003112"
---
# <a name="signer_attr_authcode-structure"></a><span data-ttu-id="52f9a-103">\_Estructura fases de atributo de firmante \_</span><span class="sxs-lookup"><span data-stu-id="52f9a-103">SIGNER\_ATTR\_AUTHCODE structure</span></span>

<span data-ttu-id="52f9a-104">La estructura **Signer \_ ATTR \_ fases** especifica atributos para una firma [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="52f9a-104">The **SIGNER\_ATTR\_AUTHCODE** structure specifies attributes for an [*Authenticode*](../secgloss/a-gly.md) signature.</span></span>

> [!Note]  
> <span data-ttu-id="52f9a-105">Esta estructura no está definida en ningún archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="52f9a-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="52f9a-106">Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.</span><span class="sxs-lookup"><span data-stu-id="52f9a-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="52f9a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52f9a-107">Syntax</span></span>


```C++
typedef struct _SIGNER_ATTR_AUTHCODE {
  DWORD   cbSize;
  BOOL    fCommercial;
  BOOL    fIndividual;
  LPCWSTR pwszName;
  LPCWSTR pwszInfo;
} SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
```



## <a name="members"></a><span data-ttu-id="52f9a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="52f9a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="52f9a-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="52f9a-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="52f9a-110">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="52f9a-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="52f9a-111">**fCommercial**</span><span class="sxs-lookup"><span data-stu-id="52f9a-111">**fCommercial**</span></span>
</dt> <dd>

<span data-ttu-id="52f9a-112">**True** para firmar el sujeto como publicador comercial; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="52f9a-112">**TRUE** to sign the subject as a commercial publisher; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="52f9a-113">**fIndividual**</span><span class="sxs-lookup"><span data-stu-id="52f9a-113">**fIndividual**</span></span>
</dt> <dd>

<span data-ttu-id="52f9a-114">**True** para firmar el sujeto como publicador individual; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="52f9a-114">**TRUE** to sign the subject as an individual publisher; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="52f9a-115">**pwszName**</span><span class="sxs-lookup"><span data-stu-id="52f9a-115">**pwszName**</span></span>
</dt> <dd>

<span data-ttu-id="52f9a-116">Nombre para mostrar del archivo durante la descarga.</span><span class="sxs-lookup"><span data-stu-id="52f9a-116">The display name of the file upon download.</span></span>

</dd> <dt>

<span data-ttu-id="52f9a-117">**pwszInfo**</span><span class="sxs-lookup"><span data-stu-id="52f9a-117">**pwszInfo**</span></span>
</dt> <dd>

<span data-ttu-id="52f9a-118">El nombre para mostrar de la dirección URL del archivo durante la descarga.</span><span class="sxs-lookup"><span data-stu-id="52f9a-118">The display name of the URL of the file upon download.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52f9a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52f9a-119">Requirements</span></span>



| <span data-ttu-id="52f9a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="52f9a-120">Requirement</span></span> | <span data-ttu-id="52f9a-121">Value</span><span class="sxs-lookup"><span data-stu-id="52f9a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="52f9a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52f9a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="52f9a-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="52f9a-123">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="52f9a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52f9a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="52f9a-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="52f9a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52f9a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="52f9a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f9a-127">**información de \_ firma del firmante \_**</span><span class="sxs-lookup"><span data-stu-id="52f9a-127">**SIGNER\_SIGNATURE\_INFO**</span></span>](signer-signature-info.md)
</dt> </dl>

 

 
