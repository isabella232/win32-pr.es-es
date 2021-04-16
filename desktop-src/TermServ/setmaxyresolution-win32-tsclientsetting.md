---
title: Método SetMaxYResolution de la clase Win32_TSClientSetting
description: Establece la propiedad MaxYResolution.
ms.assetid: a8399c7c-6b3a-464f-8112-8838257ccf06
ms.tgt_platform: multiple
keywords:
- Método SetMaxYResolution Servicios de Escritorio remoto
- Método SetMaxYResolution Servicios de Escritorio remoto, clase Win32_TSClientSetting
- Win32_TSClientSetting de clase Servicios de Escritorio remoto, método SetMaxYResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxYResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c85564e075865d993552e831869979fc6227af29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676751"
---
# <a name="setmaxyresolution-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="ef8ff-106">Método SetMaxYResolution de la \_ clase TSClientSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="ef8ff-106">SetMaxYResolution method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="ef8ff-107">Establece la propiedad **MaxYResolution** .</span><span class="sxs-lookup"><span data-stu-id="ef8ff-107">Sets the **MaxYResolution** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef8ff-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef8ff-108">Syntax</span></span>


```mof
uint32 SetMaxYResolution(
  [in] uint32 MaxYResolution
);
```



## <a name="parameters"></a><span data-ttu-id="ef8ff-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef8ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef8ff-110">*MaxYResolution* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef8ff-110">*MaxYResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef8ff-111">La nueva resolución Y máxima admitida por el servidor.</span><span class="sxs-lookup"><span data-stu-id="ef8ff-111">The new maximum Y resolution supported by the server.</span></span> <span data-ttu-id="ef8ff-112">El valor mínimo es 200 y el valor máximo es 2048.</span><span class="sxs-lookup"><span data-stu-id="ef8ff-112">The minimum value is 200 and the maximum value is 2048.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef8ff-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef8ff-113">Return value</span></span>

<span data-ttu-id="ef8ff-114">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="ef8ff-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="ef8ff-115">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="ef8ff-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="ef8ff-116">El método devuelve un error si el servidor invalida la configuración de conexión del usuario.</span><span class="sxs-lookup"><span data-stu-id="ef8ff-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef8ff-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef8ff-117">Requirements</span></span>



| <span data-ttu-id="ef8ff-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef8ff-118">Requirement</span></span> | <span data-ttu-id="ef8ff-119">Value</span><span class="sxs-lookup"><span data-stu-id="ef8ff-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef8ff-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef8ff-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ef8ff-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ef8ff-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ef8ff-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef8ff-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ef8ff-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ef8ff-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="ef8ff-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ef8ff-124">Namespace</span></span><br/>                | <span data-ttu-id="ef8ff-125">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ef8ff-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ef8ff-126">MOF</span><span class="sxs-lookup"><span data-stu-id="ef8ff-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef8ff-127"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef8ff-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef8ff-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef8ff-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef8ff-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef8ff-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef8ff-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef8ff-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef8ff-131">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="ef8ff-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





