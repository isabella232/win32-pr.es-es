---
description: Para cada contraseña que debe escribir el usuario, agregue un control de edición en un cuadro de diálogo que almacene el valor de la contraseña en una propiedad.
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Crear la interfaz de usuario para la entrada de contraseña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37cd7bb9531cbf63a443011656f200717dc0214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667026"
---
# <a name="authoring-the-user-interface-for-password-input"></a><span data-ttu-id="64455-103">Crear la interfaz de usuario para la entrada de contraseña</span><span class="sxs-lookup"><span data-stu-id="64455-103">Authoring the User Interface for Password Input</span></span>

<span data-ttu-id="64455-104">Para cada contraseña que debe escribir el usuario, agregue un control de edición en un cuadro de diálogo que almacene el valor de la contraseña en una propiedad.</span><span class="sxs-lookup"><span data-stu-id="64455-104">For each password that must be entered by the user, add an edit control on a dialog that stores the value of the password into a property.</span></span> <span data-ttu-id="64455-105">Este [control de edición](edit-control.md) debe tener el [atributo de control de contraseña](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="64455-105">This [edit control](edit-control.md) should have the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="64455-106">Esto especifica que la propiedad especificada es una contraseña e impide que el instalador escriba la propiedad en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="64455-106">This specifies that the property entered is a password and prevents the installer from writing the property to the log file.</span></span>

<span data-ttu-id="64455-107">Los [atributos de control](control-attributes.md) del control de edición de contraseña son MsidbControlAttributesVisible, MsidbControlAttributesEnabled y msidbControlAttributesPasswordInput (1 + 2 + 2097152).</span><span class="sxs-lookup"><span data-stu-id="64455-107">The [control attributes](control-attributes.md) for the password edit control are msidbControlAttributesVisible, msidbControlAttributesEnabled, and msidbControlAttributesPasswordInput (1 + 2 + 2097152).</span></span> <span data-ttu-id="64455-108">Los valores X, Y, ancho, alto y control \_ siguiente dependen del diseño del control en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="64455-108">The X, Y, Width, Height, and Control\_Next depend on the layout of the control on the dialog.</span></span>

[<span data-ttu-id="64455-109">Tabla de control</span><span class="sxs-lookup"><span data-stu-id="64455-109">Control Table</span></span>](control-table.md)



| <span data-ttu-id="64455-110">Diálogo\_</span><span class="sxs-lookup"><span data-stu-id="64455-110">Dialog\_</span></span> | <span data-ttu-id="64455-111">control\_</span><span class="sxs-lookup"><span data-stu-id="64455-111">Control\_</span></span>            | <span data-ttu-id="64455-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="64455-112">Type</span></span> | <span data-ttu-id="64455-113">X</span><span class="sxs-lookup"><span data-stu-id="64455-113">X</span></span>   | <span data-ttu-id="64455-114">Y</span><span class="sxs-lookup"><span data-stu-id="64455-114">Y</span></span>   | <span data-ttu-id="64455-115">Ancho</span><span class="sxs-lookup"><span data-stu-id="64455-115">Width</span></span> | <span data-ttu-id="64455-116">Alto</span><span class="sxs-lookup"><span data-stu-id="64455-116">Height</span></span> | <span data-ttu-id="64455-117">Atributos</span><span class="sxs-lookup"><span data-stu-id="64455-117">Attributes</span></span> | <span data-ttu-id="64455-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="64455-118">Property</span></span>         | <span data-ttu-id="64455-119">Texto</span><span class="sxs-lookup"><span data-stu-id="64455-119">Text</span></span> | <span data-ttu-id="64455-120">Control \_ siguiente</span><span class="sxs-lookup"><span data-stu-id="64455-120">Control\_Next</span></span> | <span data-ttu-id="64455-121">Ayuda</span><span class="sxs-lookup"><span data-stu-id="64455-121">Help</span></span> |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| <span data-ttu-id="64455-122">Cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="64455-122">MyDialog</span></span> | <span data-ttu-id="64455-123">TestUserPasswordEdit</span><span class="sxs-lookup"><span data-stu-id="64455-123">TestUserPasswordEdit</span></span> | <span data-ttu-id="64455-124">Editar</span><span class="sxs-lookup"><span data-stu-id="64455-124">Edit</span></span> | <span data-ttu-id="64455-125">25</span><span class="sxs-lookup"><span data-stu-id="64455-125">25</span></span>  | <span data-ttu-id="64455-126">120</span><span class="sxs-lookup"><span data-stu-id="64455-126">120</span></span> | <span data-ttu-id="64455-127">300</span><span class="sxs-lookup"><span data-stu-id="64455-127">300</span></span>   | <span data-ttu-id="64455-128">20</span><span class="sxs-lookup"><span data-stu-id="64455-128">20</span></span>     | <span data-ttu-id="64455-129">2097155</span><span class="sxs-lookup"><span data-stu-id="64455-129">2097155</span></span>    | <span data-ttu-id="64455-130">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="64455-130">TESTUSERPASSWORD</span></span> |      | <span data-ttu-id="64455-131">Cancelar</span><span class="sxs-lookup"><span data-stu-id="64455-131">Cancel</span></span>        |      |



 

<span data-ttu-id="64455-132">Continúe con [la protección de la instalación](securing-the-installation.md).</span><span class="sxs-lookup"><span data-stu-id="64455-132">Continue to [Securing the installation](securing-the-installation.md).</span></span>

 

 



