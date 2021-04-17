---
description: Contiene información que identifica el adaptador.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: D3DADAPTER_IDENTIFIER9 estructura (D3D9Types. h)
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
ms.openlocfilehash: 33aba75cafff5f9e69a74d5570f98455a9853289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717673"
---
# <a name="d3dadapter_identifier9-structure"></a><span data-ttu-id="35588-103">D3DADAPTER \_ estructura IDENTIFIER9</span><span class="sxs-lookup"><span data-stu-id="35588-103">D3DADAPTER\_IDENTIFIER9 structure</span></span>

<span data-ttu-id="35588-104">Contiene información que identifica el adaptador.</span><span class="sxs-lookup"><span data-stu-id="35588-104">Contains information identifying the adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="35588-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35588-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="35588-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="35588-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="35588-107">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="35588-107">**Driver**</span></span>
</dt> <dd>

<span data-ttu-id="35588-108">Tipo: **Char**</span><span class="sxs-lookup"><span data-stu-id="35588-108">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="35588-109">Se usa para la presentación al usuario.</span><span class="sxs-lookup"><span data-stu-id="35588-109">Used for presentation to the user.</span></span> <span data-ttu-id="35588-110">No debe usarse para identificar determinados controladores, ya que muchas cadenas diferentes podrían estar asociadas con el mismo dispositivo y controlador de distintos proveedores.</span><span class="sxs-lookup"><span data-stu-id="35588-110">This should not be used to identify particular drivers, because many different strings might be associated with the same device and driver from different vendors.</span></span>

</dd> <dt>

<span data-ttu-id="35588-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="35588-111">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="35588-112">Tipo: **Char**</span><span class="sxs-lookup"><span data-stu-id="35588-112">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="35588-113">Se usa para la presentación al usuario.</span><span class="sxs-lookup"><span data-stu-id="35588-113">Used for presentation to the user.</span></span>

</dd> <dt>

<span data-ttu-id="35588-114">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="35588-114">**DeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="35588-115">Tipo: **Char**</span><span class="sxs-lookup"><span data-stu-id="35588-115">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="35588-116">Nombre del dispositivo para GDI.</span><span class="sxs-lookup"><span data-stu-id="35588-116">Device name for GDI.</span></span>

</dd> <dt>

<span data-ttu-id="35588-117">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="35588-117">**DriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="35588-118">Tipo: **[ **\_ entero grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="35588-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="35588-119">Identifique la versión del controlador Direct3D.</span><span class="sxs-lookup"><span data-stu-id="35588-119">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="35588-120">Es válido realizar comparaciones menores que y mayores que en el valor entero con signo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="35588-120">It is legal to do less than and greater than comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="35588-121">Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos.</span><span class="sxs-lookup"><span data-stu-id="35588-121">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="35588-122">En su lugar, debe usar DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="35588-122">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="35588-123">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="35588-123">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="35588-124">**DriverVersionLowPart**</span><span class="sxs-lookup"><span data-stu-id="35588-124">**DriverVersionLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="35588-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35588-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="35588-126">Identifique la versión del controlador Direct3D.</span><span class="sxs-lookup"><span data-stu-id="35588-126">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="35588-127">Es legal realizar comparaciones de < y > en el valor entero con signo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="35588-127">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="35588-128">Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos.</span><span class="sxs-lookup"><span data-stu-id="35588-128">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="35588-129">En su lugar, debe usar DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="35588-129">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="35588-130">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="35588-130">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="35588-131">**DriverVersionHighPart**</span><span class="sxs-lookup"><span data-stu-id="35588-131">**DriverVersionHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="35588-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35588-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="35588-133">Identifique la versión del controlador Direct3D.</span><span class="sxs-lookup"><span data-stu-id="35588-133">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="35588-134">Es legal realizar comparaciones de < y > en el valor entero con signo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="35588-134">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="35588-135">Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos.</span><span class="sxs-lookup"><span data-stu-id="35588-135">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="35588-136">En su lugar, debe usar DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="35588-136">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="35588-137">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="35588-137">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="35588-138">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="35588-138">**VendorId**</span></span>
</dt> <dd>

<span data-ttu-id="35588-139">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35588-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="35588-140">Se puede usar para ayudar a identificar un conjunto de chips determinado.</span><span class="sxs-lookup"><span data-stu-id="35588-140">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="35588-141">Consulte este miembro para identificar al fabricante.</span><span class="sxs-lookup"><span data-stu-id="35588-141">Query this member to identify the manufacturer.</span></span> <span data-ttu-id="35588-142">El valor puede ser cero si se desconoce.</span><span class="sxs-lookup"><span data-stu-id="35588-142">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="35588-143">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="35588-143">**DeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="35588-144">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35588-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="35588-145">Se puede usar para ayudar a identificar un conjunto de chips determinado.</span><span class="sxs-lookup"><span data-stu-id="35588-145">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="35588-146">Consulte este miembro para identificar el tipo de conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="35588-146">Query this member to identify the type of chip set.</span></span> <span data-ttu-id="35588-147">El valor puede ser cero si se desconoce.</span><span class="sxs-lookup"><span data-stu-id="35588-147">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="35588-148">**SubSysId**</span><span class="sxs-lookup"><span data-stu-id="35588-148">**SubSysId**</span></span>
</dt> <dd>

<span data-ttu-id="35588-149">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35588-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="35588-150">Se puede usar para ayudar a identificar un conjunto de chips determinado.</span><span class="sxs-lookup"><span data-stu-id="35588-150">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="35588-151">Consulte este miembro para identificar el subsistema, normalmente el panel en cuestión.</span><span class="sxs-lookup"><span data-stu-id="35588-151">Query this member to identify the subsystem, typically the particular board.</span></span> <span data-ttu-id="35588-152">El valor puede ser cero si se desconoce.</span><span class="sxs-lookup"><span data-stu-id="35588-152">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="35588-153">**Revisión**</span><span class="sxs-lookup"><span data-stu-id="35588-153">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="35588-154">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35588-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="35588-155">Se puede usar para ayudar a identificar un conjunto de chips determinado.</span><span class="sxs-lookup"><span data-stu-id="35588-155">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="35588-156">Consulte este miembro para identificar el nivel de revisión del conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="35588-156">Query this member to identify the revision level of the chip set.</span></span> <span data-ttu-id="35588-157">El valor puede ser cero si se desconoce.</span><span class="sxs-lookup"><span data-stu-id="35588-157">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="35588-158">**DeviceIdentifier**</span><span class="sxs-lookup"><span data-stu-id="35588-158">**DeviceIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="35588-159">Tipo: **[ **GUID**](guid.md)**</span><span class="sxs-lookup"><span data-stu-id="35588-159">Type: **[**GUID**](guid.md)**</span></span>

</dd> <dd>

<span data-ttu-id="35588-160">Se puede consultar para comprobar los cambios en el controlador y en el conjunto de chips.</span><span class="sxs-lookup"><span data-stu-id="35588-160">Can be queried to check changes in the driver and chip set.</span></span> <span data-ttu-id="35588-161">Este GUID es un identificador único para el par de controladores y conjuntos de chips.</span><span class="sxs-lookup"><span data-stu-id="35588-161">This GUID is a unique identifier for the driver and chip set pair.</span></span> <span data-ttu-id="35588-162">Consulte este miembro para realizar el seguimiento de los cambios en el controlador y en el conjunto de chips con el fin de generar un nuevo perfil para el subsistema de gráficos.</span><span class="sxs-lookup"><span data-stu-id="35588-162">Query this member to track changes to the driver and chip set in order to generate a new profile for the graphics subsystem.</span></span> <span data-ttu-id="35588-163">DeviceIdentifier también se puede usar para identificar determinados controladores problemáticos.</span><span class="sxs-lookup"><span data-stu-id="35588-163">DeviceIdentifier can also be used to identify particular problematic drivers.</span></span>

</dd> <dt>

<span data-ttu-id="35588-164">**WHQLLevel**</span><span class="sxs-lookup"><span data-stu-id="35588-164">**WHQLLevel**</span></span>
</dt> <dd>

<span data-ttu-id="35588-165">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35588-165">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="35588-166">Se usa para determinar el nivel de validación de los laboratorios de calidad de hardware de Windows (WHQL) para este par de controlador y dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35588-166">Used to determine the Windows Hardware Quality Labs (WHQL) validation level for this driver and device pair.</span></span> <span data-ttu-id="35588-167">El valor DWORD es una estructura de fecha empaquetada que define la fecha de la versión de la prueba de WHQL más reciente pasada por el controlador.</span><span class="sxs-lookup"><span data-stu-id="35588-167">The DWORD is a packed date structure defining the date of the release of the most recent WHQL test passed by the driver.</span></span> <span data-ttu-id="35588-168">Es válido realizar operaciones de < y > en este valor.</span><span class="sxs-lookup"><span data-stu-id="35588-168">It is legal to perform < and > operations on this value.</span></span> <span data-ttu-id="35588-169">A continuación se muestra el formato de fecha.</span><span class="sxs-lookup"><span data-stu-id="35588-169">The following illustrates the date format.</span></span>



|       |                                               |
|-------|-----------------------------------------------|
| <span data-ttu-id="35588-170">Bits</span><span class="sxs-lookup"><span data-stu-id="35588-170">Bits</span></span>  |                                               |
| <span data-ttu-id="35588-171">31-16</span><span class="sxs-lookup"><span data-stu-id="35588-171">31-16</span></span> | <span data-ttu-id="35588-172">El año, un número decimal de 1999 en adelante.</span><span class="sxs-lookup"><span data-stu-id="35588-172">The year, a decimal number from 1999 upwards.</span></span> |
| <span data-ttu-id="35588-173">15-8</span><span class="sxs-lookup"><span data-stu-id="35588-173">15-8</span></span>  | <span data-ttu-id="35588-174">El mes, un número decimal comprendido entre 1 y 12.</span><span class="sxs-lookup"><span data-stu-id="35588-174">The month, a decimal number from 1 to 12.</span></span>     |
| <span data-ttu-id="35588-175">7-0</span><span class="sxs-lookup"><span data-stu-id="35588-175">7-0</span></span>   | <span data-ttu-id="35588-176">El día, un número decimal comprendido entre 1 y 31.</span><span class="sxs-lookup"><span data-stu-id="35588-176">The day, a decimal number from 1 to 31.</span></span>       |



 

<span data-ttu-id="35588-177">También se utilizan los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="35588-177">The following values are also used.</span></span>



|     |                                                       |
|-----|-------------------------------------------------------|
| <span data-ttu-id="35588-178">0</span><span class="sxs-lookup"><span data-stu-id="35588-178">0</span></span>   | <span data-ttu-id="35588-179">No certificado.</span><span class="sxs-lookup"><span data-stu-id="35588-179">Not certified.</span></span>                                        |
| <span data-ttu-id="35588-180">1</span><span class="sxs-lookup"><span data-stu-id="35588-180">1</span></span>   | <span data-ttu-id="35588-181">WHQL validado, pero no hay información de fecha disponible.</span><span class="sxs-lookup"><span data-stu-id="35588-181">WHQL validated, but no date information is available.</span></span> |



 

<span data-ttu-id="35588-182">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="35588-182">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

<span data-ttu-id="35588-183">Para Direct3D9Ex que se ejecuta en Windows Vista, Windows Server 2008, Windows 7 y Windows Server 2008 R2 (o más sistema operativo actual), [**IDirect3D9:: GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) devuelve 1 para el nivel de WHQL sin comprobar el estado del controlador.</span><span class="sxs-lookup"><span data-stu-id="35588-183">For Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) returns 1 for the WHQL level without checking the status of the driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35588-184">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35588-184">Remarks</span></span>

<span data-ttu-id="35588-185">En el siguiente ejemplo de pseudocódigo se muestra el formato de versión codificado en los miembros DriverVersion, DriverVersionLowPart y DriverVersionHighPart.</span><span class="sxs-lookup"><span data-stu-id="35588-185">The following pseudocode example illustrates the version format encoded in the DriverVersion, DriverVersionLowPart, and DriverVersionHighPart members.</span></span>


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



<span data-ttu-id="35588-186">Vea el SDK de la plataforma para obtener más información sobre la macro HIWORD, la macro LOWORD y la \_ estructura de enteros grandes.</span><span class="sxs-lookup"><span data-stu-id="35588-186">See the Platform SDK for more information about the HIWORD macro, the LOWORD macro, and the LARGE\_INTEGER structure.</span></span>

<span data-ttu-id="35588-187">MAX \_ Device \_ Identifier \_ String es una constante con la siguiente definición.</span><span class="sxs-lookup"><span data-stu-id="35588-187">MAX\_DEVICE\_IDENTIFIER\_STRING is a constant with the following definition.</span></span>


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



<span data-ttu-id="35588-188">Los miembros VendorId, DeviceId, SubSysId y revision se pueden usar conjuntamente para identificar determinados conjuntos de chips.</span><span class="sxs-lookup"><span data-stu-id="35588-188">The VendorId, DeviceId, SubSysId, and Revision members can be used in tandem to identify particular chip sets.</span></span> <span data-ttu-id="35588-189">Sin embargo, utilice estos miembros con precaución.</span><span class="sxs-lookup"><span data-stu-id="35588-189">However, use these members with caution.</span></span>

## <a name="requirements"></a><span data-ttu-id="35588-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35588-190">Requirements</span></span>



| <span data-ttu-id="35588-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="35588-191">Requirement</span></span> | <span data-ttu-id="35588-192">Value</span><span class="sxs-lookup"><span data-stu-id="35588-192">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35588-193">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35588-193">Header</span></span><br/> | <dl> <span data-ttu-id="35588-194"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="35588-194"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35588-195">Vea también</span><span class="sxs-lookup"><span data-stu-id="35588-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35588-196">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="35588-196">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
