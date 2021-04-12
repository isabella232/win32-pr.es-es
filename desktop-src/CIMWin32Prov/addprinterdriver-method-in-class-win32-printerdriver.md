---
description: Crea un nuevo controlador de impresora.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Método AddPrinterDriver de la clase Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.AddPrinterDriver
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03c029d7689743150235d20b0658cd154ef64a4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423235"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="08890-103">Método AddPrinterDriver de la \_ clase PrinterDriver de Win32</span><span class="sxs-lookup"><span data-stu-id="08890-103">AddPrinterDriver method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="08890-104">El método de la clase **AddPrinterDriver** crea un nuevo controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="08890-104">The **AddPrinterDriver** class method creates a new printer driver.</span></span>

<span data-ttu-id="08890-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="08890-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="08890-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="08890-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="08890-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08890-107">Syntax</span></span>


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a><span data-ttu-id="08890-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08890-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08890-109">*DriverInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08890-109">*DriverInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08890-110">Instancia de la clase [**Win32 \_ PrinterDriver**](win32-printerdriver.md) que representa el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="08890-110">An instance of the [**Win32\_PrinterDriver**](win32-printerdriver.md) class that represents the printer driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08890-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08890-111">Return value</span></span>

<span data-ttu-id="08890-112">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="08890-112">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="08890-113">Para valores distintos de los que aparecen en la lista siguiente, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="08890-113">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="08890-114">**0**</span><span class="sxs-lookup"><span data-stu-id="08890-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="08890-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="08890-115">Success.</span></span>

</dd> <dt>

<span data-ttu-id="08890-116">**5**</span><span class="sxs-lookup"><span data-stu-id="08890-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="08890-117">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="08890-117">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="08890-118">**87**</span><span class="sxs-lookup"><span data-stu-id="08890-118">**87**</span></span>
</dt> <dd>

<span data-ttu-id="08890-119">El parámetro no es correcto.</span><span class="sxs-lookup"><span data-stu-id="08890-119">The parameter is incorrect.</span></span> <span data-ttu-id="08890-120">Puede producirse cuando el objeto no se rellena correctamente o cuando no se puede encontrar el controlador en el sistema.</span><span class="sxs-lookup"><span data-stu-id="08890-120">May occur when the object is not correctly filled or when driver can not be found in the system.</span></span> <span data-ttu-id="08890-121">Como alternativa, el atributo name puede ser diferente del modelo especificado en el archivo. inf.</span><span class="sxs-lookup"><span data-stu-id="08890-121">Alternately, the name attribute may be different than the model specified in the .inf file.</span></span> <span data-ttu-id="08890-122">O bien, es posible que falte una barra diagonal inversa (" \\ ") en un atributo PathFile.</span><span class="sxs-lookup"><span data-stu-id="08890-122">Or, there may be a missing backslash ("\\") on a PathFile attribute.</span></span>

</dd> <dt>

<span data-ttu-id="08890-123">**1797**</span><span class="sxs-lookup"><span data-stu-id="08890-123">**1797**</span></span>
</dt> <dd>

<span data-ttu-id="08890-124">Se desconoce el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="08890-124">The printer driver is unknown.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08890-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08890-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="08890-126">Al usar el método **AddPrinterDriver** , debe usar **SeLoadDriverPrivilege** para cargar o descargar un controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08890-126">When using the **AddPrinterDriver** method you must use **SeLoadDriverPrivilege** to load or unload a device driver.</span></span>

 

## <a name="examples"></a><span data-ttu-id="08890-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="08890-127">Examples</span></span>

<span data-ttu-id="08890-128">El ejemplo de código[instalar un controlador de impresora no encontrado en el archivo. cab VBScript de los controladores](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) instala una impresora hipotética con un controlador de impresión no encontrado en Drivers.cab.</span><span class="sxs-lookup"><span data-stu-id="08890-128">The[Install a Printer Driver not Found in Drivers Cab](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) VBScript code example installs a hypothetical printer using a print driver not found in Drivers.cab.</span></span>

<span data-ttu-id="08890-129">En el siguiente ejemplo de VBScript se instala el controlador de impresora para una impresora Apple LaserWriter 8500.</span><span class="sxs-lookup"><span data-stu-id="08890-129">The following VBScript sample installs the printer driver for an Apple LaserWriter 8500 printer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
objWMIService.Security_.Privileges.AddAsString "SeLoadDriverPrivilege", True 
 
Set objDriver = objWMIService.Get("Win32_PrinterDriver") 
 
objDriver.Name = "NewPrinter Model 2900" 
objDriver.SupportedPlatform = "Windows NT x86" 
objDriver.Version = "3" 
objDriver.DriverPath = "C:\Scripts\NewPrinter.dll" 
objDriver.Infname = "C:\Scripts\NewPrinter.inf" 
intResult = objDriver.AddPrinterDriver(objDriver) 
```



## <a name="requirements"></a><span data-ttu-id="08890-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08890-130">Requirements</span></span>



| <span data-ttu-id="08890-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="08890-131">Requirement</span></span> | <span data-ttu-id="08890-132">Value</span><span class="sxs-lookup"><span data-stu-id="08890-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="08890-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08890-133">Minimum supported client</span></span><br/> | <span data-ttu-id="08890-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08890-134">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="08890-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08890-135">Minimum supported server</span></span><br/> | <span data-ttu-id="08890-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08890-136">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="08890-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="08890-137">Namespace</span></span><br/>                | <span data-ttu-id="08890-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="08890-138">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="08890-139">MOF</span><span class="sxs-lookup"><span data-stu-id="08890-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08890-140"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08890-140"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="08890-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08890-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08890-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08890-142"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="08890-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="08890-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08890-144">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="08890-144">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="08890-145">**Win32 \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="08890-145">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

