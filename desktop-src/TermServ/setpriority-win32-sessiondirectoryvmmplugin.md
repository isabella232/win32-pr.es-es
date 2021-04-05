---
title: Método SetPriority de la clase Win32_SessionDirectoryVMMPlugin
description: Establece la prioridad del complemento.
ms.assetid: ddcf30cd-b87c-4869-80fc-ec92092e0df3
ms.tgt_platform: multiple
keywords:
- SetPriority (método) Servicios de Escritorio remoto
- Método SetPriority Servicios de Escritorio remoto, clase Win32_SessionDirectoryVMMPlugin
- Clase Win32_SessionDirectoryVMMPlugin Servicios de Escritorio remoto, método SetPriority
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetPriority
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d20dbc4af332d0c658f819f8e47f5b3eb4e95b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997075"
---
# <a name="setpriority-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="cfde3-106">Método SetPriority de la \_ clase Win32 SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="cfde3-106">SetPriority method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="cfde3-107">Establece la prioridad del complemento.</span><span class="sxs-lookup"><span data-stu-id="cfde3-107">Sets the priority of the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfde3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfde3-108">Syntax</span></span>


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a><span data-ttu-id="cfde3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfde3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfde3-110">*Prioridad* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="cfde3-110">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfde3-111">Prioridad del complemento.</span><span class="sxs-lookup"><span data-stu-id="cfde3-111">The priority of the plug-in.</span></span> <span data-ttu-id="cfde3-112">Cuanto mayor sea el valor, mayor será la prioridad del complemento.</span><span class="sxs-lookup"><span data-stu-id="cfde3-112">The higher the value, the higher the priority of the plug-in.</span></span> <span data-ttu-id="cfde3-113">De forma predeterminada, la prioridad es cero.</span><span class="sxs-lookup"><span data-stu-id="cfde3-113">The priority is zero by default.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfde3-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfde3-114">Return value</span></span>

<span data-ttu-id="cfde3-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="cfde3-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="cfde3-116">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="cfde3-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfde3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfde3-117">Requirements</span></span>



| <span data-ttu-id="cfde3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfde3-118">Requirement</span></span> | <span data-ttu-id="cfde3-119">Value</span><span class="sxs-lookup"><span data-stu-id="cfde3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfde3-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfde3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cfde3-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cfde3-121">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cfde3-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfde3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cfde3-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cfde3-123">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="cfde3-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cfde3-124">Namespace</span></span><br/>                | <span data-ttu-id="cfde3-125">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cfde3-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="cfde3-126">MOF</span><span class="sxs-lookup"><span data-stu-id="cfde3-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfde3-127"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfde3-127"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfde3-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cfde3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfde3-129"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfde3-129"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfde3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfde3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfde3-131">**Win32 \_ SessionDirectoryVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="cfde3-131">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





