---
description: ICE36 valida que cada icono de la tabla de iconos aparece al menos una vez en la propiedad ARPPRODUCTICON o en las tablas Class, ProgId o Shortcut.
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f24eebc1b591edde418c59b6765d7ee91a00dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082926"
---
# <a name="ice36"></a><span data-ttu-id="fc289-103">ICE36</span><span class="sxs-lookup"><span data-stu-id="fc289-103">ICE36</span></span>

<span data-ttu-id="fc289-104">ICE36 valida que cada icono de la tabla de iconos aparece al menos una vez en la propiedad [**ARPPRODUCTICON**](arpproducticon.md) o en las tablas [Class](class-table.md), [ProgID](progid-table.md)o [Shortcut](shortcut-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fc289-104">ICE36 validates that every icon in the Icon table is listed at least once in the [**ARPPRODUCTICON**](arpproducticon.md) property or the [Class](class-table.md), [ProgId](progid-table.md), or [Shortcut](shortcut-table.md) tables.</span></span>

<span data-ttu-id="fc289-105">Durante el anuncio, el instalador instala todos los iconos que aparecen en la [tabla de iconos](icon-table.md) en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="fc289-105">During advertisement, the installer installs all the icons listed in the [Icon table](icon-table.md) on the user's computer.</span></span> <span data-ttu-id="fc289-106">Tener iconos sin usar en la tabla de iconos no impide que la instalación se ejecute, pero sí aumenta innecesariamente el tamaño del archivo. msi y la hora y el espacio necesarios para anunciar una característica.</span><span class="sxs-lookup"><span data-stu-id="fc289-106">Having unused icons in the Icon table does not prevent the installation from running, however it does unnecessarily increase the size of the .msi file and the time and space required to advertise a feature.</span></span>

<span data-ttu-id="fc289-107">Si no se hace referencia a un icono en la propiedad o la tabla y no se proporciona ninguna interfaz de usuario para crear una referencia en tiempo de ejecución, debe quitar el icono para lograr un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="fc289-107">If an icon is not referenced in the property or table and there is no UI provided to create a reference at run time, you should remove the icon to achieve better performance.</span></span>

## <a name="result"></a><span data-ttu-id="fc289-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="fc289-108">Result</span></span>

<span data-ttu-id="fc289-109">ICE36 envía un mensaje si hay un icono en la tabla de iconos al que no se hace referencia en las tablas [Class](class-table.md), [ProgID](progid-table.md)o [Shortcut](shortcut-table.md) y si no se proporciona ninguna interfaz de usuario para crear dicha referencia en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="fc289-109">ICE36 posts a message if there is a icon in the Icon table that is not referenced in the [Class](class-table.md), [ProgId](progid-table.md), or [Shortcut](shortcut-table.md) tables and if there is no UI provided to create such a reference at run time.</span></span>

## <a name="example"></a><span data-ttu-id="fc289-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc289-110">Example</span></span>

<span data-ttu-id="fc289-111">ICE36 notifica el siguiente error para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="fc289-111">ICE36 reports the following error for the example shown.</span></span>

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

<span data-ttu-id="fc289-112">[Tabla de iconos](icon-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="fc289-112">[Icon Table](icon-table.md) (partial)</span></span>



| <span data-ttu-id="fc289-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="fc289-113">Name</span></span>  | <span data-ttu-id="fc289-114">Datos</span><span class="sxs-lookup"><span data-stu-id="fc289-114">Data</span></span>     |
|-------|----------|
| <span data-ttu-id="fc289-115">Icon1</span><span class="sxs-lookup"><span data-stu-id="fc289-115">Icon1</span></span> | <span data-ttu-id="fc289-116">Control1</span><span class="sxs-lookup"><span data-stu-id="fc289-116">Control1</span></span> |
| <span data-ttu-id="fc289-117">Icon2</span><span class="sxs-lookup"><span data-stu-id="fc289-117">Icon2</span></span> | <span data-ttu-id="fc289-118">Control2</span><span class="sxs-lookup"><span data-stu-id="fc289-118">Control2</span></span> |
| <span data-ttu-id="fc289-119">Icon3</span><span class="sxs-lookup"><span data-stu-id="fc289-119">Icon3</span></span> | <span data-ttu-id="fc289-120">Control3</span><span class="sxs-lookup"><span data-stu-id="fc289-120">Control3</span></span> |
| <span data-ttu-id="fc289-121">Icon4</span><span class="sxs-lookup"><span data-stu-id="fc289-121">Icon4</span></span> | <span data-ttu-id="fc289-122">Control4</span><span class="sxs-lookup"><span data-stu-id="fc289-122">Control4</span></span> |



 

<span data-ttu-id="fc289-123">[Tabla ProgID](progid-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="fc289-123">[ProgID Table](progid-table.md) (partial)</span></span>



| <span data-ttu-id="fc289-124">ProgID</span><span class="sxs-lookup"><span data-stu-id="fc289-124">ProgID</span></span>    |
|-----------|
| <span data-ttu-id="fc289-125">Property1</span><span class="sxs-lookup"><span data-stu-id="fc289-125">Property1</span></span> |



 

<span data-ttu-id="fc289-126">[Tabla de clases](class-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="fc289-126">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="fc289-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="fc289-127">CLSID</span></span>                                  |
|----------------------------------------|
| <span data-ttu-id="fc289-128">{3E469ABA-3644-11d2-8892-00A0C981B015}</span><span class="sxs-lookup"><span data-stu-id="fc289-128">{3E469ABA-3644-11d2-8892-00A0C981B015}</span></span> |



 

<span data-ttu-id="fc289-129">[Tabla de acceso directo](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="fc289-129">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="fc289-130">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="fc289-130">Shortcut</span></span>  | <span data-ttu-id="fc289-131">Icono\_</span><span class="sxs-lookup"><span data-stu-id="fc289-131">Icon\_</span></span> |
|-----------|--------|
| <span data-ttu-id="fc289-132">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="fc289-132">Shortcut1</span></span> | <span data-ttu-id="fc289-133">Icon2</span><span class="sxs-lookup"><span data-stu-id="fc289-133">Icon2</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="fc289-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc289-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc289-135">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="fc289-135">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



