---
description: El objeto UIPreview se usa para ver los cuadros de diálogo y las cartelera de la interfaz de usuario durante la creación. Este objeto se crea mediante el método EnableUIPreview del objeto de base de datos.
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: Objeto UIPreview
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6650dc9bcc66a24d0e8a9d7f0d971884a2379f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679556"
---
# <a name="uipreview-object"></a><span data-ttu-id="9b664-104">Objeto UIPreview</span><span class="sxs-lookup"><span data-stu-id="9b664-104">UIPreview object</span></span>

<span data-ttu-id="9b664-105">El objeto **UIPreview** se usa para ver los cuadros de diálogo y las cartelera de la interfaz de usuario durante la creación.</span><span class="sxs-lookup"><span data-stu-id="9b664-105">The **UIPreview** object is used to view user interface dialog boxes and billboards during authoring.</span></span> <span data-ttu-id="9b664-106">Este objeto se crea mediante el método [**EnableUIPreview**](database-enableuipreview.md) del objeto de [**base de datos**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9b664-106">This object is created by the [**EnableUIPreview**](database-enableuipreview.md) method of the [**Database**](database-object.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="9b664-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9b664-107">Members</span></span>

<span data-ttu-id="9b664-108">El objeto **UIPreview** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9b664-108">The **UIPreview** object has these types of members:</span></span>

-   [<span data-ttu-id="9b664-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="9b664-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="9b664-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b664-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9b664-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9b664-111">Methods</span></span>

<span data-ttu-id="9b664-112">El objeto **UIPreview** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9b664-112">The **UIPreview** object has these methods.</span></span>



| <span data-ttu-id="9b664-113">Método</span><span class="sxs-lookup"><span data-stu-id="9b664-113">Method</span></span>                                           | <span data-ttu-id="9b664-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b664-114">Description</span></span>                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b664-115">**ViewBillboard**</span><span class="sxs-lookup"><span data-stu-id="9b664-115">**ViewBillboard**</span></span>](uipreview-viewbillboard.md) | <span data-ttu-id="9b664-116">Muestra una cartelera creada mediante el control host del cuadro de diálogo que se muestra actualmente.</span><span class="sxs-lookup"><span data-stu-id="9b664-116">Displays an authored billboard using the host control in the currently displayed dialog box.</span></span><br/> |
| [<span data-ttu-id="9b664-117">**ViewDialog**</span><span class="sxs-lookup"><span data-stu-id="9b664-117">**ViewDialog**</span></span>](uipreview-viewdialog.md)       | <span data-ttu-id="9b664-118">Muestra un cuadro de diálogo de interfaz de usuario creado almacenado en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="9b664-118">Displays an authored UI dialog box stored in the current database.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="9b664-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b664-119">Properties</span></span>

<span data-ttu-id="9b664-120">El objeto **UIPreview** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9b664-120">The **UIPreview** object has these properties.</span></span>



| <span data-ttu-id="9b664-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9b664-121">Property</span></span>                                          | <span data-ttu-id="9b664-122">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="9b664-122">Access type</span></span>           | <span data-ttu-id="9b664-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b664-123">Description</span></span>                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b664-124">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="9b664-124">**Property**</span></span>](uipreview-property.md)<br/> | <span data-ttu-id="9b664-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9b664-125">Read/write</span></span><br/> | <span data-ttu-id="9b664-126">Representa el valor de cadena de una propiedad de instalador con nombre o, si tiene como prefijo un signo de porcentaje (%), el valor de una variable de entorno del sistema para el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="9b664-126">Represents the string value of a named installer property or, if prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9b664-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b664-127">Requirements</span></span>



| <span data-ttu-id="9b664-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b664-128">Requirement</span></span> | <span data-ttu-id="9b664-129">Value</span><span class="sxs-lookup"><span data-stu-id="9b664-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b664-130">Versión</span><span class="sxs-lookup"><span data-stu-id="9b664-130">Version</span></span><br/> | <span data-ttu-id="9b664-131">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9b664-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9b664-132">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9b664-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9b664-133">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="9b664-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9b664-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b664-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="9b664-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b664-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9b664-136">IID</span><span class="sxs-lookup"><span data-stu-id="9b664-136">IID</span></span><br/>     | <span data-ttu-id="9b664-137">IID \_ IUIPreview se define como 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9b664-137">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="9b664-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b664-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b664-139">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="9b664-139">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




