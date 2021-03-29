---
description: Quita todos los trabajos, incluido el que imprime actualmente de la cola.
ms.assetid: d7466513-b123-43af-ab17-b3213ba80284
ms.tgt_platform: multiple
title: Método CancelAllJobs de la clase Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.CancelAllJobs
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d2d816dab837aafd7b6e9c6beff75c4e62b19b2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907049"
---
# <a name="cancelalljobs-method-of-the-win32_printer-class"></a><span data-ttu-id="c016b-103">Método CancelAllJobs de la \_ clase Printer de Win32</span><span class="sxs-lookup"><span data-stu-id="c016b-103">CancelAllJobs method of the Win32\_Printer class</span></span>

<span data-ttu-id="c016b-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CancelAllJobs** quita todos los trabajos, incluido el que se imprime actualmente de la cola.</span><span class="sxs-lookup"><span data-stu-id="c016b-104">The **CancelAllJobs** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method removes all jobs, including the one currently printing from the queue.</span></span>

<span data-ttu-id="c016b-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c016b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c016b-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c016b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c016b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c016b-107">Syntax</span></span>


```mof
uint32 CancelAllJobs();
```



## <a name="parameters"></a><span data-ttu-id="c016b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c016b-108">Parameters</span></span>

<span data-ttu-id="c016b-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c016b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c016b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c016b-110">Return value</span></span>

<span data-ttu-id="c016b-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="c016b-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="c016b-112">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c016b-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c016b-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c016b-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c016b-114">**0**</span><span class="sxs-lookup"><span data-stu-id="c016b-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c016b-115">Correcto</span><span class="sxs-lookup"><span data-stu-id="c016b-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="c016b-116">**5**</span><span class="sxs-lookup"><span data-stu-id="c016b-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c016b-117">Acceso denegado</span><span class="sxs-lookup"><span data-stu-id="c016b-117">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c016b-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c016b-118">Examples</span></span>

<span data-ttu-id="c016b-119">El mensaje [notificar a los usuarios cuando se purgue una cola de impresión](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) utiliza Msg.exe para enviar una alerta de red a los usuarios que tengan documentos en una cola de impresión que se va a purgar.</span><span class="sxs-lookup"><span data-stu-id="c016b-119">The [Notify Users When a Print Queue is Purged](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) uses Msg.exe to send a network alert to any users who had documents in a print queue about to be purged.</span></span> <span data-ttu-id="c016b-120">Después de enviar las alertas, el script purga la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="c016b-120">After sending the alerts, the script purges the print queue.</span></span>

<span data-ttu-id="c016b-121">El ejemplo de código de VBScript [eliminar todos los trabajos de impresión](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) elimina todos los trabajos de impresión en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="c016b-121">The [Delete all print jobs](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) VBScript code sample deletes all print jobs on the local computer.</span></span>

<span data-ttu-id="c016b-122">El siguiente ejemplo de VBScript elimina todos los trabajos de impresión de una impresora denominada HP QuietJet.</span><span class="sxs-lookup"><span data-stu-id="c016b-122">The following VBScript sample deletes all the print jobs for a printer named HP QuietJet.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'HP QuietJet'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.CancelAllJobs() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="c016b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c016b-123">Requirements</span></span>



| <span data-ttu-id="c016b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c016b-124">Requirement</span></span> | <span data-ttu-id="c016b-125">Value</span><span class="sxs-lookup"><span data-stu-id="c016b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c016b-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c016b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c016b-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c016b-127">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="c016b-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c016b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c016b-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c016b-129">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="c016b-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c016b-130">Namespace</span></span><br/>                | <span data-ttu-id="c016b-131">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c016b-131">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="c016b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c016b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c016b-133"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c016b-133"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="c016b-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c016b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c016b-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c016b-135"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="c016b-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="c016b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c016b-137">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="c016b-137">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="c016b-138">**\_Impresora Win32**</span><span class="sxs-lookup"><span data-stu-id="c016b-138">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

