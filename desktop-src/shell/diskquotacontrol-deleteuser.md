---
description: Elimina un usuario del volumen.
ms.assetid: 56a07388-b7d8-41a4-b29a-8a57fe0b9d19
title: Método DiskQuotaControl. DeleteUser (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DeleteUser
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c159375727ef115631a8a047d69ce235a5b8f2a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275232"
---
# <a name="diskquotacontroldeleteuser-method"></a><span data-ttu-id="9d1b4-103">DiskQuotaControl. DeleteUser, método</span><span class="sxs-lookup"><span data-stu-id="9d1b4-103">DiskQuotaControl.DeleteUser method</span></span>

<span data-ttu-id="9d1b4-104">Elimina un usuario del volumen.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-104">Deletes a user from the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d1b4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d1b4-105">Syntax</span></span>


```JScript
DiskQuotaControl.DeleteUser(
  oUser
)
```



## <a name="parameters"></a><span data-ttu-id="9d1b4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d1b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d1b4-107">*oUser*</span><span class="sxs-lookup"><span data-stu-id="9d1b4-107">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="9d1b4-108">Tipo: **Object**</span><span class="sxs-lookup"><span data-stu-id="9d1b4-108">Type: **Object**</span></span>

<span data-ttu-id="9d1b4-109">Expresión de objeto que se evalúa como el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) del usuario.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-109">An object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d1b4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d1b4-110">Return value</span></span>

<span data-ttu-id="9d1b4-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d1b4-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d1b4-112">Remarks</span></span>

<span data-ttu-id="9d1b4-113">Este método produce un error si el usuario posee algún almacenamiento en el volumen.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-113">This method fails if the user owns any storage on the volume.</span></span> <span data-ttu-id="9d1b4-114">Antes de eliminar un usuario de un volumen, se debe eliminar todo el almacenamiento de ese usuario, moverse a otro volumen o transferir su propiedad a otro usuario.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-114">Before you delete a user from a volume, all storage for that user must be deleted, be moved to another volume, or have its ownership transferred to another user.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d1b4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d1b4-115">Requirements</span></span>



| <span data-ttu-id="9d1b4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d1b4-116">Requirement</span></span> | <span data-ttu-id="9d1b4-117">Value</span><span class="sxs-lookup"><span data-stu-id="9d1b4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d1b4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d1b4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9d1b4-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9d1b4-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d1b4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d1b4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9d1b4-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9d1b4-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9d1b4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d1b4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d1b4-123"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d1b4-123"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="9d1b4-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9d1b4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d1b4-125"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9d1b4-125"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d1b4-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d1b4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d1b4-127">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="9d1b4-127">**AddUser**</span></span>](diskquotacontrol-adduser.md)
</dt> <dt>

[<span data-ttu-id="9d1b4-128">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="9d1b4-128">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




