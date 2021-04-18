---
description: El método reanudar clase WMI continúa un trabajo de impresión en pausa.
ms.assetid: acfbca2b-19af-4339-bbca-834db50c3d8d
ms.tgt_platform: multiple
title: Método resume de la clase Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8ca1602eb29e1e18d83d2e8b79760d13f63e101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659394"
---
# <a name="resume-method-of-the-win32_printjob-class"></a><span data-ttu-id="771d1-103">Método resume de la \_ clase de Win32 PrintJob</span><span class="sxs-lookup"><span data-stu-id="771d1-103">Resume method of the Win32\_PrintJob class</span></span>

<span data-ttu-id="771d1-104">El método **reanudar** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) continúa un trabajo de impresión en pausa.</span><span class="sxs-lookup"><span data-stu-id="771d1-104">The **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method continues a paused print job.</span></span>

<span data-ttu-id="771d1-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="771d1-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="771d1-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="771d1-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="771d1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="771d1-107">Syntax</span></span>


```mof
uint32 Resume();
```



## <a name="parameters"></a><span data-ttu-id="771d1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="771d1-108">Parameters</span></span>

<span data-ttu-id="771d1-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="771d1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="771d1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="771d1-110">Return value</span></span>

<span data-ttu-id="771d1-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="771d1-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="771d1-112">**0**</span><span class="sxs-lookup"><span data-stu-id="771d1-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="771d1-113">Correcto</span><span class="sxs-lookup"><span data-stu-id="771d1-113">Success</span></span>

</dd> <dt>

<span data-ttu-id="771d1-114">**5**</span><span class="sxs-lookup"><span data-stu-id="771d1-114">**5**</span></span>
</dt> <dd>

<span data-ttu-id="771d1-115">Acceso denegado</span><span class="sxs-lookup"><span data-stu-id="771d1-115">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="771d1-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="771d1-116">Examples</span></span>

<span data-ttu-id="771d1-117">El siguiente ejemplo de código de VBScript reanuda todos los trabajos de impresión de un equipo.</span><span class="sxs-lookup"><span data-stu-id="771d1-117">The following VBScript code sample resumes all the print jobs on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Resume 
Next 
```



## <a name="requirements"></a><span data-ttu-id="771d1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="771d1-118">Requirements</span></span>



| <span data-ttu-id="771d1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="771d1-119">Requirement</span></span> | <span data-ttu-id="771d1-120">Value</span><span class="sxs-lookup"><span data-stu-id="771d1-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="771d1-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="771d1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="771d1-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="771d1-122">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="771d1-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="771d1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="771d1-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="771d1-124">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="771d1-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="771d1-125">Namespace</span></span><br/>                | <span data-ttu-id="771d1-126">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="771d1-126">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="771d1-127">MOF</span><span class="sxs-lookup"><span data-stu-id="771d1-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="771d1-128"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="771d1-128"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="771d1-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="771d1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="771d1-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="771d1-130"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="771d1-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="771d1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="771d1-132">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="771d1-132">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="771d1-133">**PrintJob de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="771d1-133">**Win32\_PrintJob**</span></span>](win32-printjob.md)
</dt> </dl>

 

