---
title: Método AddVirtualDesktop de la clase Win32_RDMSVirtualDesktopCollection
description: Agrega un escritorio virtual a la colección de escritorios virtuales.
ms.assetid: 31a3aa28-6e5d-4f8a-81ff-ab011f568b6a
ms.tgt_platform: multiple
keywords:
- Método AddVirtualDesktop Servicios de Escritorio remoto
- Método AddVirtualDesktop Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método AddVirtualDesktop
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.AddVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4858f99f2ea4793fe0d83d06a0aaa429b7aa8f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533885"
---
# <a name="addvirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="233df-106">Método AddVirtualDesktop de la \_ clase RDMSVirtualDesktopCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="233df-106">AddVirtualDesktop method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="233df-107">Agrega un escritorio virtual a la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="233df-107">Adds a virtual desktop to the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="233df-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="233df-108">Syntax</span></span>


```mof
uint32 AddVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="233df-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="233df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="233df-110">*VMName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="233df-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="233df-111">El nombre de la máquina virtual que hospeda el escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="233df-111">The name of the virtual machine that hosts the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="233df-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="233df-112">Return value</span></span>

<span data-ttu-id="233df-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="233df-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="233df-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="233df-114">Requirements</span></span>



| <span data-ttu-id="233df-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="233df-115">Requirement</span></span> | <span data-ttu-id="233df-116">Value</span><span class="sxs-lookup"><span data-stu-id="233df-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="233df-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="233df-117">Minimum supported client</span></span><br/> | <span data-ttu-id="233df-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="233df-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="233df-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="233df-119">Minimum supported server</span></span><br/> | <span data-ttu-id="233df-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="233df-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="233df-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="233df-121">Namespace</span></span><br/>                | <span data-ttu-id="233df-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="233df-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="233df-123">MOF</span><span class="sxs-lookup"><span data-stu-id="233df-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="233df-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="233df-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="233df-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="233df-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="233df-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="233df-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="233df-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="233df-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="233df-128">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="233df-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





