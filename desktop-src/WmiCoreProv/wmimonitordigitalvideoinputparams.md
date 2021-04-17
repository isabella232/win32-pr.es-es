---
description: Representa los parámetros de entrada para el vídeo digital.
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: Clase WmiMonitorDigitalVideoInputParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDigitalVideoInputParams
- WmiMonitorDigitalVideoInputParams.Active
- WmiMonitorDigitalVideoInputParams.InstanceName
- WmiMonitorDigitalVideoInputParams.IsDFP1xCompatible
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: a08e38a38bb5f5e8d539fabdf69c429c42f4b1f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716624"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a><span data-ttu-id="eb67f-103">Clase WmiMonitorDigitalVideoInputParams</span><span class="sxs-lookup"><span data-stu-id="eb67f-103">WmiMonitorDigitalVideoInputParams class</span></span>

<span data-ttu-id="eb67f-104">**WmiMonitorDigitalVideoInputParams** representa los parámetros de entrada de vídeo digital.</span><span class="sxs-lookup"><span data-stu-id="eb67f-104">The **WmiMonitorDigitalVideoInputParams** represents input parameters for digital video.</span></span> <span data-ttu-id="eb67f-105">Los datos de esta clase se corresponden con los datos de la definición de entrada de vídeo de vídeo electrónica estándar (VESA) estándar de identificación de la visualización extendida mejorada (E-EDID).</span><span class="sxs-lookup"><span data-stu-id="eb67f-105">The data in this class corresponds to data in the Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span> <span data-ttu-id="eb67f-106">Una instancia de esta clase solo está disponible cuando el valor de la propiedad **VideoInputType** de la clase [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) es "digital".</span><span class="sxs-lookup"><span data-stu-id="eb67f-106">An instance of this class is available only when the value of the **VideoInputType** property of the [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) class is "Digital".</span></span>

## <a name="syntax"></a><span data-ttu-id="eb67f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb67f-107">Syntax</span></span>

``` syntax
class WmiMonitorDigitalVideoInputParams : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  boolean IsDFP1xCompatible;
};
```

## <a name="members"></a><span data-ttu-id="eb67f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="eb67f-108">Members</span></span>

<span data-ttu-id="eb67f-109">La clase **WmiMonitorDigitalVideoInputParams** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eb67f-109">The **WmiMonitorDigitalVideoInputParams** class has these types of members:</span></span>

-   [<span data-ttu-id="eb67f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb67f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb67f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb67f-111">Properties</span></span>

<span data-ttu-id="eb67f-112">La clase **WmiMonitorDigitalVideoInputParams** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="eb67f-112">The **WmiMonitorDigitalVideoInputParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb67f-113">**Activo**</span><span class="sxs-lookup"><span data-stu-id="eb67f-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb67f-114">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="eb67f-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb67f-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb67f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb67f-116">Indica el monitor activo.</span><span class="sxs-lookup"><span data-stu-id="eb67f-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="eb67f-117">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="eb67f-117">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb67f-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb67f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb67f-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb67f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb67f-120">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="eb67f-120">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="eb67f-121">Nombre de la instancia de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="eb67f-121">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="eb67f-122">**IsDFP1xCompatible**</span><span class="sxs-lookup"><span data-stu-id="eb67f-122">**IsDFP1xCompatible**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb67f-123">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="eb67f-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb67f-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb67f-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb67f-125">VESA DFP 1. x o compatible.</span><span class="sxs-lookup"><span data-stu-id="eb67f-125">VESA DFP 1.x or compatible.</span></span> <span data-ttu-id="eb67f-126">Si se establece, la interfaz es compatible con el panel plano digital VESA (DFP) 1. x transición minimizada de señalización diferencial (TMDS) CRGB, 1 píxel/reloj, hasta 8 bits/color más significativo (MSB) alineado, DE activo alto.</span><span class="sxs-lookup"><span data-stu-id="eb67f-126">If set, interface is signal compatible with VESA Digital Flat Panel (DFP) 1.x Transition Minimized Differential Signaling (TMDS) CRGB, 1 pixel/clock, up to 8 bits/color most significant bit (MSB) aligned, DE active high.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb67f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb67f-127">Requirements</span></span>



| <span data-ttu-id="eb67f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb67f-128">Requirement</span></span> | <span data-ttu-id="eb67f-129">Value</span><span class="sxs-lookup"><span data-stu-id="eb67f-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb67f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb67f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="eb67f-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb67f-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="eb67f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb67f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="eb67f-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb67f-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="eb67f-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb67f-134">Namespace</span></span><br/>                | <span data-ttu-id="eb67f-135">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="eb67f-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="eb67f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="eb67f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb67f-137"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb67f-137"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb67f-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eb67f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb67f-139"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb67f-139"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb67f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb67f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb67f-141">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="eb67f-141">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




