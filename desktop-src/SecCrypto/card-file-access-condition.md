---
description: Especifica los permisos de control de acceso para un archivo en una tarjeta inteligente.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: Enumeración CARD_FILE_ACCESS_CONDITION (Cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: d3ef9fc81c9ab3bff5f3992c3aedeb3f923648ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666459"
---
# <a name="card_file_access_condition-enumeration"></a><span data-ttu-id="0b401-103">\_ \_ Enumeración de condiciones de acceso a archivos de tarjeta \_</span><span class="sxs-lookup"><span data-stu-id="0b401-103">CARD\_FILE\_ACCESS\_CONDITION enumeration</span></span>

<span data-ttu-id="0b401-104">La enumeración de la **\_ \_ \_ condición de acceso a archivos de tarjeta** especifica los permisos de control de acceso para un archivo en una [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0b401-104">The **CARD\_FILE\_ACCESS\_CONDITION** enumeration specifies access control permissions for a file on a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b401-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b401-105">Syntax</span></span>


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a><span data-ttu-id="0b401-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="0b401-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0b401-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span><span class="sxs-lookup"><span data-stu-id="0b401-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span></span>
</dt> <dd>

<span data-ttu-id="0b401-108">Este valor no es válido.</span><span class="sxs-lookup"><span data-stu-id="0b401-108">This value is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0b401-109"><span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**</span><span class="sxs-lookup"><span data-stu-id="0b401-109"><span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**</span></span>
</dt> <dd>

<span data-ttu-id="0b401-110">Todo el mundo puede leer el archivo.</span><span class="sxs-lookup"><span data-stu-id="0b401-110">Everyone can read the file.</span></span> <span data-ttu-id="0b401-111">Los usuarios específicos pueden escribir en el archivo.</span><span class="sxs-lookup"><span data-stu-id="0b401-111">Specific users can write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="0b401-112"><span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**</span><span class="sxs-lookup"><span data-stu-id="0b401-112"><span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**</span></span>
</dt> <dd>

<span data-ttu-id="0b401-113">Solo los usuarios específicos pueden leer o escribir en el archivo.</span><span class="sxs-lookup"><span data-stu-id="0b401-113">Only specific users can read or write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="0b401-114"><span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**</span><span class="sxs-lookup"><span data-stu-id="0b401-114"><span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**</span></span>
</dt> <dd>

<span data-ttu-id="0b401-115">Todo el mundo puede leer el archivo.</span><span class="sxs-lookup"><span data-stu-id="0b401-115">Everyone can read the file.</span></span> <span data-ttu-id="0b401-116">Los administradores pueden escribir en el archivo.</span><span class="sxs-lookup"><span data-stu-id="0b401-116">Administrators can write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="0b401-117"><span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**</span><span class="sxs-lookup"><span data-stu-id="0b401-117"><span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**</span></span>
</dt> <dd>

<span data-ttu-id="0b401-118">Los permisos de acceso para el archivo son desconocidos.</span><span class="sxs-lookup"><span data-stu-id="0b401-118">Access permissions for the file are unknown.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b401-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b401-119">Requirements</span></span>



| <span data-ttu-id="0b401-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b401-120">Requirement</span></span> | <span data-ttu-id="0b401-121">Value</span><span class="sxs-lookup"><span data-stu-id="0b401-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0b401-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b401-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0b401-123">Windows XP, \[ solo aplicaciones de escritorio de Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0b401-123">Windows XP, Windows XP \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0b401-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b401-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0b401-125">Windows Server 2003, solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b401-125">Windows Server 2003, Windows Server 2003 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="0b401-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b401-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b401-127"><dt>Cardmod. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b401-127"><dt>Cardmod.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b401-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b401-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b401-129">Proveedor de servicios criptográficos de tarjeta inteligente base de Microsoft</span><span class="sxs-lookup"><span data-stu-id="0b401-129">Microsoft Base Smart Card Cryptographic Service Provider</span></span>](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[<span data-ttu-id="0b401-130">**\_información del archivo de tarjeta \_**</span><span class="sxs-lookup"><span data-stu-id="0b401-130">**CARD\_FILE\_INFO**</span></span>](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[<span data-ttu-id="0b401-131">**CardCreateFile**</span><span class="sxs-lookup"><span data-stu-id="0b401-131">**CardCreateFile**</span></span>](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
