---
description: Coloca el servicio representado por el \_ objeto PrinterDriver de Win32 en estado detenido.
ms.assetid: 0e730fe6-ff9f-4866-a255-be6d372f2d7d
ms.tgt_platform: multiple
title: Método StopService de la clase Win32_PrinterDriver (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faed7e9ed22ddcacbd8720e589463fd9a75fd87a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080205"
---
# <a name="stopservice-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="2c23a-103">Método StopService de la \_ clase PrinterDriver de Win32</span><span class="sxs-lookup"><span data-stu-id="2c23a-103">StopService method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="2c23a-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** coloca el servicio representado por el objeto [**\_ PrinterDriver de Win32**](win32-printerdriver.md) en el estado Stopped.</span><span class="sxs-lookup"><span data-stu-id="2c23a-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service represented by the [**Win32\_PrinterDriver**](win32-printerdriver.md) object in the stopped state.</span></span>

<span data-ttu-id="2c23a-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="2c23a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2c23a-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2c23a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c23a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c23a-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="2c23a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c23a-108">Parameters</span></span>

<span data-ttu-id="2c23a-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2c23a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c23a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c23a-110">Return value</span></span>

<span data-ttu-id="2c23a-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="2c23a-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="2c23a-112">Para valores distintos de los que aparecen en la lista siguiente, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="2c23a-112">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="2c23a-113">**0**</span><span class="sxs-lookup"><span data-stu-id="2c23a-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2c23a-114">El servicio se detuvo correctamente.</span><span class="sxs-lookup"><span data-stu-id="2c23a-114">Service successfully stopped.</span></span>

</dd> <dt>

<span data-ttu-id="2c23a-115">**1**</span><span class="sxs-lookup"><span data-stu-id="2c23a-115">**1**</span></span>
</dt> <dd>

<span data-ttu-id="2c23a-116">Solicitud no admitida.</span><span class="sxs-lookup"><span data-stu-id="2c23a-116">Request not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c23a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c23a-117">Requirements</span></span>



| <span data-ttu-id="2c23a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c23a-118">Requirement</span></span> | <span data-ttu-id="2c23a-119">Value</span><span class="sxs-lookup"><span data-stu-id="2c23a-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c23a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c23a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2c23a-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c23a-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="2c23a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c23a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2c23a-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c23a-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="2c23a-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2c23a-124">Namespace</span></span><br/>                | <span data-ttu-id="2c23a-125">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2c23a-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="2c23a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c23a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c23a-127"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c23a-127"><dt>Sdoias.h</dt></span></span> </dl>           |
| <span data-ttu-id="2c23a-128">MOF</span><span class="sxs-lookup"><span data-stu-id="2c23a-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c23a-129"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c23a-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c23a-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c23a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c23a-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c23a-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="2c23a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c23a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c23a-133">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="2c23a-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="2c23a-134">**Win32 \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="2c23a-134">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

