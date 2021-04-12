---
description: ICE45 valida que las columnas de campo de bits de la base de datos no establezcan ningún bit reservado en 1.
ms.assetid: 43fa5e9c-2059-4217-8f8e-c194e37f238a
title: ICE45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0651d94c296ae14f66b562841c3c4e2bca7b8e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276509"
---
# <a name="ice45"></a><span data-ttu-id="3dda2-103">ICE45</span><span class="sxs-lookup"><span data-stu-id="3dda2-103">ICE45</span></span>

<span data-ttu-id="3dda2-104">ICE45 valida que las columnas de campo de bits de la base de datos no establezcan ningún bit reservado en 1.</span><span class="sxs-lookup"><span data-stu-id="3dda2-104">ICE45 validates that bit field columns in the database do not set any reserved bits to 1.</span></span>

<span data-ttu-id="3dda2-105">Los bits reservados no proporcionan ninguna funcionalidad en las versiones actuales del instalador, pero pueden en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="3dda2-105">Reserved bits provide no functionality in current versions of the installer, but might in future versions.</span></span> <span data-ttu-id="3dda2-106">Deben establecerse en 0 para ser compatibles con versiones futuras de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3dda2-106">They should be set to 0 to be compatible with future versions of Windows Installer.</span></span>

## <a name="result"></a><span data-ttu-id="3dda2-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="3dda2-107">Result</span></span>

<span data-ttu-id="3dda2-108">ICE45 envía un mensaje de error si alguna de las tablas siguientes contiene un campo de bits con un bit reservado establecido en un valor de 1.</span><span class="sxs-lookup"><span data-stu-id="3dda2-108">ICE45 posts an error message if any of the following tables contains a bit field with a reserved bit set to a value of 1.</span></span>

-   [<span data-ttu-id="3dda2-109">Tabla BBControl</span><span class="sxs-lookup"><span data-stu-id="3dda2-109">BBControl table</span></span>](bbcontrol-table.md)
-   [<span data-ttu-id="3dda2-110">Tabla de cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="3dda2-110">Dialog table</span></span>](dialog-table.md)
-   [<span data-ttu-id="3dda2-111">Tabla de características</span><span class="sxs-lookup"><span data-stu-id="3dda2-111">Feature table</span></span>](feature-table.md)
-   [<span data-ttu-id="3dda2-112">Tabla de archivos</span><span class="sxs-lookup"><span data-stu-id="3dda2-112">File table</span></span>](file-table.md)
-   [<span data-ttu-id="3dda2-113">Tabla MoveFile</span><span class="sxs-lookup"><span data-stu-id="3dda2-113">MoveFile table</span></span>](movefile-table.md)
-   [<span data-ttu-id="3dda2-114">Tabla ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3dda2-114">ModuleConfiguration table</span></span>](moduleconfiguration-table.md)
-   [<span data-ttu-id="3dda2-115">Tabla ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="3dda2-115">ODBCDataSource table</span></span>](odbcdatasource-table.md)
-   [<span data-ttu-id="3dda2-116">Tabla de revisión</span><span class="sxs-lookup"><span data-stu-id="3dda2-116">Patch table</span></span>](patch-table.md)
-   [<span data-ttu-id="3dda2-117">Tabla RemoveFile</span><span class="sxs-lookup"><span data-stu-id="3dda2-117">RemoveFile table</span></span>](removefile-table.md)
-   [<span data-ttu-id="3dda2-118">Tabla ServiceControl</span><span class="sxs-lookup"><span data-stu-id="3dda2-118">ServiceControl table</span></span>](servicecontrol-table.md)
-   [<span data-ttu-id="3dda2-119">Tabla ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="3dda2-119">ServiceInstall table</span></span>](serviceinstall-table.md)
-   [<span data-ttu-id="3dda2-120">Tabla de TextStyle</span><span class="sxs-lookup"><span data-stu-id="3dda2-120">TextStyle table</span></span>](textstyle-table.md)

<span data-ttu-id="3dda2-121">ICE45 envía uno de dos mensajes de advertencia si la [tabla de control](control-table.md) contiene un campo de bits con un bit reservado establecido en un valor de 1.</span><span class="sxs-lookup"><span data-stu-id="3dda2-121">ICE45 posts one of two warning messages if the [Control Table](control-table.md) contains a bit field with a reserved bit set to a value of 1.</span></span>

## <a name="example"></a><span data-ttu-id="3dda2-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3dda2-122">Example</span></span>

<span data-ttu-id="3dda2-123">ICE45 notifica el siguiente error para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="3dda2-123">ICE45 reports the following error for the example shown.</span></span>

``` syntax
Row 'File1' in table 'File' has bits set in the 'Attributes' 
    column that are reserved. They must be 0 to ensure 
    compatibility with future installer versions.
```

<span data-ttu-id="3dda2-124">ICE45 notifica la siguiente advertencia para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="3dda2-124">ICE45 reports the following warning for the example shown.</span></span>

``` syntax
Row 'Dialog1.Edit2' in table 'Control' has bits set in the 'Attribute' 
    column that are reserved. They should be 0 to ensure compatibility 
    with future installer versions.
```

<span data-ttu-id="3dda2-125">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="3dda2-125">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="3dda2-126">Archivo</span><span class="sxs-lookup"><span data-stu-id="3dda2-126">File</span></span>  | <span data-ttu-id="3dda2-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="3dda2-127">Attributes</span></span> |
|-------|------------|
| <span data-ttu-id="3dda2-128">Archivo1</span><span class="sxs-lookup"><span data-stu-id="3dda2-128">File1</span></span> | <span data-ttu-id="3dda2-129">128</span><span class="sxs-lookup"><span data-stu-id="3dda2-129">128</span></span>        |



 

<span data-ttu-id="3dda2-130">[Tabla de control](control-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="3dda2-130">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="3dda2-131">Diálogo</span><span class="sxs-lookup"><span data-stu-id="3dda2-131">Dialog</span></span>  | <span data-ttu-id="3dda2-132">Control</span><span class="sxs-lookup"><span data-stu-id="3dda2-132">Control</span></span> | <span data-ttu-id="3dda2-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="3dda2-133">Attributes</span></span> |
|---------|---------|------------|
| <span data-ttu-id="3dda2-134">Dialog1</span><span class="sxs-lookup"><span data-stu-id="3dda2-134">Dialog1</span></span> | <span data-ttu-id="3dda2-135">Edit1</span><span class="sxs-lookup"><span data-stu-id="3dda2-135">Edit1</span></span>   | <span data-ttu-id="3dda2-136">2 097 152</span><span class="sxs-lookup"><span data-stu-id="3dda2-136">2097152</span></span>    |
| <span data-ttu-id="3dda2-137">Dialog1</span><span class="sxs-lookup"><span data-stu-id="3dda2-137">Dialog1</span></span> | <span data-ttu-id="3dda2-138">Edit2</span><span class="sxs-lookup"><span data-stu-id="3dda2-138">Edit2</span></span>   | <span data-ttu-id="3dda2-139">1 048 576</span><span class="sxs-lookup"><span data-stu-id="3dda2-139">1048576</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="3dda2-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3dda2-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dda2-141">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="3dda2-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



