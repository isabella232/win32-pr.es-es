---
description: Especifica los permisos de control de acceso para un directorio en una tarjeta inteligente.
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: Enumeración CARD_DIRECTORY_ACCESS_CONDITION (Cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_DIRECTORY_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: 9879fa73f6bb45b56f433d7bca7765ab5fc0daef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275334"
---
# <a name="card_directory_access_condition-enumeration"></a><span data-ttu-id="e3a57-103">\_ \_ Enumeración de condiciones de acceso al directorio de tarjeta \_</span><span class="sxs-lookup"><span data-stu-id="e3a57-103">CARD\_DIRECTORY\_ACCESS\_CONDITION enumeration</span></span>

<span data-ttu-id="e3a57-104">La enumeración **\_ condición de \_ acceso \_ al directorio** de la tarjeta especifica los permisos de control de acceso para un directorio en una [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e3a57-104">The **CARD\_DIRECTORY\_ACCESS\_CONDITION** enumeration specifies access control permissions for a directory on a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a57-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3a57-105">Syntax</span></span>


```C++
typedef enum  { 
  InvalidAc               = 0,
  UserCreateDeleteDirAc   = 1,
  AdminCreateDeleteDirAc  = 2
} CARD_DIRECTORY_ACCESS_CONDITION;
```



## <a name="constants"></a><span data-ttu-id="e3a57-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="e3a57-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e3a57-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span><span class="sxs-lookup"><span data-stu-id="e3a57-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span></span>
</dt> <dd>

<span data-ttu-id="e3a57-108">Este valor no es válido.</span><span class="sxs-lookup"><span data-stu-id="e3a57-108">This value is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e3a57-109"><span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**</span><span class="sxs-lookup"><span data-stu-id="e3a57-109"><span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**</span></span>
</dt> <dd>

<span data-ttu-id="e3a57-110">Los usuarios específicos pueden leer, escribir y eliminar el directorio.</span><span class="sxs-lookup"><span data-stu-id="e3a57-110">Specific users can read, write, and delete the directory.</span></span>

</dd> <dt>

<span data-ttu-id="e3a57-111"><span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**</span><span class="sxs-lookup"><span data-stu-id="e3a57-111"><span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**</span></span>
</dt> <dd>

<span data-ttu-id="e3a57-112">Los administradores pueden leer, escribir y eliminar el directorio.</span><span class="sxs-lookup"><span data-stu-id="e3a57-112">Administrators can read, write, and delete the directory.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3a57-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3a57-113">Requirements</span></span>



| <span data-ttu-id="e3a57-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a57-114">Requirement</span></span> | <span data-ttu-id="e3a57-115">Value</span><span class="sxs-lookup"><span data-stu-id="e3a57-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a57-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3a57-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a57-117">Windows XP, \[ solo aplicaciones de escritorio de Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e3a57-117">Windows XP, Windows XP \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e3a57-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3a57-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a57-119">Windows Server 2003, solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3a57-119">Windows Server 2003, Windows Server 2003 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="e3a57-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3a57-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3a57-121"><dt>Cardmod. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3a57-121"><dt>Cardmod.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a57-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3a57-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a57-123">Proveedor de servicios criptográficos de tarjeta inteligente base de Microsoft</span><span class="sxs-lookup"><span data-stu-id="e3a57-123">Microsoft Base Smart Card Cryptographic Service Provider</span></span>](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[<span data-ttu-id="e3a57-124">**CardCreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="e3a57-124">**CardCreateDirectory**</span></span>](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[<span data-ttu-id="e3a57-125">**CardDeleteDirectory**</span><span class="sxs-lookup"><span data-stu-id="e3a57-125">**CardDeleteDirectory**</span></span>](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 
