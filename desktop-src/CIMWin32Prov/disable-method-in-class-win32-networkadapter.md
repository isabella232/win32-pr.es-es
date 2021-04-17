---
description: Deshabilita el adaptador de red.
ms.assetid: 6b328d7c-a9ef-4c9b-bc32-13fa2e0f65eb
ms.tgt_platform: multiple
title: Método Disable de la clase Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a9c6b1a506310460d9131709092b739f68986e02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659492"
---
# <a name="disable-method-of-the-win32_networkadapter-class"></a><span data-ttu-id="3d3a9-103">Método Disable de la \_ clase Win32 el adaptador</span><span class="sxs-lookup"><span data-stu-id="3d3a9-103">Disable method of the Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="3d3a9-104">El método **Disable** deshabilita el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="3d3a9-104">The **Disable** method disables the network adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d3a9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d3a9-105">Syntax</span></span>


```mof
uint32 Disable();
```



## <a name="parameters"></a><span data-ttu-id="3d3a9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d3a9-106">Parameters</span></span>

<span data-ttu-id="3d3a9-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3d3a9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d3a9-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d3a9-108">Return value</span></span>

<span data-ttu-id="3d3a9-109">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3d3a9-109">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="3d3a9-110">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="3d3a9-110">Any other number indicates an error.</span></span> <span data-ttu-id="3d3a9-111">Para ver los códigos de error, consulte [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3d3a9-111">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d3a9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d3a9-112">Requirements</span></span>



| <span data-ttu-id="3d3a9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d3a9-113">Requirement</span></span> | <span data-ttu-id="3d3a9-114">Value</span><span class="sxs-lookup"><span data-stu-id="3d3a9-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d3a9-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d3a9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3d3a9-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d3a9-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d3a9-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d3a9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3d3a9-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d3a9-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d3a9-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3d3a9-119">Namespace</span></span><br/>                | <span data-ttu-id="3d3a9-120">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3d3a9-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d3a9-121">MOF</span><span class="sxs-lookup"><span data-stu-id="3d3a9-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d3a9-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d3a9-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d3a9-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d3a9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d3a9-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d3a9-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d3a9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d3a9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d3a9-126">**Adaptador de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="3d3a9-126">**Win32\_NetworkAdapter**</span></span>](win32-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="3d3a9-127">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="3d3a9-127">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="3d3a9-128">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="3d3a9-128">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

