---
description: La \_ clase WMI PrinterDriverDll Association de Win32 relaciona una impresora local con su archivo de controlador.
ms.assetid: decbd1de-8091-47f7-94a1-42862070b920
ms.tgt_platform: multiple
title: Win32_PrinterDriverDll (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriverDll
- Win32_PrinterDriverDll.Antecedent
- Win32_PrinterDriverDll.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41484c39d9e1b59efd79d7aee08719b3a241de97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496523"
---
# <a name="win32_printerdriverdll-class"></a><span data-ttu-id="5e330-103">\_Clase Win32 PrinterDriverDll</span><span class="sxs-lookup"><span data-stu-id="5e330-103">Win32\_PrinterDriverDll class</span></span>

<span data-ttu-id="5e330-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PrinterDriverDll** Association de Win32 relaciona una impresora local con su archivo de controlador.</span><span class="sxs-lookup"><span data-stu-id="5e330-104">The **Win32\_PrinterDriverDll** association [WMI class](../wmisdk/retrieving-a-class.md) relates a local printer and its driver file.</span></span>

<span data-ttu-id="5e330-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5e330-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5e330-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5e330-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e330-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e330-107">Syntax</span></span>

``` syntax
class Win32_PrinterDriverDll : CIM_Dependency
{
  CIM_DataFile  REF Antecedent;
  Win32_Printer REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5e330-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e330-108">Members</span></span>

<span data-ttu-id="5e330-109">La **clase \_ PrinterDriverDll de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5e330-109">The **Win32\_PrinterDriverDll** class has these types of members:</span></span>

-   [<span data-ttu-id="5e330-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e330-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e330-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e330-111">Properties</span></span>

<span data-ttu-id="5e330-112">La **clase \_ PrinterDriverDll de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5e330-112">The **Win32\_PrinterDriverDll** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e330-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5e330-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e330-114">Tipo de datos **: \_ archivo** de datos CIM</span><span class="sxs-lookup"><span data-stu-id="5e330-114">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="5e330-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e330-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e330-116">Calificadores: [ **clave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5e330-116">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5e330-117">Referencia a la instancia de [**\_ archivo de archivos CIM**](cim-datafile.md) que representa el archivo del controlador para esta impresora basada en Windows.</span><span class="sxs-lookup"><span data-stu-id="5e330-117">Reference to the [**CIM\_DataFile**](cim-datafile.md) instance representing the driver file for this Windows-based printer.</span></span>

<span data-ttu-id="5e330-118">Esta propiedad se hereda de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5e330-118">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e330-119">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="5e330-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e330-120">Tipo de datos **: \_ impresora Win32**</span><span class="sxs-lookup"><span data-stu-id="5e330-120">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="5e330-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e330-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e330-122">Calificadores: [ **clave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5e330-122">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5e330-123">Referencia a la instancia de [**\_ impresora de Win32**](win32-printer.md) .</span><span class="sxs-lookup"><span data-stu-id="5e330-123">Reference to the [**Win32\_Printer**](win32-printer.md) instance.</span></span>

<span data-ttu-id="5e330-124">Esta propiedad se hereda de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5e330-124">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e330-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e330-125">Remarks</span></span>

<span data-ttu-id="5e330-126">La **clase \_ PrinterDriverDll de Win32** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5e330-126">The **Win32\_PrinterDriverDll** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e330-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e330-127">Requirements</span></span>



| <span data-ttu-id="5e330-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e330-128">Requirement</span></span> | <span data-ttu-id="5e330-129">Value</span><span class="sxs-lookup"><span data-stu-id="5e330-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e330-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e330-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5e330-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e330-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="5e330-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e330-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5e330-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e330-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="5e330-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5e330-134">Namespace</span></span><br/>                | <span data-ttu-id="5e330-135">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5e330-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="5e330-136">MOF</span><span class="sxs-lookup"><span data-stu-id="5e330-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e330-137"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e330-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e330-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e330-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e330-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e330-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="5e330-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e330-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e330-141">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="5e330-141">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="5e330-142">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="5e330-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
