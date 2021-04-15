---
title: Método SetServiceLocation de la clase Win32_SessionDirectoryVMMPlugin
description: Establece la ubicación del servicio para el complemento.
ms.assetid: e886a40b-9ea9-4159-a2ea-776160559410
ms.tgt_platform: multiple
keywords:
- Método SetServiceLocation Servicios de Escritorio remoto
- Método SetServiceLocation Servicios de Escritorio remoto, clase Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de clase Servicios de Escritorio remoto, método SetServiceLocation
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetServiceLocation
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c16a6bbe802052f53d28d4cd8cc2b9ab559b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534551"
---
# <a name="setservicelocation-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="443d4-106">Método SetServiceLocation de la \_ clase SessionDirectoryVMMPlugin de Win32</span><span class="sxs-lookup"><span data-stu-id="443d4-106">SetServiceLocation method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="443d4-107">Establece la ubicación del servicio para el complemento.</span><span class="sxs-lookup"><span data-stu-id="443d4-107">Sets the service location for the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="443d4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="443d4-108">Syntax</span></span>


```mof
uint32 SetServiceLocation(
  [in] string sServiceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="443d4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="443d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="443d4-110">*sServiceLocation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="443d4-110">*sServiceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="443d4-111">La ubicación del servicio en la que debe ponerse en contacto el complemento.</span><span class="sxs-lookup"><span data-stu-id="443d4-111">The service location that the plug-in should contact.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="443d4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="443d4-112">Return value</span></span>

<span data-ttu-id="443d4-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="443d4-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="443d4-114">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="443d4-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="443d4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="443d4-115">Requirements</span></span>



| <span data-ttu-id="443d4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="443d4-116">Requirement</span></span> | <span data-ttu-id="443d4-117">Value</span><span class="sxs-lookup"><span data-stu-id="443d4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="443d4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="443d4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="443d4-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="443d4-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="443d4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="443d4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="443d4-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="443d4-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="443d4-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="443d4-122">Namespace</span></span><br/>                | <span data-ttu-id="443d4-123">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="443d4-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="443d4-124">MOF</span><span class="sxs-lookup"><span data-stu-id="443d4-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="443d4-125"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="443d4-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="443d4-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="443d4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="443d4-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="443d4-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="443d4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="443d4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="443d4-129">**Win32 \_ SessionDirectoryVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="443d4-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





