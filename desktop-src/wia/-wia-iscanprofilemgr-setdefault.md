---
description: Establece el perfil de digitalización especificado como perfil predeterminado.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: 'IScanProfileMgr:: SetDefault (método) (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 3a7c32f246bcafc8ff7ce55e8c6f34ea45553a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667489"
---
# <a name="iscanprofilemgrsetdefault-method"></a><span data-ttu-id="bca09-103">IScanProfileMgr:: SetDefault (método)</span><span class="sxs-lookup"><span data-stu-id="bca09-103">IScanProfileMgr::SetDefault method</span></span>

<span data-ttu-id="bca09-104">Establece el perfil de digitalización especificado como perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bca09-104">Sets the specified scan profile as the default profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="bca09-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bca09-105">Syntax</span></span>


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="bca09-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bca09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bca09-107">*pScanProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bca09-107">*pScanProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bca09-108">Tipo: \**[**IScanProfile**](-wia-iscanprofile.md) \** _</span><span class="sxs-lookup"><span data-stu-id="bca09-108">Type: \**[**IScanProfile**](-wia-iscanprofile.md)\** _</span></span>

<span data-ttu-id="bca09-109">Puntero al perfil.</span><span class="sxs-lookup"><span data-stu-id="bca09-109">A pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bca09-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bca09-110">Return value</span></span>

<span data-ttu-id="bca09-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="bca09-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="bca09-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="bca09-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bca09-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bca09-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bca09-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bca09-114">Remarks</span></span>

<span data-ttu-id="bca09-115">Use el método **IScanProfileMgr:: SetDefault** para agregar un `<Default>` elemento al perfil o para quitar ese elemento del perfil predeterminado anterior del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bca09-115">Use the **IScanProfileMgr::SetDefault** method to add a `<Default>` element to the profile or to remove that element from the device's previous default profile.</span></span>

<span data-ttu-id="bca09-116">Use el método [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) para cambiar el perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bca09-116">Use the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method to change the default profile.</span></span>

## <a name="requirements"></a><span data-ttu-id="bca09-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bca09-117">Requirements</span></span>



| <span data-ttu-id="bca09-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bca09-118">Requirement</span></span> | <span data-ttu-id="bca09-119">Value</span><span class="sxs-lookup"><span data-stu-id="bca09-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="bca09-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bca09-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bca09-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bca09-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="bca09-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bca09-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bca09-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bca09-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bca09-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bca09-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bca09-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="bca09-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="bca09-126">IDL</span><span class="sxs-lookup"><span data-stu-id="bca09-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bca09-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bca09-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bca09-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="bca09-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bca09-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="bca09-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="bca09-130">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="bca09-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




