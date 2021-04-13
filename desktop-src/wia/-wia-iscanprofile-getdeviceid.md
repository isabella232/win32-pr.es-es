---
description: Devuelve el identificador del dispositivo.
ms.assetid: 72a0843d-36f2-463f-8269-0e91233f1931
title: 'IScanProfile:: GetDeviceID (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetDeviceID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: fb0e2597164cb0a82c15cecf394ce7a9e0bec16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360402"
---
# <a name="iscanprofilegetdeviceid-method"></a><span data-ttu-id="19c0c-103">IScanProfile:: GetDeviceID (método)</span><span class="sxs-lookup"><span data-stu-id="19c0c-103">IScanProfile::GetDeviceID method</span></span>

<span data-ttu-id="19c0c-104">Devuelve el identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19c0c-104">Returns the ID of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="19c0c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19c0c-105">Syntax</span></span>


```C++
HRESULT GetDeviceID(
  [out] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="19c0c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19c0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19c0c-107">*pbstrDeviceID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="19c0c-107">*pbstrDeviceID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19c0c-108">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="19c0c-108">Type: \**BSTR\** _</span></span>

<span data-ttu-id="19c0c-109">Puntero al identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19c0c-109">A pointer to the device ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19c0c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19c0c-110">Return value</span></span>

<span data-ttu-id="19c0c-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="19c0c-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="19c0c-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="19c0c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19c0c-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="19c0c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="19c0c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19c0c-114">Requirements</span></span>



| <span data-ttu-id="19c0c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="19c0c-115">Requirement</span></span> | <span data-ttu-id="19c0c-116">Value</span><span class="sxs-lookup"><span data-stu-id="19c0c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="19c0c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19c0c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="19c0c-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="19c0c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="19c0c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19c0c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="19c0c-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="19c0c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19c0c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19c0c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="19c0c-122"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="19c0c-122"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="19c0c-123">IDL</span><span class="sxs-lookup"><span data-stu-id="19c0c-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19c0c-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="19c0c-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19c0c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="19c0c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19c0c-126">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="19c0c-126">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="19c0c-127">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="19c0c-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




