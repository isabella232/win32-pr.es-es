---
title: Códigos de error (UIAutomationCoreApi. h)
description: En este tema se describen los códigos de error expuestos por la automatización de la interfaz de usuario de Microsoft.
ms.assetid: f7820aa3-908e-426e-851c-84397019d735
topic_type:
- apiref
api_name:
- UIA_E_ELEMENTNOTAVAILABLE
- UIA_E_ELEMENTNOTENABLED
- UIA_E_INVALIDOPERATION
- UIA_E_NOCLICKABLEPOINT
- UIA_E_NOTSUPPORTED
- UIA_E_PROXYASSEMBLYNOTLOADED
- UIA_E_TIMEOUT
api_location:
- UIAutomationCoreApi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaa03746bfb1a5e56fcac8b39d326581159f459
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078796"
---
# <a name="error-codes-uiautomationcoreapih"></a><span data-ttu-id="430b3-103">Códigos de error (UIAutomationCoreApi. h)</span><span class="sxs-lookup"><span data-stu-id="430b3-103">Error Codes (UIAutomationCoreApi.h)</span></span>

<span data-ttu-id="430b3-104">En este tema se describen los códigos de error expuestos por la automatización de la interfaz de usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="430b3-104">This topic describes the error codes exposed by Microsoft UI Automation.</span></span> <span data-ttu-id="430b3-105">La lista está ordenada alfabéticamente por nombre.</span><span class="sxs-lookup"><span data-stu-id="430b3-105">The list is sorted alphabetically by name.</span></span>



| <span data-ttu-id="430b3-106">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="430b3-106">Constant/value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="430b3-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="430b3-107">Description</span></span>                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <span data-ttu-id="430b3-108"><dt>**UIA \_ E \_ ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="430b3-108"><dt>**UIA\_E\_ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt></span></span> </dl>          | <span data-ttu-id="430b3-109">Indica que se llamó a un método en un elemento virtualizado o en un elemento que ya no existe, normalmente porque se ha destruido.</span><span class="sxs-lookup"><span data-stu-id="430b3-109">Indicates that a method was called on a virtualized element, or on an element that no longer exists, usually because it has been destroyed.</span></span> <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <span data-ttu-id="430b3-110"><dt>**UIA \_ E \_ ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt></span><span class="sxs-lookup"><span data-stu-id="430b3-110"><dt>**UIA\_E\_ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt></span></span> </dl>                | <span data-ttu-id="430b3-111">Indica que se ha llamado a un método que requiere un elemento habilitado, como [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) o [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), en un elemento que se ha deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="430b3-111">Indicates that a method that requires an enabled element, such as [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) or [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), was called on an element that was disabled.</span></span> <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <span data-ttu-id="430b3-112"><dt>**UIA \_ E \_ INVALIDOPERATION**</dt> <dt>0x80131509</dt></span><span class="sxs-lookup"><span data-stu-id="430b3-112"><dt>**UIA\_E\_INVALIDOPERATION**</dt> <dt>0x80131509</dt></span></span> </dl>                   | <span data-ttu-id="430b3-113">Indica que el método intentó realizar una operación que no era válida.</span><span class="sxs-lookup"><span data-stu-id="430b3-113">Indicates that the method attempted an operation that was not valid.</span></span><br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <span data-ttu-id="430b3-114"><dt>**UIA \_ E \_ NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="430b3-114"><dt>**UIA\_E\_NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt></span></span> </dl>                   | <span data-ttu-id="430b3-115">Indica que se llamó al método [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) en un elemento que no tiene ningún punto en el que hacer clic.</span><span class="sxs-lookup"><span data-stu-id="430b3-115">Indicates that the [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) method was called on an element that has no clickable point.</span></span><br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <span data-ttu-id="430b3-116"><dt>**UIA \_ E \_ NOTSUPPORTED**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="430b3-116"><dt>**UIA\_E\_NOTSUPPORTED**</dt> <dt>0x80040204</dt></span></span> </dl>                               | <span data-ttu-id="430b3-117">Indica que el proveedor no admite explícitamente la propiedad o el patrón de control especificados.</span><span class="sxs-lookup"><span data-stu-id="430b3-117">Indicates that the provider explicitly does not support the specified property or control pattern.</span></span> <span data-ttu-id="430b3-118">La automatización de la interfaz de usuario devolverá este código de error al autor de la llamada sin intentar proporcionar un valor predeterminado o revertir a otro proveedor.</span><span class="sxs-lookup"><span data-stu-id="430b3-118">UI Automation will return this error code to the caller without attempting to provide a default value or falling back to another provider.</span></span><br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <span data-ttu-id="430b3-119"><dt>**UIA \_ E \_ PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="430b3-119"><dt>**UIA\_E\_PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt></span></span> </dl> | <span data-ttu-id="430b3-120">Indica que se produjo un problema al cargar un ensamblado que contiene un proveedor del lado cliente (proxy).</span><span class="sxs-lookup"><span data-stu-id="430b3-120">Indicates that a problem occurred when loading an assembly that contains a client-side (proxy) provider.</span></span><br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <span data-ttu-id="430b3-121"><dt>**UIA \_ E \_**</dt> <dt>0x80131505</dt> de tiempo de espera</span><span class="sxs-lookup"><span data-stu-id="430b3-121"><dt>**UIA\_E\_TIMEOUT**</dt> <dt>0x80131505</dt></span></span> </dl>                                                      | <span data-ttu-id="430b3-122">Indica que ha expirado la hora asignada para un proceso u operación.</span><span class="sxs-lookup"><span data-stu-id="430b3-122">Indicates that the time allotted for a process or operation has expired.</span></span><br/>                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="430b3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="430b3-123">Requirements</span></span>



| <span data-ttu-id="430b3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="430b3-124">Requirement</span></span> | <span data-ttu-id="430b3-125">Value</span><span class="sxs-lookup"><span data-stu-id="430b3-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="430b3-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="430b3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="430b3-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="430b3-127">Windows XP \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="430b3-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="430b3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="430b3-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="430b3-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="430b3-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="430b3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="430b3-131"><dt>UIAutomationCoreApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="430b3-131"><dt>UIAutomationCoreApi.h</dt></span></span> </dl> |



 

 





