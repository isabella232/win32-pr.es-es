---
description: Vuelve a enumerar todos los perfiles de digitalización en el sistema.
ms.assetid: f5e49645-e81a-4750-8ea5-f0c698a61752
title: 'IScanProfileMgr:: Refresh (método) (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.Refresh
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: e4af44e95889abf35fe13e1669411513458a16c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001301"
---
# <a name="iscanprofilemgrrefresh-method"></a><span data-ttu-id="86ade-103">IScanProfileMgr:: Refresh (método)</span><span class="sxs-lookup"><span data-stu-id="86ade-103">IScanProfileMgr::Refresh method</span></span>

<span data-ttu-id="86ade-104">Vuelve a enumerar todos los perfiles de digitalización en el sistema.</span><span class="sxs-lookup"><span data-stu-id="86ade-104">Re-enumerates all the scan profiles in the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="86ade-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86ade-105">Syntax</span></span>


```C++
HRESULT Refresh();
```



## <a name="parameters"></a><span data-ttu-id="86ade-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86ade-106">Parameters</span></span>

<span data-ttu-id="86ade-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="86ade-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86ade-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86ade-108">Return value</span></span>

<span data-ttu-id="86ade-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="86ade-109">Type: **HRESULT**</span></span>

<span data-ttu-id="86ade-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="86ade-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="86ade-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="86ade-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="86ade-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86ade-112">Remarks</span></span>

<span data-ttu-id="86ade-113">Use este método cuando más de un objeto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) pueda estar creando o eliminando perfiles al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="86ade-113">Use this method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="86ade-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86ade-114">Requirements</span></span>



| <span data-ttu-id="86ade-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="86ade-115">Requirement</span></span> | <span data-ttu-id="86ade-116">Value</span><span class="sxs-lookup"><span data-stu-id="86ade-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="86ade-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86ade-117">Minimum supported client</span></span><br/> | <span data-ttu-id="86ade-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="86ade-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="86ade-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86ade-119">Minimum supported server</span></span><br/> | <span data-ttu-id="86ade-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="86ade-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="86ade-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86ade-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="86ade-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="86ade-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="86ade-123">IDL</span><span class="sxs-lookup"><span data-stu-id="86ade-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="86ade-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="86ade-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86ade-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="86ade-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86ade-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="86ade-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="86ade-127">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="86ade-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




