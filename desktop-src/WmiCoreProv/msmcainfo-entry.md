---
description: Indica una entrada de información de MCA, corrección de máquina corregida (CMC) o error de plataforma corregida (CPE). Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: MSMCAInfo_Entry (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_Entry
- MSMCAInfo_Entry.Data
- MSMCAInfo_Entry.Length
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cda6abba06dc4d4f3fec3a4763391eee1fa81274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716707"
---
# <a name="msmcainfo_entry-class"></a><span data-ttu-id="594b4-104">\_Clase de entrada MSMCAInfo</span><span class="sxs-lookup"><span data-stu-id="594b4-104">MSMCAInfo\_Entry class</span></span>

<span data-ttu-id="594b4-105">La clase de **\_ entrada MSMCAInfo** indica una entrada de información de MCA, corrección de máquina corregida (CMC) o error de plataforma corregida (CPE).</span><span class="sxs-lookup"><span data-stu-id="594b4-105">The **MSMCAInfo\_Entry** class indicates an MCA, corrected machine check (CMC), or corrected platform error (CPE) information entry.</span></span> <span data-ttu-id="594b4-106">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="594b4-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="594b4-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="594b4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="594b4-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="594b4-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="594b4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="594b4-109">Syntax</span></span>

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a><span data-ttu-id="594b4-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="594b4-110">Members</span></span>

<span data-ttu-id="594b4-111">La clase de **\_ entrada MSMCAInfo** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="594b4-111">The **MSMCAInfo\_Entry** class has these types of members:</span></span>

-   [<span data-ttu-id="594b4-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="594b4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="594b4-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="594b4-113">Properties</span></span>

<span data-ttu-id="594b4-114">La clase de **\_ entrada MSMCAInfo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="594b4-114">The **MSMCAInfo\_Entry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="594b4-115">**Data**</span><span class="sxs-lookup"><span data-stu-id="594b4-115">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="594b4-116">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="594b4-116">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="594b4-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="594b4-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="594b4-118">Matriz de enteros que contiene un registro de errores de MCA completo según lo indicado por la capa de abstracción del sistema (SAL).</span><span class="sxs-lookup"><span data-stu-id="594b4-118">Integer array that contains a complete MCA error record as reported by the system abstraction layer (SAL).</span></span> <span data-ttu-id="594b4-119">SAL es código grabado en la ROM que el sistema operativo llama para realizar operaciones dependientes de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="594b4-119">The SAL is code burned into ROM that the operating system calls to perform platform-dependent operations.</span></span> <span data-ttu-id="594b4-120">Es similar al BIOS en una plataforma x86.</span><span class="sxs-lookup"><span data-stu-id="594b4-120">It is similar to the BIOS on an x86 platform.</span></span>

</dd> <dt>

<span data-ttu-id="594b4-121">**Duración**</span><span class="sxs-lookup"><span data-stu-id="594b4-121">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="594b4-122">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="594b4-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="594b4-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="594b4-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="594b4-124">Número de bytes en el registro de errores.</span><span class="sxs-lookup"><span data-stu-id="594b4-124">Number of bytes in the error record.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="594b4-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="594b4-125">Remarks</span></span>

<span data-ttu-id="594b4-126">La clase de **\_ entrada MSMCAInfo** se deriva de [**MSMCAInfo**](msmcainfo.md).</span><span class="sxs-lookup"><span data-stu-id="594b4-126">The **MSMCAInfo\_Entry** class is derived from [**MSMCAInfo**](msmcainfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="594b4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="594b4-127">Requirements</span></span>



| <span data-ttu-id="594b4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="594b4-128">Requirement</span></span> | <span data-ttu-id="594b4-129">Value</span><span class="sxs-lookup"><span data-stu-id="594b4-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="594b4-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="594b4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="594b4-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="594b4-131">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="594b4-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="594b4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="594b4-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="594b4-133">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="594b4-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="594b4-134">Namespace</span></span><br/>                | <span data-ttu-id="594b4-135">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="594b4-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="594b4-136">MOF</span><span class="sxs-lookup"><span data-stu-id="594b4-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="594b4-137"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="594b4-137"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="594b4-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="594b4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="594b4-139"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="594b4-139"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="594b4-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="594b4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="594b4-141">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="594b4-141">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="594b4-142">**MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="594b4-142">**MSMCAInfo**</span></span>](msmcainfo.md)
</dt> </dl>

 

 




