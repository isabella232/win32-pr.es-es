---
description: El método de clase WMI SetDefaultPrinter establece la impresora predeterminada del sistema para el usuario que llama al método.
ms.assetid: 7e896961-363d-4b8b-9d22-bbfc9681e97b
ms.tgt_platform: multiple
title: Método SetDefaultPrinter de la clase Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetDefaultPrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a18c6d7771eb0e95d86142f41262d721509eb6f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907535"
---
# <a name="setdefaultprinter-method-of-the-win32_printer-class"></a><span data-ttu-id="c288f-103">Método SetDefaultPrinter de la \_ clase Printer de Win32</span><span class="sxs-lookup"><span data-stu-id="c288f-103">SetDefaultPrinter method of the Win32\_Printer class</span></span>

<span data-ttu-id="c288f-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultPrinter** establece la impresora predeterminada del sistema para el usuario que llama al método.</span><span class="sxs-lookup"><span data-stu-id="c288f-104">The **SetDefaultPrinter** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the default system printer for the user calling the method.</span></span>

<span data-ttu-id="c288f-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c288f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c288f-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c288f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c288f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c288f-107">Syntax</span></span>


```mof
uint32 SetDefaultPrinter();
```



## <a name="parameters"></a><span data-ttu-id="c288f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c288f-108">Parameters</span></span>

<span data-ttu-id="c288f-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c288f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c288f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c288f-110">Return value</span></span>

<span data-ttu-id="c288f-111">Devuelve 0 (cero) si es correcto y otro valor si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="c288f-111">Returns 0 (zero) if successful, and some other value if an error occurs.</span></span> <span data-ttu-id="c288f-112">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c288f-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c288f-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c288f-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

## <a name="examples"></a><span data-ttu-id="c288f-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c288f-114">Examples</span></span>

<span data-ttu-id="c288f-115">El ejemplo [instalar un puerto de impresora TCP/IP y una impresora](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) de VBScript instala un puerto de impresora TCP/IP, instala una impresora y, a continuación, establece la impresora como predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c288f-115">The [Install a TCP/IP Printer Port and Printer](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) VBScript sample installs a TCP/IP printer port, installs a printer, and then sets the printer to be default.</span></span>

<span data-ttu-id="c288f-116">En el siguiente ejemplo de código de VBScript se establece la impresora predeterminada en un equipo.</span><span class="sxs-lookup"><span data-stu-id="c288f-116">The following VBScript code sample sets the default printer on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'ScriptedPrinter'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.SetDefaultPrinter() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="c288f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c288f-117">Requirements</span></span>



| <span data-ttu-id="c288f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c288f-118">Requirement</span></span> | <span data-ttu-id="c288f-119">Value</span><span class="sxs-lookup"><span data-stu-id="c288f-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c288f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c288f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c288f-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c288f-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="c288f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c288f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c288f-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c288f-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="c288f-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c288f-124">Namespace</span></span><br/>                | <span data-ttu-id="c288f-125">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c288f-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="c288f-126">MOF</span><span class="sxs-lookup"><span data-stu-id="c288f-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c288f-127"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c288f-127"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="c288f-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c288f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c288f-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c288f-129"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="c288f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c288f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c288f-131">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="c288f-131">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="c288f-132">Tareas de WMI: impresoras e impresión</span><span class="sxs-lookup"><span data-stu-id="c288f-132">WMI Tasks: Printers and Printing</span></span>](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[<span data-ttu-id="c288f-133">**\_Impresora Win32**</span><span class="sxs-lookup"><span data-stu-id="c288f-133">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

