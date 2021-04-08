---
description: La tabla ReserveCost es una tabla opcional que permite al autor reservar una cantidad de espacio en disco en cualquier directorio que dependa del estado de instalación de un componente.
ms.assetid: 371e72f1-40a2-4ed2-b0ab-33840075ff47
title: Tabla ReserveCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f593fd11789cd2304385b97e96e50a009fbde0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002196"
---
# <a name="reservecost-table"></a><span data-ttu-id="4a9fe-103">Tabla ReserveCost</span><span class="sxs-lookup"><span data-stu-id="4a9fe-103">ReserveCost Table</span></span>

<span data-ttu-id="4a9fe-104">La tabla ReserveCost es una tabla opcional que permite al autor reservar una cantidad de espacio en disco en cualquier directorio que dependa del estado de instalación de un componente.</span><span class="sxs-lookup"><span data-stu-id="4a9fe-104">The ReserveCost table is an optional table that allows the author to reserve an amount of disk space in any directory that depends on the installation state of a component.</span></span>

<span data-ttu-id="4a9fe-105">La tabla ReserveCost tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="4a9fe-105">The ReserveCost table has the following columns.</span></span>



| <span data-ttu-id="4a9fe-106">Columna</span><span class="sxs-lookup"><span data-stu-id="4a9fe-106">Column</span></span>        | <span data-ttu-id="4a9fe-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a9fe-107">Type</span></span>                               | <span data-ttu-id="4a9fe-108">Clave</span><span class="sxs-lookup"><span data-stu-id="4a9fe-108">Key</span></span> | <span data-ttu-id="4a9fe-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="4a9fe-109">Nullable</span></span> |
|---------------|------------------------------------|-----|----------|
| <span data-ttu-id="4a9fe-110">ReserveKey</span><span class="sxs-lookup"><span data-stu-id="4a9fe-110">ReserveKey</span></span>    | [<span data-ttu-id="4a9fe-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="4a9fe-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="4a9fe-112">Y</span><span class="sxs-lookup"><span data-stu-id="4a9fe-112">Y</span></span>   | <span data-ttu-id="4a9fe-113">N</span><span class="sxs-lookup"><span data-stu-id="4a9fe-113">N</span></span>        |
| <span data-ttu-id="4a9fe-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="4a9fe-114">Component\_</span></span>   | [<span data-ttu-id="4a9fe-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="4a9fe-115">Identifier</span></span>](identifier.md)       | <span data-ttu-id="4a9fe-116">N</span><span class="sxs-lookup"><span data-stu-id="4a9fe-116">N</span></span>   | <span data-ttu-id="4a9fe-117">N</span><span class="sxs-lookup"><span data-stu-id="4a9fe-117">N</span></span>        |
| <span data-ttu-id="4a9fe-118">ReserveFolder</span><span class="sxs-lookup"><span data-stu-id="4a9fe-118">ReserveFolder</span></span> | [<span data-ttu-id="4a9fe-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="4a9fe-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="4a9fe-120">N</span><span class="sxs-lookup"><span data-stu-id="4a9fe-120">N</span></span>   | <span data-ttu-id="4a9fe-121">Y</span><span class="sxs-lookup"><span data-stu-id="4a9fe-121">Y</span></span>        |
| <span data-ttu-id="4a9fe-122">ReserveLocal</span><span class="sxs-lookup"><span data-stu-id="4a9fe-122">ReserveLocal</span></span>  | [<span data-ttu-id="4a9fe-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="4a9fe-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="4a9fe-124">N</span><span class="sxs-lookup"><span data-stu-id="4a9fe-124">N</span></span>   | <span data-ttu-id="4a9fe-125">N</span><span class="sxs-lookup"><span data-stu-id="4a9fe-125">N</span></span>        |
| <span data-ttu-id="4a9fe-126">ReserveSource</span><span class="sxs-lookup"><span data-stu-id="4a9fe-126">ReserveSource</span></span> | [<span data-ttu-id="4a9fe-127">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="4a9fe-127">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="4a9fe-128">N</span><span class="sxs-lookup"><span data-stu-id="4a9fe-128">N</span></span>   | <span data-ttu-id="4a9fe-129">N</span><span class="sxs-lookup"><span data-stu-id="4a9fe-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="4a9fe-130">Columnas</span><span class="sxs-lookup"><span data-stu-id="4a9fe-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="4a9fe-131"><span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey</span><span class="sxs-lookup"><span data-stu-id="4a9fe-131"><span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey</span></span>
</dt> <dd>

<span data-ttu-id="4a9fe-132">Clave principal que identifica de forma única una entrada de la tabla ReserveCost.</span><span class="sxs-lookup"><span data-stu-id="4a9fe-132">Primary key that uniquely identifies a ReserveCost table entry.</span></span>

</dd> <dt>

<span data-ttu-id="4a9fe-133"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="4a9fe-133"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="4a9fe-134">Clave externa para la columna uno de la tabla de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="4a9fe-134">External key to column one of the [Component](component-table.md) table.</span></span> <span data-ttu-id="4a9fe-135">Reserva una cantidad especificada de espacio si se va a instalar este componente.</span><span class="sxs-lookup"><span data-stu-id="4a9fe-135">Reserves a specified amount of space if this component is to be installed.</span></span>

</dd> <dt>

<span data-ttu-id="4a9fe-136"><span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder</span><span class="sxs-lookup"><span data-stu-id="4a9fe-136"><span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder</span></span>
</dt> <dd>

<span data-ttu-id="4a9fe-137">Esta columna contiene el nombre de una propiedad que es la ruta de acceso completa al directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="4a9fe-137">This column contains the name of a property that is the full path to the destination directory.</span></span> <span data-ttu-id="4a9fe-138">Este nombre de propiedad suele ser el nombre de un directorio en la tabla del [directorio](directory-table.md) o el nombre de un conjunto de propiedades obtenido mediante la acción [AppSearch](appsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="4a9fe-138">This property name is typically the name of a directory in the [Directory](directory-table.md) table or the name of a property set obtained using the [Appsearch](appsearch-action.md) action.</span></span> <span data-ttu-id="4a9fe-139">Esto agrega la cantidad de espacio en disco especificada en ReserveLocal o ReserveSource al costo del volumen del dispositivo que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="4a9fe-139">This adds the amount of disk space specified in ReserveLocal or ReserveSource to the volume cost of the device containing the directory.</span></span>

</dd> <dt>

<span data-ttu-id="4a9fe-140"><span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal</span><span class="sxs-lookup"><span data-stu-id="4a9fe-140"><span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal</span></span>
</dt> <dd>

<span data-ttu-id="4a9fe-141">El número de bytes de espacio en disco que se reservan si el componente vinculado está instalado para ejecutarse localmente.</span><span class="sxs-lookup"><span data-stu-id="4a9fe-141">The number of bytes of disk space to reserve if the linked component is installed to run locally.</span></span>

</dd> <dt>

<span data-ttu-id="4a9fe-142"><span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource</span><span class="sxs-lookup"><span data-stu-id="4a9fe-142"><span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource</span></span>
</dt> <dd>

<span data-ttu-id="4a9fe-143">El número de bytes de espacio en disco que se reservan si el componente vinculado está instalado para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="4a9fe-143">The number of bytes of disk space to reserve if the linked component is installed to run from source.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a9fe-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a9fe-144">Remarks</span></span>

<span data-ttu-id="4a9fe-145">El costo de la reserva de esta manera podría ser útil para los autores que deseen asegurarse de que habrá una cantidad mínima de espacio en disco disponible una vez completada la instalación.</span><span class="sxs-lookup"><span data-stu-id="4a9fe-145">Reserving cost in this way could be useful for authors who want to ensure that a minimum amount of disk space will be available after the installation is completed.</span></span> <span data-ttu-id="4a9fe-146">Por ejemplo, puede que este espacio en disco esté reservado para documentos de usuario o para archivos de aplicación (como archivos de índice) que se crean solo después de que la aplicación se inicie después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="4a9fe-146">For example, this disk space might be reserved for user documents or for application files (such as index files) that are created only after the application is started following installation.</span></span>

<span data-ttu-id="4a9fe-147">Puede usar la tabla ReserveCost para habilitar las acciones personalizadas con el fin de especificar un costo aproximado para los archivos, entradas del registro u otros elementos que pueda instalar la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="4a9fe-147">You can use the ReserveCost table to enable custom actions to specify an approximate cost for any files, registry entries, or other items that the custom action might install.</span></span> <span data-ttu-id="4a9fe-148">Las acciones personalizadas que agregan entradas a la tabla ReserveCost se deben secuenciar entre las acciones [CostInitialize](costinitialize-action.md) y [FileCost](filecost-action.md) .</span><span class="sxs-lookup"><span data-stu-id="4a9fe-148">Custom actions that add entries to the ReserveCost table should be sequenced between the [CostInitialize](costinitialize-action.md) and [FileCost](filecost-action.md) actions.</span></span> <span data-ttu-id="4a9fe-149">Esto es necesario para que la acción FileCost inicialice correctamente el costo de todos los componentes afectados por las entradas de la tabla ReserveCost.</span><span class="sxs-lookup"><span data-stu-id="4a9fe-149">This is necessary for the FileCost action to correctly initialize the costing of all components affected by entries in the ReserveCost table.</span></span>

## <a name="validation"></a><span data-ttu-id="4a9fe-150">Validación</span><span class="sxs-lookup"><span data-stu-id="4a9fe-150">Validation</span></span>

<dl>

[<span data-ttu-id="4a9fe-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="4a9fe-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="4a9fe-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="4a9fe-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="4a9fe-153">ICE32</span><span class="sxs-lookup"><span data-stu-id="4a9fe-153">ICE32</span></span>](ice32.md)  
</dl>

 

 



