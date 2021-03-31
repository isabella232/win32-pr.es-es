---
description: Elimina todos los perfiles de digitalización disponibles para el usuario en el sistema en el que se ejecuta la aplicación.
ms.assetid: 1a79fd0e-1309-4fc4-863f-6dfb20594d91
title: IScanProfileMgr::D método eleteAllProfilesForUser (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfilesForUser
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: c5d723379bb542346e3612f70c19a1629d325ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154869"
---
# <a name="iscanprofilemgrdeleteallprofilesforuser-method"></a><span data-ttu-id="b4ce2-103">IScanProfileMgr::D método eleteAllProfilesForUser</span><span class="sxs-lookup"><span data-stu-id="b4ce2-103">IScanProfileMgr::DeleteAllProfilesForUser method</span></span>

<span data-ttu-id="b4ce2-104">Elimina todos los perfiles de digitalización disponibles para el usuario en el sistema en el que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b4ce2-104">Deletes all the scan profiles available for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4ce2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4ce2-105">Syntax</span></span>


```C++
HRESULT DeleteAllProfilesForUser();
```



## <a name="parameters"></a><span data-ttu-id="b4ce2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4ce2-106">Parameters</span></span>

<span data-ttu-id="b4ce2-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b4ce2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4ce2-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4ce2-108">Return value</span></span>

<span data-ttu-id="b4ce2-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b4ce2-109">Type: **HRESULT**</span></span>

<span data-ttu-id="b4ce2-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b4ce2-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b4ce2-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b4ce2-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4ce2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4ce2-112">Requirements</span></span>



| <span data-ttu-id="b4ce2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4ce2-113">Requirement</span></span> | <span data-ttu-id="b4ce2-114">Value</span><span class="sxs-lookup"><span data-stu-id="b4ce2-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ce2-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4ce2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b4ce2-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b4ce2-116">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b4ce2-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4ce2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b4ce2-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b4ce2-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b4ce2-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4ce2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4ce2-120"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4ce2-120"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="b4ce2-121">IDL</span><span class="sxs-lookup"><span data-stu-id="b4ce2-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4ce2-122"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4ce2-122"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4ce2-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4ce2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4ce2-124">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="b4ce2-124">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="b4ce2-125">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="b4ce2-125">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




