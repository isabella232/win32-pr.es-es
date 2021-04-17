---
description: El método StartService coloca el servicio en el estado Iniciado.
ms.assetid: 0f221db1-29ad-4071-98d3-6d06e4f5e026
ms.tgt_platform: multiple
title: Método StartService de la clase Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44e6fedb9e1d0edd9f355c654c7fe2cd25760ec7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659569"
---
# <a name="startservice-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="cdacc-103">Método StartService de la \_ clase PrinterDriver de Win32</span><span class="sxs-lookup"><span data-stu-id="cdacc-103">StartService method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="cdacc-104">El método **StartService** coloca el servicio en el estado Iniciado.</span><span class="sxs-lookup"><span data-stu-id="cdacc-104">The **StartService** method places the service in the started state.</span></span>

<span data-ttu-id="cdacc-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="cdacc-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cdacc-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cdacc-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cdacc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cdacc-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="cdacc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cdacc-108">Parameters</span></span>

<span data-ttu-id="cdacc-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cdacc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cdacc-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cdacc-110">Return value</span></span>

<span data-ttu-id="cdacc-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="cdacc-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="cdacc-112">Para valores distintos de los que aparecen en la lista siguiente, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="cdacc-112">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="cdacc-113">**0**</span><span class="sxs-lookup"><span data-stu-id="cdacc-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="cdacc-114">El servicio se ha iniciado correctamente.</span><span class="sxs-lookup"><span data-stu-id="cdacc-114">Service successfully started.</span></span>

</dd> <dt>

<span data-ttu-id="cdacc-115">**1**</span><span class="sxs-lookup"><span data-stu-id="cdacc-115">**1**</span></span>
</dt> <dd>

<span data-ttu-id="cdacc-116">Solicitud no admitida.</span><span class="sxs-lookup"><span data-stu-id="cdacc-116">Request not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cdacc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdacc-117">Requirements</span></span>



| <span data-ttu-id="cdacc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdacc-118">Requirement</span></span> | <span data-ttu-id="cdacc-119">Value</span><span class="sxs-lookup"><span data-stu-id="cdacc-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdacc-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdacc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cdacc-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cdacc-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="cdacc-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdacc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cdacc-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cdacc-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="cdacc-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cdacc-124">Namespace</span></span><br/>                | <span data-ttu-id="cdacc-125">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cdacc-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="cdacc-126">MOF</span><span class="sxs-lookup"><span data-stu-id="cdacc-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdacc-127"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdacc-127"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="cdacc-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cdacc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdacc-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdacc-129"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="cdacc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdacc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdacc-131">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="cdacc-131">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="cdacc-132">**Win32 \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="cdacc-132">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

