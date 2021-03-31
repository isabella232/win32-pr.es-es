---
title: Método GetVirtualDesktopDetails de la clase Win32_RDMSVirtualDesktop
description: Recupera la información adicional sobre el escritorio virtual.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- Método GetVirtualDesktopDetails Servicios de Escritorio remoto
- Método GetVirtualDesktopDetails Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de clase Servicios de Escritorio remoto, método GetVirtualDesktopDetails
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopDetails
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7382a7ea10b3e557cd7317bdf1ddb0c4bcea55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491338"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="b64bc-106">Método GetVirtualDesktopDetails de la \_ clase RDMSVirtualDesktop de Win32</span><span class="sxs-lookup"><span data-stu-id="b64bc-106">GetVirtualDesktopDetails method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="b64bc-107">Recupera la información adicional sobre el escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="b64bc-107">Retrieves the additional information about the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="b64bc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b64bc-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopDetails(
  [out] uint32  RAMSizeInMB,
  [out] boolean RemoteFXEnabled,
  [out] string  OSVersion
);
```



## <a name="parameters"></a><span data-ttu-id="b64bc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b64bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b64bc-110">*RAMSizeInMB* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b64bc-110">*RAMSizeInMB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b64bc-111">Recibe la cantidad de RAM asignada al escritorio virtual, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b64bc-111">Receives the amount of RAM assigned to the virtual desktop, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b64bc-112">*RemoteFXEnabled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b64bc-112">*RemoteFXEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b64bc-113">Recibe un valor que indica si RemoteFX está habilitado en el escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="b64bc-113">Receives a value that indicates whether RemoteFX is enabled on the virtual desktop.</span></span> <span data-ttu-id="b64bc-114">**True** si RemoteFX está habilitado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b64bc-114">**TRUE** if RemoteFX is enabled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b64bc-115">*OSVersion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b64bc-115">*OSVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b64bc-116">Recibe la versión del sistema operativo del escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="b64bc-116">Receives the OS version of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b64bc-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b64bc-117">Return value</span></span>

<span data-ttu-id="b64bc-118">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="b64bc-118">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b64bc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b64bc-119">Requirements</span></span>



| <span data-ttu-id="b64bc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b64bc-120">Requirement</span></span> | <span data-ttu-id="b64bc-121">Value</span><span class="sxs-lookup"><span data-stu-id="b64bc-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b64bc-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b64bc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b64bc-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b64bc-123">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b64bc-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b64bc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b64bc-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b64bc-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b64bc-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b64bc-126">Namespace</span></span><br/>                | <span data-ttu-id="b64bc-127">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="b64bc-127">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b64bc-128">MOF</span><span class="sxs-lookup"><span data-stu-id="b64bc-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b64bc-129"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b64bc-129"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b64bc-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b64bc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b64bc-131"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b64bc-131"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b64bc-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b64bc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b64bc-133">**Win32 \_ RDMSVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="b64bc-133">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





