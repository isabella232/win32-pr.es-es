---
title: Método SetMaxXResolution de la clase Win32_TSClientSetting
description: Establece la propiedad MaxXResolution.
ms.assetid: c1e00bab-ab32-4cf6-8121-950184bd8a01
ms.tgt_platform: multiple
keywords:
- Método SetMaxXResolution Servicios de Escritorio remoto
- Método SetMaxXResolution Servicios de Escritorio remoto, clase Win32_TSClientSetting
- Win32_TSClientSetting de clase Servicios de Escritorio remoto, método SetMaxXResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxXResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ab911fd66c7cf6b4f657d8f9e060eccee80675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490306"
---
# <a name="setmaxxresolution-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="3e0d0-106">Método SetMaxXResolution de la \_ clase TSClientSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="3e0d0-106">SetMaxXResolution method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="3e0d0-107">Establece la propiedad **MaxXResolution** .</span><span class="sxs-lookup"><span data-stu-id="3e0d0-107">Sets the **MaxXResolution** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e0d0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e0d0-108">Syntax</span></span>


```mof
uint32 SetMaxXResolution(
  [in] uint32 MaxXResolution
);
```



## <a name="parameters"></a><span data-ttu-id="3e0d0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e0d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e0d0-110">*MaxXResolution* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e0d0-110">*MaxXResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e0d0-111">La nueva resolución X máxima admitida por el servidor.</span><span class="sxs-lookup"><span data-stu-id="3e0d0-111">The new maximum X resolution supported by the server.</span></span> <span data-ttu-id="3e0d0-112">El valor mínimo es 200 y el valor máximo es 4096.</span><span class="sxs-lookup"><span data-stu-id="3e0d0-112">The minimum value is 200 and maximum value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e0d0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e0d0-113">Return value</span></span>

<span data-ttu-id="3e0d0-114">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="3e0d0-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="3e0d0-115">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="3e0d0-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="3e0d0-116">El método devuelve un error si el servidor invalida la configuración de conexión del usuario.</span><span class="sxs-lookup"><span data-stu-id="3e0d0-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e0d0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e0d0-117">Requirements</span></span>



| <span data-ttu-id="3e0d0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e0d0-118">Requirement</span></span> | <span data-ttu-id="3e0d0-119">Value</span><span class="sxs-lookup"><span data-stu-id="3e0d0-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e0d0-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e0d0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3e0d0-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3e0d0-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3e0d0-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e0d0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3e0d0-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3e0d0-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="3e0d0-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3e0d0-124">Namespace</span></span><br/>                | <span data-ttu-id="3e0d0-125">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3e0d0-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3e0d0-126">MOF</span><span class="sxs-lookup"><span data-stu-id="3e0d0-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e0d0-127"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e0d0-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e0d0-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e0d0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e0d0-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e0d0-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e0d0-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e0d0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e0d0-131">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="3e0d0-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





