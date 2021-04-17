---
description: Representa los datos sin procesar de una estructura de datos de identificación mejorada de la presentación extendida (E-EDID) de la Asociación estándar de vídeo electrónica (VESA).
ms.assetid: a51b73bb-a5f7-4e01-9c88-780105e9952b
title: Clase WmiMonitorRawEEdidV1Block
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorRawEEdidV1Block
- WmiMonitorRawEEdidV1Block.Active
- WmiMonitorRawEEdidV1Block.InstanceName
- WmiMonitorRawEEdidV1Block.Id
- WmiMonitorRawEEdidV1Block.Type
- WmiMonitorRawEEdidV1Block.Content
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 79566dccceb36281c9b3a94b19fed2ed5679dc8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716290"
---
# <a name="wmimonitorraweedidv1block-class"></a><span data-ttu-id="1ebdd-103">Clase WmiMonitorRawEEdidV1Block</span><span class="sxs-lookup"><span data-stu-id="1ebdd-103">WmiMonitorRawEEdidV1Block class</span></span>

<span data-ttu-id="1ebdd-104">La clase WMI **WmiMonitorRawEEdidV1Block** representa los datos sin procesar de una estructura de datos de identificación mejorada de la presentación extendida (E-EDID) de vídeo electrónica estándar (VESA).</span><span class="sxs-lookup"><span data-stu-id="1ebdd-104">The **WmiMonitorRawEEdidV1Block** WMI class represents the raw data from a Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure.</span></span> <span data-ttu-id="1ebdd-105">Esta estructura de datos de 128 bytes contiene información que describe la configuración óptima para una pantalla.</span><span class="sxs-lookup"><span data-stu-id="1ebdd-105">This 128-byte data structure contains information that describes the optimal configuration for a display.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ebdd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ebdd-106">Syntax</span></span>

``` syntax
class WmiMonitorRawEEdidV1Block : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint8   Id;
  uint8   Type;
  uint8   Content[];
};
```

## <a name="members"></a><span data-ttu-id="1ebdd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1ebdd-107">Members</span></span>

<span data-ttu-id="1ebdd-108">La clase **WmiMonitorRawEEdidV1Block** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1ebdd-108">The **WmiMonitorRawEEdidV1Block** class has these types of members:</span></span>

-   [<span data-ttu-id="1ebdd-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1ebdd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ebdd-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1ebdd-110">Properties</span></span>

<span data-ttu-id="1ebdd-111">La clase **WmiMonitorRawEEdidV1Block** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1ebdd-111">The **WmiMonitorRawEEdidV1Block** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ebdd-112">**Activo**</span><span class="sxs-lookup"><span data-stu-id="1ebdd-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebdd-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1ebdd-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ebdd-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1ebdd-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebdd-115">Indica el monitor activo.</span><span class="sxs-lookup"><span data-stu-id="1ebdd-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="1ebdd-116">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="1ebdd-116">**Content**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebdd-117">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="1ebdd-117">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1ebdd-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1ebdd-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebdd-119">128 matriz de bytes que contiene el contenido del bloque sin formato.</span><span class="sxs-lookup"><span data-stu-id="1ebdd-119">128 byte array that contains the raw block content.</span></span>

</dd> <dt>

<span data-ttu-id="1ebdd-120">**Id**</span><span class="sxs-lookup"><span data-stu-id="1ebdd-120">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebdd-121">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1ebdd-121">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1ebdd-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1ebdd-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebdd-123">Identidad del bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="1ebdd-123">Identity of the data block.</span></span>

</dd> <dt>

<span data-ttu-id="1ebdd-124">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="1ebdd-124">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebdd-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1ebdd-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ebdd-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1ebdd-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ebdd-127">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="1ebdd-127">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1ebdd-128">Nombre de la instancia de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="1ebdd-128">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="1ebdd-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1ebdd-129">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebdd-130">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1ebdd-130">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1ebdd-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1ebdd-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebdd-132">Tipo de bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="1ebdd-132">Type of data block.</span></span> <span data-ttu-id="1ebdd-133">En la tabla siguiente se enumeran los posibles valores que se pueden devolver.</span><span class="sxs-lookup"><span data-stu-id="1ebdd-133">The following table lists possible values that can be returned.</span></span>



| <span data-ttu-id="1ebdd-134">Value</span><span class="sxs-lookup"><span data-stu-id="1ebdd-134">Value</span></span>                                                                                 | <span data-ttu-id="1ebdd-135">Significado</span><span class="sxs-lookup"><span data-stu-id="1ebdd-135">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="1ebdd-136"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="1ebdd-136"><dt>0 (0x0)</dt></span></span> </dl>    | <span data-ttu-id="1ebdd-137">No inicializado</span><span class="sxs-lookup"><span data-stu-id="1ebdd-137">Uninitialized</span></span><br/>   |
| <dl> <span data-ttu-id="1ebdd-138"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="1ebdd-138"><dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="1ebdd-139">Bloque base EDID</span><span class="sxs-lookup"><span data-stu-id="1ebdd-139">EDID base block</span></span><br/> |
| <dl> <span data-ttu-id="1ebdd-140"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="1ebdd-140"><dt>2 (0x2)</dt></span></span> </dl>    | <span data-ttu-id="1ebdd-141">Asignación de bloques EDID</span><span class="sxs-lookup"><span data-stu-id="1ebdd-141">EDID block map</span></span><br/>  |
| <dl> <span data-ttu-id="1ebdd-142"><dt>255 (0xFF)</dt></span><span class="sxs-lookup"><span data-stu-id="1ebdd-142"><dt>255 (0xFF)</dt></span></span> </dl> | <span data-ttu-id="1ebdd-143">Otros</span><span class="sxs-lookup"><span data-stu-id="1ebdd-143">Other</span></span><br/>           |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ebdd-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ebdd-144">Requirements</span></span>



| <span data-ttu-id="1ebdd-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ebdd-145">Requirement</span></span> | <span data-ttu-id="1ebdd-146">Value</span><span class="sxs-lookup"><span data-stu-id="1ebdd-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ebdd-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ebdd-147">Minimum supported client</span></span><br/> | <span data-ttu-id="1ebdd-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ebdd-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1ebdd-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ebdd-149">Minimum supported server</span></span><br/> | <span data-ttu-id="1ebdd-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ebdd-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1ebdd-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1ebdd-151">Namespace</span></span><br/>                | <span data-ttu-id="1ebdd-152">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="1ebdd-152">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1ebdd-153">MOF</span><span class="sxs-lookup"><span data-stu-id="1ebdd-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ebdd-154"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ebdd-154"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ebdd-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1ebdd-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ebdd-156"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ebdd-156"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ebdd-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ebdd-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ebdd-158">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="1ebdd-158">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> <dt>

[<span data-ttu-id="1ebdd-159">**WmiGetMonitorRawEEdidV1Block**</span><span class="sxs-lookup"><span data-stu-id="1ebdd-159">**WmiGetMonitorRawEEdidV1Block**</span></span>](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md)
</dt> </dl>

 

 




