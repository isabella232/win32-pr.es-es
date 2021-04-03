---
description: La \_ clase WMI PrinterShare Association de Win32 relaciona una impresora local y el recurso compartido que la representa como se ve a través de una red.
ms.assetid: 9ac99e52-5e8f-4329-960f-7bd1fd229e37
ms.tgt_platform: multiple
title: Win32_PrinterShare (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterShare
- Win32_PrinterShare.Antecedent
- Win32_PrinterShare.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57bc15fc5d3db78179335b039851d7d3b7cbf8a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907414"
---
# <a name="win32_printershare-class"></a><span data-ttu-id="805b8-103">\_Clase Win32 PrinterShare</span><span class="sxs-lookup"><span data-stu-id="805b8-103">Win32\_PrinterShare class</span></span>

<span data-ttu-id="805b8-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PrinterShare** Association de Win32 relaciona una impresora local y el recurso compartido que la representa como se ve a través de una red.</span><span class="sxs-lookup"><span data-stu-id="805b8-104">The **Win32\_PrinterShare** association [WMI class](../wmisdk/retrieving-a-class.md) relates a local printer and the share that represents it as it is viewed over a network.</span></span>

<span data-ttu-id="805b8-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="805b8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="805b8-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="805b8-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="805b8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="805b8-107">Syntax</span></span>

``` syntax
class Win32_PrinterShare : CIM_Dependency
{
  Win32_Printer REF Antecedent;
  Win32_Share   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="805b8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="805b8-108">Members</span></span>

<span data-ttu-id="805b8-109">La **clase \_ PrinterShare de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="805b8-109">The **Win32\_PrinterShare** class has these types of members:</span></span>

-   [<span data-ttu-id="805b8-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="805b8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="805b8-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="805b8-111">Properties</span></span>

<span data-ttu-id="805b8-112">La **clase \_ PrinterShare de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="805b8-112">The **Win32\_PrinterShare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="805b8-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="805b8-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="805b8-114">Tipo de datos **: \_ impresora Win32**</span><span class="sxs-lookup"><span data-stu-id="805b8-114">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="805b8-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="805b8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="805b8-116">Calificadores: [ **clave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="805b8-116">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="805b8-117">Referencia a la instancia de que representa la impresora local compartida en esta asociación.</span><span class="sxs-lookup"><span data-stu-id="805b8-117">Reference to the instance representing the local printer shared in this association.</span></span>

</dd> <dt>

<span data-ttu-id="805b8-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="805b8-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="805b8-119">Tipo de datos **: \_ recurso compartido de Win32**</span><span class="sxs-lookup"><span data-stu-id="805b8-119">Data type: **Win32\_Share**</span></span>
</dt> <dt>

<span data-ttu-id="805b8-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="805b8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="805b8-121">Calificadores: [ **clave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="805b8-121">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="805b8-122">Referencia a la instancia de que representa el recurso compartido de la impresora en esta asociación.</span><span class="sxs-lookup"><span data-stu-id="805b8-122">Reference to the instance representing the share of the printer in this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="805b8-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="805b8-123">Remarks</span></span>

<span data-ttu-id="805b8-124">La **clase \_ PrinterShare de Win32** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="805b8-124">The **Win32\_PrinterShare** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="805b8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="805b8-125">Requirements</span></span>



| <span data-ttu-id="805b8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="805b8-126">Requirement</span></span> | <span data-ttu-id="805b8-127">Value</span><span class="sxs-lookup"><span data-stu-id="805b8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="805b8-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="805b8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="805b8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="805b8-129">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="805b8-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="805b8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="805b8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="805b8-131">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="805b8-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="805b8-132">Namespace</span></span><br/>                | <span data-ttu-id="805b8-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="805b8-133">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="805b8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="805b8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="805b8-135"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="805b8-135"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="805b8-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="805b8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="805b8-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="805b8-137"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="805b8-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="805b8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805b8-139">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="805b8-139">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
