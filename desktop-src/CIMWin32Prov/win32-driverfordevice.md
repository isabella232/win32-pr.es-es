---
description: La \_ clase WMI DriverForDevice Association de Win32 relaciona una instancia de impresora con una instancia del controlador de impresora.
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Win32_DriverForDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DriverForDevice
- Win32_DriverForDevice.Antecedent
- Win32_DriverForDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5fb384eed80c6a614af448477c50be3204d3080
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659673"
---
# <a name="win32_driverfordevice-class"></a><span data-ttu-id="ee353-103">\_Clase Win32 DriverForDevice</span><span class="sxs-lookup"><span data-stu-id="ee353-103">Win32\_DriverForDevice class</span></span>

<span data-ttu-id="ee353-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DriverForDevice** Association de Win32 relaciona una instancia de impresora con una instancia del controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="ee353-104">The **Win32\_DriverForDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a printer instance to a printer driver instance.</span></span>

<span data-ttu-id="ee353-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ee353-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ee353-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="ee353-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee353-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee353-107">Syntax</span></span>

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ee353-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ee353-108">Members</span></span>

<span data-ttu-id="ee353-109">La **clase \_ DriverForDevice de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ee353-109">The **Win32\_DriverForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="ee353-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ee353-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee353-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ee353-111">Properties</span></span>

<span data-ttu-id="ee353-112">La **clase \_ DriverForDevice de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ee353-112">The **Win32\_DriverForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee353-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="ee353-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee353-114">Tipo de datos **: \_ impresora Win32**</span><span class="sxs-lookup"><span data-stu-id="ee353-114">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="ee353-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ee353-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ee353-116">Referencia a la instancia de la [**\_ impresora Win32**](win32-printer.md) que representa la impresora.</span><span class="sxs-lookup"><span data-stu-id="ee353-116">Reference to the [**Win32\_Printer**](win32-printer.md) instance that represents the printer.</span></span>

<span data-ttu-id="ee353-117">Esta propiedad se hereda de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="ee353-117">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee353-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="ee353-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee353-119">Tipo de datos: **Win32 \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="ee353-119">Data type: **Win32\_PrinterDriver**</span></span>
</dt> <dt>

<span data-ttu-id="ee353-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ee353-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee353-121">Referencia a la instancia de [**Win32 \_ PrinterDriver**](win32-printerdriver.md) que representa el controlador de impresora para la impresora.</span><span class="sxs-lookup"><span data-stu-id="ee353-121">Reference to the [**Win32\_PrinterDriver**](win32-printerdriver.md) instance that represents the printer driver for the printer.</span></span>

<span data-ttu-id="ee353-122">Esta propiedad se hereda de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="ee353-122">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee353-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee353-123">Remarks</span></span>

<span data-ttu-id="ee353-124">La **clase \_ DriverForDevice de Win32** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="ee353-124">The **Win32\_DriverForDevice** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee353-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee353-125">Requirements</span></span>



| <span data-ttu-id="ee353-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee353-126">Requirement</span></span> | <span data-ttu-id="ee353-127">Value</span><span class="sxs-lookup"><span data-stu-id="ee353-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee353-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee353-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ee353-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee353-129">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="ee353-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee353-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ee353-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee353-131">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="ee353-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ee353-132">Namespace</span></span><br/>                | <span data-ttu-id="ee353-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ee353-133">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="ee353-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ee353-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee353-135"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee353-135"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee353-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ee353-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee353-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee353-137"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ee353-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee353-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee353-139">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="ee353-139">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

