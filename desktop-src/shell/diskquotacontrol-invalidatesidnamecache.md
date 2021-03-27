---
description: Invalida la memoria caché de nombres de usuario del identificador de seguridad.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: Método DiskQuotaControl. InvalidateSidNameCache (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.InvalidateSidNameCache
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e7202c1293d32d55e12e88671ed9960d376f63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000983"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a><span data-ttu-id="6d746-103">DiskQuotaControl. InvalidateSidNameCache, método</span><span class="sxs-lookup"><span data-stu-id="6d746-103">DiskQuotaControl.InvalidateSidNameCache method</span></span>

<span data-ttu-id="6d746-104">Invalida la memoria caché de nombres de usuario del identificador de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6d746-104">Invalidates the security ID user name cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d746-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d746-105">Syntax</span></span>


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a><span data-ttu-id="6d746-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d746-106">Parameters</span></span>

<span data-ttu-id="6d746-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6d746-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d746-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d746-108">Return value</span></span>

<span data-ttu-id="6d746-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6d746-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d746-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d746-110">Remarks</span></span>

<span data-ttu-id="6d746-111">Los nombres de usuario y los identificadores de seguridad asociados se almacenan en una caché.</span><span class="sxs-lookup"><span data-stu-id="6d746-111">User names and associated security IDs are stored in a cache.</span></span> <span data-ttu-id="6d746-112">Puede borrar esta memoria caché mediante una llamada a **InvalidateSidNameCache**.</span><span class="sxs-lookup"><span data-stu-id="6d746-112">You can clear this cache by calling **InvalidateSidNameCache**.</span></span> <span data-ttu-id="6d746-113">Si posteriormente crea un nuevo objeto de usuario, la información deberá obtenerse del controlador de dominio y se tendrá que restablecer la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="6d746-113">If you subsequently create a new user object, the information will have to be obtained from the domain controller, and the cache will have to be reestablished.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d746-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d746-114">Requirements</span></span>



| <span data-ttu-id="6d746-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d746-115">Requirement</span></span> | <span data-ttu-id="6d746-116">Value</span><span class="sxs-lookup"><span data-stu-id="6d746-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d746-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d746-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6d746-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6d746-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d746-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d746-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6d746-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6d746-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6d746-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d746-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d746-122"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d746-122"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="6d746-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6d746-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d746-124"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6d746-124"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d746-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d746-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d746-126">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="6d746-126">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




