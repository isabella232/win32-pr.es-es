---
description: Imprime una página de prueba.
ms.assetid: 7968e637-9817-4111-89f5-d3c6961395e5
ms.tgt_platform: multiple
title: Método PrintTestPage de la clase Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.PrintTestPage
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: abf31237918d533ec43586ddd3d71204f2c8ae21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659759"
---
# <a name="printtestpage-method-of-the-win32_printer-class"></a><span data-ttu-id="665bc-103">Método PrintTestPage de la \_ clase Printer de Win32</span><span class="sxs-lookup"><span data-stu-id="665bc-103">PrintTestPage method of the Win32\_Printer class</span></span>

<span data-ttu-id="665bc-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PrintTestPage** imprime una página de prueba.</span><span class="sxs-lookup"><span data-stu-id="665bc-104">The **PrintTestPage** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method prints a test page.</span></span>

<span data-ttu-id="665bc-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="665bc-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="665bc-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="665bc-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="665bc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="665bc-107">Syntax</span></span>


```mof
uint32 PrintTestPage();
```



## <a name="parameters"></a><span data-ttu-id="665bc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="665bc-108">Parameters</span></span>

<span data-ttu-id="665bc-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="665bc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="665bc-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="665bc-110">Return value</span></span>

<span data-ttu-id="665bc-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="665bc-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="665bc-112">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="665bc-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="665bc-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="665bc-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="665bc-114">**0**</span><span class="sxs-lookup"><span data-stu-id="665bc-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="665bc-115">Correcto</span><span class="sxs-lookup"><span data-stu-id="665bc-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="665bc-116">**5**</span><span class="sxs-lookup"><span data-stu-id="665bc-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="665bc-117">Acceso denegado</span><span class="sxs-lookup"><span data-stu-id="665bc-117">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="665bc-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="665bc-118">Examples</span></span>

<span data-ttu-id="665bc-119">El siguiente ejemplo de código de PowerShell imprime una página de prueba.</span><span class="sxs-lookup"><span data-stu-id="665bc-119">The following PowerShell code sample prints a test page.</span></span>


```PowerShell
# Get printer objects from  WMI
$printers=Get-WmiObject Win32_Printer
"{0} Printers defined on this system" -f $printers.count

# Get a specific printer
$printer = $printers | where {$_.name -eq "\\smallguy\HP LaserJet 5M"}

# Display info
"Printer share name: {0}\{1}" -f $printer.servername, $printer.sharename
"Printer Port      : {0}    " -f $printer.PortName
  
# Print a test page
$printer.PrintTestPage()
```



## <a name="requirements"></a><span data-ttu-id="665bc-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="665bc-120">Requirements</span></span>



| <span data-ttu-id="665bc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="665bc-121">Requirement</span></span> | <span data-ttu-id="665bc-122">Value</span><span class="sxs-lookup"><span data-stu-id="665bc-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="665bc-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="665bc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="665bc-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="665bc-124">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="665bc-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="665bc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="665bc-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="665bc-126">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="665bc-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="665bc-127">Namespace</span></span><br/>                | <span data-ttu-id="665bc-128">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="665bc-128">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="665bc-129">MOF</span><span class="sxs-lookup"><span data-stu-id="665bc-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="665bc-130"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="665bc-130"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="665bc-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="665bc-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="665bc-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="665bc-132"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="665bc-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="665bc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="665bc-134">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="665bc-134">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="665bc-135">**\_Impresora Win32**</span><span class="sxs-lookup"><span data-stu-id="665bc-135">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

