---
description: Cambia el nombre de una impresora.
ms.assetid: afbef871-5153-4b9e-9ad3-4d271a497c37
ms.tgt_platform: multiple
title: Método RenamePrinter de la clase Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.RenamePrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6066dfd4280f7c43c9804933fb1ed5fb931bfa08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274831"
---
# <a name="renameprinter-method-of-the-win32_printer-class"></a><span data-ttu-id="1ca3f-103">Método RenamePrinter de la \_ clase Printer de Win32</span><span class="sxs-lookup"><span data-stu-id="1ca3f-103">RenamePrinter method of the Win32\_Printer class</span></span>

<span data-ttu-id="1ca3f-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **RenamePrinter** cambia el nombre de una impresora.</span><span class="sxs-lookup"><span data-stu-id="1ca3f-104">The **RenamePrinter** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames a printer.</span></span>

<span data-ttu-id="1ca3f-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="1ca3f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1ca3f-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1ca3f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1ca3f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ca3f-107">Syntax</span></span>


```mof
uint32 RenamePrinter(
  [in] string NewPrinterName
);
```



## <a name="parameters"></a><span data-ttu-id="1ca3f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ca3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ca3f-109">*NewPrinterName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1ca3f-109">*NewPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca3f-110">Nuevo nombre de impresora.</span><span class="sxs-lookup"><span data-stu-id="1ca3f-110">New printer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ca3f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ca3f-111">Return value</span></span>

<span data-ttu-id="1ca3f-112">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="1ca3f-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="1ca3f-113">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1ca3f-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1ca3f-114">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1ca3f-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1ca3f-115">**0**</span><span class="sxs-lookup"><span data-stu-id="1ca3f-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1ca3f-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="1ca3f-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="1ca3f-117">**5**</span><span class="sxs-lookup"><span data-stu-id="1ca3f-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="1ca3f-118">Acceso denegado</span><span class="sxs-lookup"><span data-stu-id="1ca3f-118">Access Denied</span></span>

</dd> <dt>

<span data-ttu-id="1ca3f-119">**1801**</span><span class="sxs-lookup"><span data-stu-id="1ca3f-119">**1801**</span></span>
</dt> <dd>

<span data-ttu-id="1ca3f-120">Nombre de impresora no válido</span><span class="sxs-lookup"><span data-stu-id="1ca3f-120">Invalid Printer Name</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="1ca3f-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1ca3f-121">Examples</span></span>

<span data-ttu-id="1ca3f-122">En el siguiente ejemplo de VBScript se cambia el nombre de una impresora y su nombre de recurso compartido de impresora.</span><span class="sxs-lookup"><span data-stu-id="1ca3f-122">The following VBScript example renames both a printer and its printer share name.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where DeviceID = 'HP LaserJet 4Si M'") 
 
For Each objPrinter in colPrinters 
    objPrinter.RenamePrinter("ArtDepartmentPrinter") 
Next 
 
Set colPrinters = objWMIService.ExecQuery _ 
    ("Select * From Win32_Printer Where DeviceID = 'ArtDepartmentPrinter' ") 
 
For Each objPrinter in colPrinters 
    objPrinter.ShareName = "ArtDepartmentPrinter" 
    objPrinter.Put_ 
Next 
```



## <a name="requirements"></a><span data-ttu-id="1ca3f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ca3f-123">Requirements</span></span>



| <span data-ttu-id="1ca3f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ca3f-124">Requirement</span></span> | <span data-ttu-id="1ca3f-125">Value</span><span class="sxs-lookup"><span data-stu-id="1ca3f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ca3f-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ca3f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1ca3f-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ca3f-127">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="1ca3f-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ca3f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1ca3f-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ca3f-129">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="1ca3f-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1ca3f-130">Namespace</span></span><br/>                | <span data-ttu-id="1ca3f-131">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1ca3f-131">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="1ca3f-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1ca3f-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ca3f-133"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ca3f-133"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ca3f-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1ca3f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ca3f-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ca3f-135"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="1ca3f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ca3f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ca3f-137">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="1ca3f-137">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1ca3f-138">**\_Impresora Win32**</span><span class="sxs-lookup"><span data-stu-id="1ca3f-138">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

