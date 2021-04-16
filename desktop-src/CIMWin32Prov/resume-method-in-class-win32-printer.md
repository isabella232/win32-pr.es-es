---
description: Reanuda una cola de impresión en pausa.
ms.assetid: 6d6d21e9-f469-4e2c-9a89-3e9febe229fc
ms.tgt_platform: multiple
title: Método resume de la clase Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3eca8849fd1c5c449261dac1a9530f4da42e9482
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659436"
---
# <a name="resume-method-of-the-win32_printer-class"></a><span data-ttu-id="32797-103">Método resume de la \_ clase Printer de Win32</span><span class="sxs-lookup"><span data-stu-id="32797-103">Resume method of the Win32\_Printer class</span></span>

<span data-ttu-id="32797-104">El método **reanudar** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) reanuda una cola de impresión en pausa.</span><span class="sxs-lookup"><span data-stu-id="32797-104">The **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method resumes a paused print queue.</span></span>

<span data-ttu-id="32797-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="32797-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="32797-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="32797-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="32797-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32797-107">Syntax</span></span>


```mof
uint32 Resume();
```



## <a name="parameters"></a><span data-ttu-id="32797-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32797-108">Parameters</span></span>

<span data-ttu-id="32797-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="32797-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32797-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32797-110">Return value</span></span>

<span data-ttu-id="32797-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="32797-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="32797-112">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="32797-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="32797-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="32797-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="32797-114">**0**</span><span class="sxs-lookup"><span data-stu-id="32797-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="32797-115">Correcto</span><span class="sxs-lookup"><span data-stu-id="32797-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="32797-116">**5**</span><span class="sxs-lookup"><span data-stu-id="32797-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="32797-117">Acceso denegado</span><span class="sxs-lookup"><span data-stu-id="32797-117">Access Denied</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32797-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32797-118">Requirements</span></span>



| <span data-ttu-id="32797-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="32797-119">Requirement</span></span> | <span data-ttu-id="32797-120">Value</span><span class="sxs-lookup"><span data-stu-id="32797-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="32797-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32797-121">Minimum supported client</span></span><br/> | <span data-ttu-id="32797-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32797-122">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="32797-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32797-123">Minimum supported server</span></span><br/> | <span data-ttu-id="32797-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32797-124">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="32797-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="32797-125">Namespace</span></span><br/>                | <span data-ttu-id="32797-126">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="32797-126">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="32797-127">MOF</span><span class="sxs-lookup"><span data-stu-id="32797-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32797-128"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32797-128"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="32797-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32797-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32797-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32797-130"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="32797-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="32797-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32797-132">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="32797-132">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="32797-133">**\_Impresora Win32**</span><span class="sxs-lookup"><span data-stu-id="32797-133">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="32797-134">**PAUSE (método)**</span><span class="sxs-lookup"><span data-stu-id="32797-134">**Pause Method**</span></span>](pause-method-in-class-win32-printer.md)
</dt> </dl>

 

