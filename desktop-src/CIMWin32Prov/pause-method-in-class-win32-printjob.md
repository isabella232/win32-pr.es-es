---
description: El método pausar clase WMI suspende un trabajo de impresión.
ms.assetid: f1e3906f-1ca2-45c0-9863-5762e4e2119a
ms.tgt_platform: multiple
title: Método PAUSE de la clase Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 785ba54b56c65fd298b6ef763ec2d7eca0d8f61a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907540"
---
# <a name="pause-method-of-the-win32_printjob-class"></a><span data-ttu-id="0d339-103">Método PAUSE de la \_ clase PrintJob de Win32</span><span class="sxs-lookup"><span data-stu-id="0d339-103">Pause method of the Win32\_PrintJob class</span></span>

<span data-ttu-id="0d339-104">El método **pausar** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) suspende un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="0d339-104">The **Pause** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method suspends a print job.</span></span>

<span data-ttu-id="0d339-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="0d339-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0d339-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0d339-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d339-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d339-107">Syntax</span></span>


```mof
uint32 Pause();
```



## <a name="parameters"></a><span data-ttu-id="0d339-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d339-108">Parameters</span></span>

<span data-ttu-id="0d339-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0d339-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0d339-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d339-110">Return value</span></span>

<span data-ttu-id="0d339-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="0d339-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0d339-112">**0**</span><span class="sxs-lookup"><span data-stu-id="0d339-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0d339-113">Correcto</span><span class="sxs-lookup"><span data-stu-id="0d339-113">Success</span></span>

</dd> <dt>

<span data-ttu-id="0d339-114">**5**</span><span class="sxs-lookup"><span data-stu-id="0d339-114">**5**</span></span>
</dt> <dd>

<span data-ttu-id="0d339-115">Acceso denegado</span><span class="sxs-lookup"><span data-stu-id="0d339-115">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="0d339-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0d339-116">Examples</span></span>

<span data-ttu-id="0d339-117">En el ejemplo de código de VBScript [pausar todas las impresoras con colas de impresión vacías](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) se usan todas las impresoras que no tienen trabajos de impresión pendientes.</span><span class="sxs-lookup"><span data-stu-id="0d339-117">The [Pause All Printers with Empty Print Queues](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) VBScript code sample pauses any printers that have no pending print jobs.</span></span>

<span data-ttu-id="0d339-118">El siguiente ejemplo de código de VBScript pone en pausa todos los trabajos de impresión en un servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="0d339-118">The following VBScript code sample pauses all the print jobs on a print server.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Pause 
Next 
```



## <a name="requirements"></a><span data-ttu-id="0d339-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d339-119">Requirements</span></span>



| <span data-ttu-id="0d339-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d339-120">Requirement</span></span> | <span data-ttu-id="0d339-121">Value</span><span class="sxs-lookup"><span data-stu-id="0d339-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d339-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d339-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0d339-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d339-123">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="0d339-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d339-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0d339-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d339-125">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="0d339-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0d339-126">Namespace</span></span><br/>                | <span data-ttu-id="0d339-127">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0d339-127">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="0d339-128">MOF</span><span class="sxs-lookup"><span data-stu-id="0d339-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d339-129"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d339-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d339-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d339-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d339-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d339-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="0d339-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d339-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d339-133">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="0d339-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="0d339-134">**PrintJob de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="0d339-134">**Win32\_PrintJob**</span></span>](win32-printjob.md)
</dt> </dl>

 

