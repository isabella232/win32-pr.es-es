---
description: Contiene información que identifica el adaptador.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: D3DADAPTER_IDENTIFIER9 estructura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DADAPTER_IDENTIFIER9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: db4b25cb44b3b43b3b9754f241e2c505bdfedbc7
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343400"
---
# <a name="d3dadapter_identifier9-structure"></a><span data-ttu-id="60886-103">Estructura D3DADAPTER \_ IDENTIFIER9</span><span class="sxs-lookup"><span data-stu-id="60886-103">D3DADAPTER\_IDENTIFIER9 structure</span></span>

<span data-ttu-id="60886-104">Contiene información que identifica el adaptador.</span><span class="sxs-lookup"><span data-stu-id="60886-104">Contains information identifying the adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="60886-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60886-105">Syntax</span></span>


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
  LARGE_INTEGER DriverVersion;
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a><span data-ttu-id="60886-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="60886-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="60886-107">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="60886-107">**Driver**</span></span>
</dt> <dd>

<span data-ttu-id="60886-108">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="60886-108">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="60886-109">Se usa para la presentación al usuario.</span><span class="sxs-lookup"><span data-stu-id="60886-109">Used for presentation to the user.</span></span> <span data-ttu-id="60886-110">Esto no debe usarse para identificar controladores concretos, ya que muchas cadenas diferentes podrían estar asociadas al mismo dispositivo y controlador de proveedores diferentes.</span><span class="sxs-lookup"><span data-stu-id="60886-110">This should not be used to identify particular drivers, because many different strings might be associated with the same device and driver from different vendors.</span></span>

</dd> <dt>

<span data-ttu-id="60886-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60886-111">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="60886-112">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="60886-112">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="60886-113">Se usa para la presentación al usuario.</span><span class="sxs-lookup"><span data-stu-id="60886-113">Used for presentation to the user.</span></span>

</dd> <dt>

<span data-ttu-id="60886-114">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="60886-114">**DeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="60886-115">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="60886-115">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="60886-116">Nombre del dispositivo para GDI.</span><span class="sxs-lookup"><span data-stu-id="60886-116">Device name for GDI.</span></span>

</dd> <dt>

<span data-ttu-id="60886-117">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="60886-117">**DriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="60886-118">Tipo: **[ **ENTERO \_ GRANDE**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="60886-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="60886-119">Identifique la versión del controlador Direct3D.</span><span class="sxs-lookup"><span data-stu-id="60886-119">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="60886-120">Es legal realizar comparaciones menores y mayores que en el valor entero de 64 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="60886-120">It is legal to do less than and greater than comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="60886-121">Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos.</span><span class="sxs-lookup"><span data-stu-id="60886-121">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="60886-122">En su lugar, debe usar DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="60886-122">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="60886-123">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="60886-123">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="60886-124">**DriverVersionLowPart**</span><span class="sxs-lookup"><span data-stu-id="60886-124">**DriverVersionLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="60886-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60886-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60886-126">Identifique la versión del controlador de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="60886-126">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="60886-127">Es válido realizar comparaciones < y > en el valor entero de 64 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="60886-127">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="60886-128">Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos.</span><span class="sxs-lookup"><span data-stu-id="60886-128">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="60886-129">En su lugar, debe usar DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="60886-129">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="60886-130">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="60886-130">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="60886-131">**DriverVersionHighPart**</span><span class="sxs-lookup"><span data-stu-id="60886-131">**DriverVersionHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="60886-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60886-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60886-133">Identifique la versión del controlador de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="60886-133">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="60886-134">Es válido realizar comparaciones < y > en el valor entero de 64 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="60886-134">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="60886-135">Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos.</span><span class="sxs-lookup"><span data-stu-id="60886-135">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="60886-136">En su lugar, debe usar DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="60886-136">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="60886-137">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="60886-137">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="60886-138">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="60886-138">**VendorId**</span></span>
</dt> <dd>

<span data-ttu-id="60886-139">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60886-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60886-140">Se puede usar para ayudar a identificar un conjunto de chip determinado.</span><span class="sxs-lookup"><span data-stu-id="60886-140">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="60886-141">Consulte este miembro para identificar al fabricante.</span><span class="sxs-lookup"><span data-stu-id="60886-141">Query this member to identify the manufacturer.</span></span> <span data-ttu-id="60886-142">El valor puede ser cero si se desconoce.</span><span class="sxs-lookup"><span data-stu-id="60886-142">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="60886-143">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="60886-143">**DeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="60886-144">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60886-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60886-145">Se puede usar para ayudar a identificar un conjunto de chip determinado.</span><span class="sxs-lookup"><span data-stu-id="60886-145">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="60886-146">Consulte este miembro para identificar el tipo de conjunto de chip.</span><span class="sxs-lookup"><span data-stu-id="60886-146">Query this member to identify the type of chip set.</span></span> <span data-ttu-id="60886-147">El valor puede ser cero si se desconoce.</span><span class="sxs-lookup"><span data-stu-id="60886-147">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="60886-148">**SubSysId**</span><span class="sxs-lookup"><span data-stu-id="60886-148">**SubSysId**</span></span>
</dt> <dd>

<span data-ttu-id="60886-149">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60886-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60886-150">Se puede usar para ayudar a identificar un conjunto de chips determinado.</span><span class="sxs-lookup"><span data-stu-id="60886-150">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="60886-151">Consulte este miembro para identificar el subsistema, normalmente la placa determinada.</span><span class="sxs-lookup"><span data-stu-id="60886-151">Query this member to identify the subsystem, typically the particular board.</span></span> <span data-ttu-id="60886-152">El valor puede ser cero si es desconocido.</span><span class="sxs-lookup"><span data-stu-id="60886-152">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="60886-153">**Revisión**</span><span class="sxs-lookup"><span data-stu-id="60886-153">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="60886-154">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60886-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60886-155">Se puede usar para ayudar a identificar un conjunto de chips determinado.</span><span class="sxs-lookup"><span data-stu-id="60886-155">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="60886-156">Consulte este miembro para identificar el nivel de revisión del conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="60886-156">Query this member to identify the revision level of the chip set.</span></span> <span data-ttu-id="60886-157">El valor puede ser cero si es desconocido.</span><span class="sxs-lookup"><span data-stu-id="60886-157">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="60886-158">**DeviceIdentifier**</span><span class="sxs-lookup"><span data-stu-id="60886-158">**DeviceIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="60886-159">Tipo: **[ **GUID**](guid.md)**</span><span class="sxs-lookup"><span data-stu-id="60886-159">Type: **[**GUID**](guid.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60886-160">Se puede consultar para comprobar los cambios en el controlador y el conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="60886-160">Can be queried to check changes in the driver and chip set.</span></span> <span data-ttu-id="60886-161">Este GUID es un identificador único para el par de controladores y conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="60886-161">This GUID is a unique identifier for the driver and chip set pair.</span></span> <span data-ttu-id="60886-162">Consulte este miembro para realizar un seguimiento de los cambios en el controlador y el conjunto de chips con el fin de generar un nuevo perfil para el subsistema de gráficos.</span><span class="sxs-lookup"><span data-stu-id="60886-162">Query this member to track changes to the driver and chip set in order to generate a new profile for the graphics subsystem.</span></span> <span data-ttu-id="60886-163">DeviceIdentifier también se puede usar para identificar controladores problemáticos concretos.</span><span class="sxs-lookup"><span data-stu-id="60886-163">DeviceIdentifier can also be used to identify particular problematic drivers.</span></span>

</dd> <dt>

<span data-ttu-id="60886-164">**WHQLLevel**</span><span class="sxs-lookup"><span data-stu-id="60886-164">**WHQLLevel**</span></span>
</dt> <dd>

<span data-ttu-id="60886-165">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60886-165">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60886-166">Se usa para determinar el Laboratorios de calidad de hardware de Windows (WHQL) de validación de controladores (WHQL) para este par de controladores y dispositivos.</span><span class="sxs-lookup"><span data-stu-id="60886-166">Used to determine the Windows Hardware Quality Labs (WHQL) validation level for this driver and device pair.</span></span> <span data-ttu-id="60886-167">DWORD es una estructura de fechas empaquetada que define la fecha de lanzamiento de la prueba WHQL más reciente superada por el controlador.</span><span class="sxs-lookup"><span data-stu-id="60886-167">The DWORD is a packed date structure defining the date of the release of the most recent WHQL test passed by the driver.</span></span> <span data-ttu-id="60886-168">Es legal realizar operaciones < y > en este valor.</span><span class="sxs-lookup"><span data-stu-id="60886-168">It is legal to perform < and > operations on this value.</span></span> <span data-ttu-id="60886-169">A continuación se muestra el formato de fecha.</span><span class="sxs-lookup"><span data-stu-id="60886-169">The following illustrates the date format.</span></span>



| <span data-ttu-id="60886-170">Bits</span><span class="sxs-lookup"><span data-stu-id="60886-170">Bits</span></span>  |  <span data-ttu-id="60886-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="60886-171">Description</span></span>                                             |
|-------|-----------------------------------------------|
| <span data-ttu-id="60886-172">31-16</span><span class="sxs-lookup"><span data-stu-id="60886-172">31-16</span></span> | <span data-ttu-id="60886-173">Año, un número decimal de 1999 hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="60886-173">The year, a decimal number from 1999 upwards.</span></span> |
| <span data-ttu-id="60886-174">15-8</span><span class="sxs-lookup"><span data-stu-id="60886-174">15-8</span></span>  | <span data-ttu-id="60886-175">El mes, un número decimal de 1 a 12.</span><span class="sxs-lookup"><span data-stu-id="60886-175">The month, a decimal number from 1 to 12.</span></span>     |
| <span data-ttu-id="60886-176">7-0</span><span class="sxs-lookup"><span data-stu-id="60886-176">7-0</span></span>   | <span data-ttu-id="60886-177">El día, un número decimal de 1 a 31.</span><span class="sxs-lookup"><span data-stu-id="60886-177">The day, a decimal number from 1 to 31.</span></span>       |



 

<span data-ttu-id="60886-178">También se usan los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="60886-178">The following values are also used.</span></span>



| <span data-ttu-id="60886-179">Valor</span><span class="sxs-lookup"><span data-stu-id="60886-179">Value</span></span>    |  <span data-ttu-id="60886-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="60886-180">Description</span></span>                                                     |
|-----|-------------------------------------------------------|
| <span data-ttu-id="60886-181">0</span><span class="sxs-lookup"><span data-stu-id="60886-181">0</span></span>   | <span data-ttu-id="60886-182">No certificado.</span><span class="sxs-lookup"><span data-stu-id="60886-182">Not certified.</span></span>                                        |
| <span data-ttu-id="60886-183">1</span><span class="sxs-lookup"><span data-stu-id="60886-183">1</span></span>   | <span data-ttu-id="60886-184">WHQL validado, pero no hay información de fecha disponible.</span><span class="sxs-lookup"><span data-stu-id="60886-184">WHQL validated, but no date information is available.</span></span> |



 

<span data-ttu-id="60886-185">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="60886-185">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

<span data-ttu-id="60886-186">Para Direct3D9Ex que se ejecuta en Windows Vista, Windows Server 2008, Windows 7 y Windows Server 2008 R2 (o más sistema operativo actual), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) devuelve 1 para el nivel WHQL sin comprobar el estado del controlador.</span><span class="sxs-lookup"><span data-stu-id="60886-186">For Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) returns 1 for the WHQL level without checking the status of the driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60886-187">Comentarios</span><span class="sxs-lookup"><span data-stu-id="60886-187">Remarks</span></span>

<span data-ttu-id="60886-188">En el ejemplo de pseudocódigo siguiente se muestra el formato de versión codificado en los miembros DriverVersion, DriverVersionLowPart y DriverVersionHighPart.</span><span class="sxs-lookup"><span data-stu-id="60886-188">The following pseudocode example illustrates the version format encoded in the DriverVersion, DriverVersionLowPart, and DriverVersionHighPart members.</span></span>


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



<span data-ttu-id="60886-189">Consulte Platform SDK para obtener más información sobre la macro HIWORD, la macro LOWORD y la estructura \_ LARGE INTEGER.</span><span class="sxs-lookup"><span data-stu-id="60886-189">See the Platform SDK for more information about the HIWORD macro, the LOWORD macro, and the LARGE\_INTEGER structure.</span></span>

<span data-ttu-id="60886-190">MAX \_ DEVICE IDENTIFIER STRING es una constante con la siguiente \_ \_ definición.</span><span class="sxs-lookup"><span data-stu-id="60886-190">MAX\_DEVICE\_IDENTIFIER\_STRING is a constant with the following definition.</span></span>


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



<span data-ttu-id="60886-191">Los miembros VendorId, DeviceId, SubSysId y Revision se pueden usar conjuntamente para identificar conjuntos de chip determinados.</span><span class="sxs-lookup"><span data-stu-id="60886-191">The VendorId, DeviceId, SubSysId, and Revision members can be used in tandem to identify particular chip sets.</span></span> <span data-ttu-id="60886-192">Sin embargo, use estos miembros con precaución.</span><span class="sxs-lookup"><span data-stu-id="60886-192">However, use these members with caution.</span></span>

## <a name="requirements"></a><span data-ttu-id="60886-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60886-193">Requirements</span></span>



| <span data-ttu-id="60886-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="60886-194">Requirement</span></span> | <span data-ttu-id="60886-195">Value</span><span class="sxs-lookup"><span data-stu-id="60886-195">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60886-196">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60886-196">Header</span></span><br/> | <dl> <span data-ttu-id="60886-197"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="60886-197"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60886-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="60886-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60886-199">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="60886-199">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
