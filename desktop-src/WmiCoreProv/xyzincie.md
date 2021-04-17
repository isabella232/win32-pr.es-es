---
description: Contiene las coordenadas de la presentación en el espacio de color de la Comisión Internacional de iluminación (CIE) XYZ.
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: Clase XYZinCIE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XYZinCIE
- XYZinCIE.X
- XYZinCIE.Y
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ba7f781a83f3e6ba5aa4683003386a0478d65088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716770"
---
# <a name="xyzincie-class"></a><span data-ttu-id="71628-103">Clase XYZinCIE</span><span class="sxs-lookup"><span data-stu-id="71628-103">XYZinCIE class</span></span>

<span data-ttu-id="71628-104">La clase WMI **XYZinCIE** contiene las coordenadas de la presentación en el espacio de color de la Comisión Internacional en la iluminación (CIE) XYZ.</span><span class="sxs-lookup"><span data-stu-id="71628-104">The **XYZinCIE** WMI class contains the coordinates of the display in the International Commission on Illumination (CIE) XYZ color space.</span></span>

## <a name="syntax"></a><span data-ttu-id="71628-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71628-105">Syntax</span></span>

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a><span data-ttu-id="71628-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="71628-106">Members</span></span>

<span data-ttu-id="71628-107">La clase **XYZinCIE** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="71628-107">The **XYZinCIE** class has these types of members:</span></span>

-   [<span data-ttu-id="71628-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71628-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71628-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71628-109">Properties</span></span>

<span data-ttu-id="71628-110">La clase **XYZinCIE** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="71628-110">The **XYZinCIE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71628-111">**X**</span><span class="sxs-lookup"><span data-stu-id="71628-111">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71628-112">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71628-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71628-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71628-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71628-114">Coordenada X.</span><span class="sxs-lookup"><span data-stu-id="71628-114">X-coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="71628-115">**S**</span><span class="sxs-lookup"><span data-stu-id="71628-115">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71628-116">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71628-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71628-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71628-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71628-118">Coordenada Y.</span><span class="sxs-lookup"><span data-stu-id="71628-118">Y-coordinate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71628-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71628-119">Remarks</span></span>

<span data-ttu-id="71628-120">La clase [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) contiene las instancias incrustadas de la clase **XYZinCIE** para describir las características de color de un monitor.</span><span class="sxs-lookup"><span data-stu-id="71628-120">The [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) class contains embedded instances of the **XYZinCIE** class to describe the color characteristics of a monitor.</span></span>

<span data-ttu-id="71628-121">Para calcular la coordenada z, en función de los valores x e y, use la relación \| \| (x, y, z) \| \| = 1.</span><span class="sxs-lookup"><span data-stu-id="71628-121">To calculate the z-coordinate, based on the x and y values, use the relation \|\|(x,y,z)\|\| = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="71628-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71628-122">Requirements</span></span>



| <span data-ttu-id="71628-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="71628-123">Requirement</span></span> | <span data-ttu-id="71628-124">Value</span><span class="sxs-lookup"><span data-stu-id="71628-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71628-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71628-125">Minimum supported client</span></span><br/> | <span data-ttu-id="71628-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71628-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="71628-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71628-127">Minimum supported server</span></span><br/> | <span data-ttu-id="71628-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71628-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="71628-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="71628-129">Namespace</span></span><br/>                | <span data-ttu-id="71628-130">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="71628-130">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="71628-131">MOF</span><span class="sxs-lookup"><span data-stu-id="71628-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71628-132"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71628-132"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="71628-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="71628-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71628-134"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71628-134"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71628-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="71628-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71628-136">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="71628-136">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




