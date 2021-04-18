---
description: Obtiene el número de perfiles de examen creados para el usuario en el sistema en el que se ejecuta la aplicación.
ms.assetid: 0667a885-d61f-4c44-b988-a42242c2678e
title: 'IScanProfileMgr:: GetNumProfiles (método) (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: a8c3167bd428054054a32d7823ce57e562501533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706319"
---
# <a name="iscanprofilemgrgetnumprofiles-method"></a><span data-ttu-id="8e5e6-103">IScanProfileMgr:: GetNumProfiles (método)</span><span class="sxs-lookup"><span data-stu-id="8e5e6-103">IScanProfileMgr::GetNumProfiles method</span></span>

<span data-ttu-id="8e5e6-104">Obtiene el número de perfiles de examen creados para el usuario en el sistema en el que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-104">Gets the number of scan profiles created for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e5e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e5e6-105">Syntax</span></span>


```C++
HRESULT GetNumProfiles(
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a><span data-ttu-id="8e5e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e5e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e5e6-107">*pulNumProfiles* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8e5e6-107">*pulNumProfiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5e6-108">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="8e5e6-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="8e5e6-109">Puntero al número de perfiles creados para el usuario.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-109">A pointer to the number of profiles created for the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e5e6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e5e6-110">Return value</span></span>

<span data-ttu-id="8e5e6-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8e5e6-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8e5e6-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e5e6-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e5e6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e5e6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e5e6-114">Requirements</span></span>



| <span data-ttu-id="8e5e6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e5e6-115">Requirement</span></span> | <span data-ttu-id="8e5e6-116">Value</span><span class="sxs-lookup"><span data-stu-id="8e5e6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e5e6-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e5e6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8e5e6-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8e5e6-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="8e5e6-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e5e6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8e5e6-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e5e6-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e5e6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e5e6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e5e6-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e5e6-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="8e5e6-123">IDL</span><span class="sxs-lookup"><span data-stu-id="8e5e6-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8e5e6-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8e5e6-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e5e6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e5e6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e5e6-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="8e5e6-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="8e5e6-127">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="8e5e6-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




