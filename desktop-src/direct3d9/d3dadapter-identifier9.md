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
ms.openlocfilehash: 85401573956d29386b5ddabbd48711a7be140463
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129974"
---
# <a name="d3dadapter_identifier9-structure"></a><span data-ttu-id="f5c59-103">Estructura D3DADAPTER \_ IDENTIFIER9</span><span class="sxs-lookup"><span data-stu-id="f5c59-103">D3DADAPTER\_IDENTIFIER9 structure</span></span>

<span data-ttu-id="f5c59-104">Contiene información que identifica el adaptador.</span><span class="sxs-lookup"><span data-stu-id="f5c59-104">Contains information identifying the adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5c59-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5c59-105">Syntax</span></span>


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
#ifdef _WIN32
  LARGE_INTEGER DriverVersion;
#else
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
#endif
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a><span data-ttu-id="f5c59-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f5c59-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f5c59-107">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="f5c59-107">**Driver**</span></span>
</dt> <dd>

<span data-ttu-id="f5c59-108">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="f5c59-108">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="f5c59-109">Se usa para la presentación al usuario.</span><span class="sxs-lookup"><span data-stu-id="f5c59-109">Used for presentation to the user.</span></span> <span data-ttu-id="f5c59-110">Esto no debe usarse para identificar controladores concretos, ya que muchas cadenas diferentes podrían estar asociadas al mismo dispositivo y controlador de proveedores diferentes.</span><span class="sxs-lookup"><span data-stu-id="f5c59-110">This should not be used to identify particular drivers, because many different strings might be associated with the same device and driver from different vendors.</span></span>

</dd> <dt>

<span data-ttu-id="f5c59-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f5c59-111">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f5c59-112">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="f5c59-112">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="f5c59-113">Se usa para la presentación al usuario.</span><span class="sxs-lookup"><span data-stu-id="f5c59-113">Used for presentation to the user.</span></span>

</dd> <dt>

<span data-ttu-id="f5c59-114">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="f5c59-114">**DeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="f5c59-115">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="f5c59-115">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="f5c59-116">Nombre del dispositivo para GDI.</span><span class="sxs-lookup"><span data-stu-id="f5c59-116">Device name for GDI.</span></span>

</dd> <dt>

<span data-ttu-id="f5c59-117">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="f5c59-117">**DriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="f5c59-118">Tipo: **[ **ENTERO \_ GRANDE**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="f5c59-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="f5c59-119">Identifique la versión del controlador Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f5c59-119">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="f5c59-120">Es legal realizar comparaciones menores y mayores que en el valor entero de 64 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="f5c59-120">It is legal to do less than and greater than comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="f5c59-121">Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos.</span><span class="sxs-lookup"><span data-stu-id="f5c59-121">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="f5c59-122">En su lugar, debe usar DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="f5c59-122">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="f5c59-123">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f5c59-123">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f5c59-124">**DriverVersionLowPart**</span><span class="sxs-lookup"><span data-stu-id="f5c59-124">**DriverVersionLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="f5c59-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5c59-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5c59-126">Identifique la versión del controlador Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f5c59-126">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="f5c59-127">Es válido realizar comparaciones < y > en el valor entero de 64 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="f5c59-127">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="f5c59-128">Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos.</span><span class="sxs-lookup"><span data-stu-id="f5c59-128">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="f5c59-129">En su lugar, debe usar DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="f5c59-129">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="f5c59-130">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f5c59-130">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f5c59-131">**DriverVersionHighPart**</span><span class="sxs-lookup"><span data-stu-id="f5c59-131">**DriverVersionHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="f5c59-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5c59-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5c59-133">Identifique la versión del controlador Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f5c59-133">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="f5c59-134">Es válido realizar comparaciones < y > en el valor entero de 64 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="f5c59-134">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="f5c59-135">Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos.</span><span class="sxs-lookup"><span data-stu-id="f5c59-135">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="f5c59-136">En su lugar, debe usar DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="f5c59-136">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="f5c59-137">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f5c59-137">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f5c59-138">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="f5c59-138">**VendorId**</span></span>
</dt> <dd>

<span data-ttu-id="f5c59-139">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5c59-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5c59-140">Se puede usar para ayudar a identificar un conjunto de chips determinado.</span><span class="sxs-lookup"><span data-stu-id="f5c59-140">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="f5c59-141">Consulte este miembro para identificar al fabricante.</span><span class="sxs-lookup"><span data-stu-id="f5c59-141">Query this member to identify the manufacturer.</span></span> <span data-ttu-id="f5c59-142">El valor puede ser cero si es desconocido.</span><span class="sxs-lookup"><span data-stu-id="f5c59-142">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="f5c59-143">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="f5c59-143">**DeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="f5c59-144">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5c59-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5c59-145">Se puede usar para ayudar a identificar un conjunto de chips determinado.</span><span class="sxs-lookup"><span data-stu-id="f5c59-145">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="f5c59-146">Consulte este miembro para identificar el tipo de conjunto de chip.</span><span class="sxs-lookup"><span data-stu-id="f5c59-146">Query this member to identify the type of chip set.</span></span> <span data-ttu-id="f5c59-147">El valor puede ser cero si es desconocido.</span><span class="sxs-lookup"><span data-stu-id="f5c59-147">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="f5c59-148">**SubSysId**</span><span class="sxs-lookup"><span data-stu-id="f5c59-148">**SubSysId**</span></span>
</dt> <dd>

<span data-ttu-id="f5c59-149">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5c59-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5c59-150">Se puede usar para ayudar a identificar un conjunto de chips determinado.</span><span class="sxs-lookup"><span data-stu-id="f5c59-150">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="f5c59-151">Consulte este miembro para identificar el subsistema, normalmente la placa determinada.</span><span class="sxs-lookup"><span data-stu-id="f5c59-151">Query this member to identify the subsystem, typically the particular board.</span></span> <span data-ttu-id="f5c59-152">El valor puede ser cero si es desconocido.</span><span class="sxs-lookup"><span data-stu-id="f5c59-152">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="f5c59-153">**Revisión**</span><span class="sxs-lookup"><span data-stu-id="f5c59-153">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="f5c59-154">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5c59-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5c59-155">Se puede usar para ayudar a identificar un conjunto de chips determinado.</span><span class="sxs-lookup"><span data-stu-id="f5c59-155">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="f5c59-156">Consulte este miembro para identificar el nivel de revisión del conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="f5c59-156">Query this member to identify the revision level of the chip set.</span></span> <span data-ttu-id="f5c59-157">El valor puede ser cero si es desconocido.</span><span class="sxs-lookup"><span data-stu-id="f5c59-157">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="f5c59-158">**DeviceIdentifier**</span><span class="sxs-lookup"><span data-stu-id="f5c59-158">**DeviceIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="f5c59-159">Tipo: **[ **GUID**](guid.md)**</span><span class="sxs-lookup"><span data-stu-id="f5c59-159">Type: **[**GUID**](guid.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5c59-160">Se puede consultar para comprobar los cambios en el controlador y el conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="f5c59-160">Can be queried to check changes in the driver and chip set.</span></span> <span data-ttu-id="f5c59-161">Este GUID es un identificador único para el par de controladores y conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="f5c59-161">This GUID is a unique identifier for the driver and chip set pair.</span></span> <span data-ttu-id="f5c59-162">Consulte este miembro para realizar un seguimiento de los cambios en el controlador y el conjunto de chips con el fin de generar un nuevo perfil para el subsistema de gráficos.</span><span class="sxs-lookup"><span data-stu-id="f5c59-162">Query this member to track changes to the driver and chip set in order to generate a new profile for the graphics subsystem.</span></span> <span data-ttu-id="f5c59-163">DeviceIdentifier también se puede usar para identificar controladores problemáticos concretos.</span><span class="sxs-lookup"><span data-stu-id="f5c59-163">DeviceIdentifier can also be used to identify particular problematic drivers.</span></span>

</dd> <dt>

<span data-ttu-id="f5c59-164">**WHQLLevel**</span><span class="sxs-lookup"><span data-stu-id="f5c59-164">**WHQLLevel**</span></span>
</dt> <dd>

<span data-ttu-id="f5c59-165">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5c59-165">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5c59-166">Se usa para determinar el Laboratorios de calidad de hardware de Windows (WHQL) de validación de controladores (WHQL) para este par de controladores y dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f5c59-166">Used to determine the Windows Hardware Quality Labs (WHQL) validation level for this driver and device pair.</span></span> <span data-ttu-id="f5c59-167">DWORD es una estructura de fecha empaquetada que define la fecha de lanzamiento de la prueba WHQL más reciente superada por el controlador.</span><span class="sxs-lookup"><span data-stu-id="f5c59-167">The DWORD is a packed date structure defining the date of the release of the most recent WHQL test passed by the driver.</span></span> <span data-ttu-id="f5c59-168">Es válido realizar operaciones < y > en este valor.</span><span class="sxs-lookup"><span data-stu-id="f5c59-168">It is legal to perform < and > operations on this value.</span></span> <span data-ttu-id="f5c59-169">A continuación se muestra el formato de fecha.</span><span class="sxs-lookup"><span data-stu-id="f5c59-169">The following illustrates the date format.</span></span>



| <span data-ttu-id="f5c59-170">Bits</span><span class="sxs-lookup"><span data-stu-id="f5c59-170">Bits</span></span>  |  <span data-ttu-id="f5c59-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c59-171">Description</span></span>                                             |
|-------|-----------------------------------------------|
| <span data-ttu-id="f5c59-172">31-16</span><span class="sxs-lookup"><span data-stu-id="f5c59-172">31-16</span></span> | <span data-ttu-id="f5c59-173">El año, un número decimal de 1999 hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="f5c59-173">The year, a decimal number from 1999 upwards.</span></span> |
| <span data-ttu-id="f5c59-174">15-8</span><span class="sxs-lookup"><span data-stu-id="f5c59-174">15-8</span></span>  | <span data-ttu-id="f5c59-175">El mes, un número decimal de 1 a 12.</span><span class="sxs-lookup"><span data-stu-id="f5c59-175">The month, a decimal number from 1 to 12.</span></span>     |
| <span data-ttu-id="f5c59-176">7-0</span><span class="sxs-lookup"><span data-stu-id="f5c59-176">7-0</span></span>   | <span data-ttu-id="f5c59-177">El día, un número decimal de 1 a 31.</span><span class="sxs-lookup"><span data-stu-id="f5c59-177">The day, a decimal number from 1 to 31.</span></span>       |



 

<span data-ttu-id="f5c59-178">También se usan los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="f5c59-178">The following values are also used.</span></span>



| <span data-ttu-id="f5c59-179">Valor</span><span class="sxs-lookup"><span data-stu-id="f5c59-179">Value</span></span>    |  <span data-ttu-id="f5c59-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5c59-180">Description</span></span>                                                     |
|-----|-------------------------------------------------------|
| <span data-ttu-id="f5c59-181">0</span><span class="sxs-lookup"><span data-stu-id="f5c59-181">0</span></span>   | <span data-ttu-id="f5c59-182">No certificado.</span><span class="sxs-lookup"><span data-stu-id="f5c59-182">Not certified.</span></span>                                        |
| <span data-ttu-id="f5c59-183">1</span><span class="sxs-lookup"><span data-stu-id="f5c59-183">1</span></span>   | <span data-ttu-id="f5c59-184">WHQL validado, pero no hay información de fecha disponible.</span><span class="sxs-lookup"><span data-stu-id="f5c59-184">WHQL validated, but no date information is available.</span></span> |



 

<span data-ttu-id="f5c59-185">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="f5c59-185">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

<span data-ttu-id="f5c59-186">Para Direct3D9Ex que se ejecuta en Windows Vista, Windows Server 2008, Windows 7 y Windows Server 2008 R2 (o más sistema operativo actual), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) devuelve 1 para el nivel WHQL sin comprobar el estado del controlador.</span><span class="sxs-lookup"><span data-stu-id="f5c59-186">For Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) returns 1 for the WHQL level without checking the status of the driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5c59-187">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5c59-187">Remarks</span></span>

<span data-ttu-id="f5c59-188">En el ejemplo de pseudocódigo siguiente se muestra el formato de versión codificado en los miembros DriverVersion, DriverVersionLowPart y DriverVersionHighPart.</span><span class="sxs-lookup"><span data-stu-id="f5c59-188">The following pseudocode example illustrates the version format encoded in the DriverVersion, DriverVersionLowPart, and DriverVersionHighPart members.</span></span>


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



<span data-ttu-id="f5c59-189">Consulte Platform SDK para obtener más información sobre la macro HIWORD, la macro LOWORD y la estructura LARGE \_ INTEGER.</span><span class="sxs-lookup"><span data-stu-id="f5c59-189">See the Platform SDK for more information about the HIWORD macro, the LOWORD macro, and the LARGE\_INTEGER structure.</span></span>

<span data-ttu-id="f5c59-190">MAX \_ DEVICE IDENTIFIER STRING es una constante con la siguiente \_ \_ definición.</span><span class="sxs-lookup"><span data-stu-id="f5c59-190">MAX\_DEVICE\_IDENTIFIER\_STRING is a constant with the following definition.</span></span>


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



<span data-ttu-id="f5c59-191">Los miembros VendorId, DeviceId, SubSysId y Revision se pueden usar conjuntamente para identificar conjuntos de chips concretos.</span><span class="sxs-lookup"><span data-stu-id="f5c59-191">The VendorId, DeviceId, SubSysId, and Revision members can be used in tandem to identify particular chip sets.</span></span> <span data-ttu-id="f5c59-192">Sin embargo, use estos miembros con precaución.</span><span class="sxs-lookup"><span data-stu-id="f5c59-192">However, use these members with caution.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c59-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5c59-193">Requirements</span></span>



| <span data-ttu-id="f5c59-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5c59-194">Requirement</span></span> | <span data-ttu-id="f5c59-195">Value</span><span class="sxs-lookup"><span data-stu-id="f5c59-195">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c59-196">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5c59-196">Header</span></span><br/> | <dl> <span data-ttu-id="f5c59-197"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="f5c59-197"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5c59-198">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f5c59-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c59-199">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="f5c59-199">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
