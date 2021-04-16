---
title: Método EnableUserVhd de la clase Win32_TSSessionDirectory
description: Habilita un VHD de Perfil de usuario en un servidor RDSH.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- Método EnableUserVhd Servicios de Escritorio remoto
- Método EnableUserVhd Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método EnableUserVhd
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.EnableUserVhd
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464e105d2f8f0c80126e6b9ca5e5a383b2d17628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686243"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="757c0-106">Método EnableUserVhd de la \_ clase TSSessionDirectory de Win32</span><span class="sxs-lookup"><span data-stu-id="757c0-106">EnableUserVhd method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="757c0-107">Habilita un VHD de Perfil de usuario en un servidor RDSH.</span><span class="sxs-lookup"><span data-stu-id="757c0-107">Enables a user profile VHD on an RDSH server.</span></span>

## <a name="syntax"></a><span data-ttu-id="757c0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="757c0-108">Syntax</span></span>


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a><span data-ttu-id="757c0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="757c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="757c0-110">*UvhdShareUrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="757c0-110">*UvhdShareUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="757c0-111">Ubicación del recurso compartido donde se almacenan todos los VHD de Perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="757c0-111">The location of the share where all user profile VHDs are stored.</span></span>

</dd> <dt>

<span data-ttu-id="757c0-112">*UvhdRoamingPolicyXml* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="757c0-112">*UvhdRoamingPolicyXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="757c0-113">La Directiva de itinerancia para el VHD de Perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="757c0-113">The roaming policy for the user profile VHD.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="757c0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="757c0-114">Requirements</span></span>



| <span data-ttu-id="757c0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="757c0-115">Requirement</span></span> | <span data-ttu-id="757c0-116">Value</span><span class="sxs-lookup"><span data-stu-id="757c0-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="757c0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="757c0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="757c0-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="757c0-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="757c0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="757c0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="757c0-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="757c0-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="757c0-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="757c0-121">Namespace</span></span><br/>                | <span data-ttu-id="757c0-122">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="757c0-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="757c0-123">MOF</span><span class="sxs-lookup"><span data-stu-id="757c0-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="757c0-124"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="757c0-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="757c0-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="757c0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="757c0-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="757c0-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="757c0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="757c0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="757c0-128">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="757c0-128">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

 





