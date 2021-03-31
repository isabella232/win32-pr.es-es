---
description: Representa las características de color de la Comisión Internacional de iluminación (CIE) de un monitor del equipo.
ms.assetid: 476aefae-11c0-46be-a2bb-83fbafd70421
title: Clase WmiMonitorColorCharacteristics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorColorCharacteristics
- WmiMonitorColorCharacteristics.Active
- WmiMonitorColorCharacteristics.Blue
- WmiMonitorColorCharacteristics.DefaultWhite
- WmiMonitorColorCharacteristics.Green
- WmiMonitorColorCharacteristics.InstanceName
- WmiMonitorColorCharacteristics.Red
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 9fbb7d56e56519576d257b077311a144e923d6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360900"
---
# <a name="wmimonitorcolorcharacteristics-class"></a><span data-ttu-id="b0aaa-103">Clase WmiMonitorColorCharacteristics</span><span class="sxs-lookup"><span data-stu-id="b0aaa-103">WmiMonitorColorCharacteristics class</span></span>

<span data-ttu-id="b0aaa-104">La clase **WmiMonitorColorCharacteristics** representa las características de color de la Comisión Internacional en iluminación (CIE) de un monitor del equipo.</span><span class="sxs-lookup"><span data-stu-id="b0aaa-104">The **WmiMonitorColorCharacteristics** class represents the International Commission on Illumination (CIE) color characteristics of a computer monitor.</span></span> <span data-ttu-id="b0aaa-105">Los datos corresponden a los datos del bloque de características del color de la estructura de vídeo electrónica estándar (VESA) de la asociación mejorada de la visualización de datos (E-EDID).</span><span class="sxs-lookup"><span data-stu-id="b0aaa-105">The data corresponds to data in the Color Characteristics block of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0aaa-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0aaa-106">Syntax</span></span>

``` syntax
class WmiMonitorColorCharacteristics : MSMonitorClass
{
  boolean  Active;
  XYZinCIE Blue;
  XYZinCIE DefaultWhite;
  XYZinCIE Green;
  string   InstanceName;
  XYZinCIE Red;
};
```

## <a name="members"></a><span data-ttu-id="b0aaa-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b0aaa-107">Members</span></span>

<span data-ttu-id="b0aaa-108">La clase **WmiMonitorColorCharacteristics** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b0aaa-108">The **WmiMonitorColorCharacteristics** class has these types of members:</span></span>

-   [<span data-ttu-id="b0aaa-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b0aaa-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0aaa-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b0aaa-110">Properties</span></span>

<span data-ttu-id="b0aaa-111">La clase **WmiMonitorColorCharacteristics** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b0aaa-111">The **WmiMonitorColorCharacteristics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0aaa-112">**Activo**</span><span class="sxs-lookup"><span data-stu-id="b0aaa-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0aaa-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b0aaa-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0aaa-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b0aaa-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0aaa-115">Indica el monitor activo.</span><span class="sxs-lookup"><span data-stu-id="b0aaa-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b0aaa-116">**Azul**</span><span class="sxs-lookup"><span data-stu-id="b0aaa-116">**Blue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0aaa-117">Tipo de datos: **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="b0aaa-117">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b0aaa-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b0aaa-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0aaa-119">Coordenadas CIE para Blue, representadas por una instancia de la clase [**XYZinCIE**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="b0aaa-119">CIE coordinates for blue, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b0aaa-120">**DefaultWhite**</span><span class="sxs-lookup"><span data-stu-id="b0aaa-120">**DefaultWhite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0aaa-121">Tipo de datos: **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="b0aaa-121">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b0aaa-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b0aaa-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0aaa-123">Coordenadas de CIE blancas predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="b0aaa-123">Default white CIE coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="b0aaa-124">**Verde**</span><span class="sxs-lookup"><span data-stu-id="b0aaa-124">**Green**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0aaa-125">Tipo de datos: **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="b0aaa-125">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b0aaa-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b0aaa-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0aaa-127">Coordenadas CIE para verde, representadas por una instancia de la clase [**XYZinCIE**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="b0aaa-127">CIE coordinates for green, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b0aaa-128">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="b0aaa-128">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0aaa-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b0aaa-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0aaa-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b0aaa-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0aaa-131">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="b0aaa-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b0aaa-132">Nombre de la instancia de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="b0aaa-132">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="b0aaa-133">**Rojo**</span><span class="sxs-lookup"><span data-stu-id="b0aaa-133">**Red**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0aaa-134">Tipo de datos: **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="b0aaa-134">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b0aaa-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b0aaa-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0aaa-136">Coordenadas CIE para rojo, representadas por una instancia de la clase [**XYZinCIE**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="b0aaa-136">CIE coordinates for red, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0aaa-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0aaa-137">Remarks</span></span>

<span data-ttu-id="b0aaa-138">Los valores de cromaticidad y de punto blanco se expresan como números fraccionarios con un formato de codificación.</span><span class="sxs-lookup"><span data-stu-id="b0aaa-138">The chromaticity and white point values are expressed as fractional numbers using an encoding format.</span></span> <span data-ttu-id="b0aaa-139">Este formato es preciso en la milésima ubicación, que tiene una longitud de 10 bits.</span><span class="sxs-lookup"><span data-stu-id="b0aaa-139">This format is accurate to the thousandth place, which is 10 bits in length.</span></span> <span data-ttu-id="b0aaa-140">El bit más significativo (MSB) representa 2 ^-1 y el bit menos significativo (LSB) representa los coeficientes de 2 ^-10, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b0aaa-140">The most significant bit (MSB) represents 2^-1 and the least significant bit (LSB) represents 2^-10 coefficients, respectively.</span></span> <span data-ttu-id="b0aaa-141">La precisión de los valores almacenados en la estructura E-EDID v1. x debe ser precisa de +/-0,005 del valor real.</span><span class="sxs-lookup"><span data-stu-id="b0aaa-141">Precision of the stored values in the E-EDID v1.x structure should be accurate to +/- 0.005 of the actual value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0aaa-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0aaa-142">Requirements</span></span>



| <span data-ttu-id="b0aaa-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0aaa-143">Requirement</span></span> | <span data-ttu-id="b0aaa-144">Value</span><span class="sxs-lookup"><span data-stu-id="b0aaa-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0aaa-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0aaa-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b0aaa-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0aaa-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b0aaa-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0aaa-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b0aaa-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0aaa-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b0aaa-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b0aaa-149">Namespace</span></span><br/>                | <span data-ttu-id="b0aaa-150">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="b0aaa-150">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="b0aaa-151">MOF</span><span class="sxs-lookup"><span data-stu-id="b0aaa-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0aaa-152"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0aaa-152"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0aaa-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0aaa-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0aaa-154"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0aaa-154"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0aaa-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0aaa-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0aaa-156">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="b0aaa-156">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




