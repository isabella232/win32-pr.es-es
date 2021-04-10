---
description: Proporciona una conexión a una impresora existente en la red y la agrega a la lista de impresoras disponibles.
ms.assetid: 44149051-4abf-4428-8999-355dd0b0ce69
ms.tgt_platform: multiple
title: Método AddPrinterConnection de la clase Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.AddPrinterConnection
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2ad9e225a60e33fdf51d5f677dd4342acd148b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907052"
---
# <a name="addprinterconnection-method-of-the-win32_printer-class"></a><span data-ttu-id="116c3-103">Método AddPrinterConnection de la \_ clase Printer de Win32</span><span class="sxs-lookup"><span data-stu-id="116c3-103">AddPrinterConnection method of the Win32\_Printer class</span></span>

<span data-ttu-id="116c3-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AddPrinterConnection** proporciona una conexión a una impresora existente en la red y la agrega a la lista de impresoras disponibles.</span><span class="sxs-lookup"><span data-stu-id="116c3-104">The **AddPrinterConnection** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method provides a connection to an existing printer on the network, and adds it to the list of available printers.</span></span>

<span data-ttu-id="116c3-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="116c3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="116c3-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="116c3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="116c3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="116c3-107">Syntax</span></span>


```mof
uint32 AddPrinterConnection(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="116c3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="116c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="116c3-109">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="116c3-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="116c3-110">Nombre descriptivo de la impresora.</span><span class="sxs-lookup"><span data-stu-id="116c3-110">Friendly name for the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="116c3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="116c3-111">Return value</span></span>

<span data-ttu-id="116c3-112">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="116c3-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="116c3-113">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="116c3-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="116c3-114">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="116c3-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="116c3-115">**0**</span><span class="sxs-lookup"><span data-stu-id="116c3-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="116c3-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="116c3-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="116c3-117">**5**</span><span class="sxs-lookup"><span data-stu-id="116c3-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="116c3-118">Acceso denegado</span><span class="sxs-lookup"><span data-stu-id="116c3-118">Access Denied</span></span>

</dd> <dt>

<span data-ttu-id="116c3-119">**1801**</span><span class="sxs-lookup"><span data-stu-id="116c3-119">**1801**</span></span>
</dt> <dd>

<span data-ttu-id="116c3-120">Nombre de impresora no válido</span><span class="sxs-lookup"><span data-stu-id="116c3-120">Invalid Printer Name</span></span>

</dd> <dt>

<span data-ttu-id="116c3-121">**1930**</span><span class="sxs-lookup"><span data-stu-id="116c3-121">**1930**</span></span>
</dt> <dd>

<span data-ttu-id="116c3-122">Controlador de impresora incompatible</span><span class="sxs-lookup"><span data-stu-id="116c3-122">Incompatible Printer Driver</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="116c3-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="116c3-123">Examples</span></span>

<span data-ttu-id="116c3-124">El ejemplo de PowerShell [Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) instala todos los controladores de impresora desde un servidor de impresión especificado.</span><span class="sxs-lookup"><span data-stu-id="116c3-124">The [Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) PowerShell sample installs all printer drivers from a specified print server.</span></span>

<span data-ttu-id="116c3-125">En el ejemplo de PowerShell de [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) se enumeran las impresoras compartidas de un equipo remoto y se ofrece la posibilidad de agregar una conexión de impresora desde el equipo remoto al equipo.</span><span class="sxs-lookup"><span data-stu-id="116c3-125">The [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) PowerShell sample lists shared printers on a remote comptuer, and gives you the ability to add a printer connection from the remote computer to your computer.</span></span>

<span data-ttu-id="116c3-126">El siguiente ejemplo de código de VBScript agrega una impresora local.</span><span class="sxs-lookup"><span data-stu-id="116c3-126">The following VBScript code sample adds a local printer.</span></span>


```VB
Dim strPrinterName as String = "Isidoros Printer"
Dim strComputer AsString = My.Computer.Name
Dim objWMIService, objPrinter AsObject
objWMIService = GetObject(
"winmgmts:" _

& 
"{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

objPrinter = objWMIService.Get(
"Win32_Printer").SpawnInstance_
objPrinter.Name = strPrinterName
objPrinter.DriverName = "Generic / Text Only"
objPrinter.PortName = 
"c:\temp\file.prn"
objPrinter.DeviceID = strPrinterName
'objPrinter.Location = "Athens, Greece"
objPrinter.Network = 
False
objPrinter.Shared = 
False'objPrinter.ShareName = "MyShareName"
objPrinter.Put_()
```



## <a name="requirements"></a><span data-ttu-id="116c3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="116c3-127">Requirements</span></span>



| <span data-ttu-id="116c3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="116c3-128">Requirement</span></span> | <span data-ttu-id="116c3-129">Value</span><span class="sxs-lookup"><span data-stu-id="116c3-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="116c3-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="116c3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="116c3-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="116c3-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="116c3-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="116c3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="116c3-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="116c3-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="116c3-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="116c3-134">Namespace</span></span><br/>                | <span data-ttu-id="116c3-135">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="116c3-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="116c3-136">MOF</span><span class="sxs-lookup"><span data-stu-id="116c3-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="116c3-137"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="116c3-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="116c3-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="116c3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="116c3-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="116c3-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="116c3-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="116c3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="116c3-141">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="116c3-141">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="116c3-142">Tareas de WMI: impresoras e impresión</span><span class="sxs-lookup"><span data-stu-id="116c3-142">WMI Tasks: Printers and Printing</span></span>](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[<span data-ttu-id="116c3-143">**\_Impresora Win32**</span><span class="sxs-lookup"><span data-stu-id="116c3-143">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

