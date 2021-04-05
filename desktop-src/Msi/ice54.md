---
description: ICE54 comprueba los componentes que usan un archivo complementario como su ruta de acceso de clave.
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df2ba90ccb44e33b67aaf8ecdcadc723e8d2fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910094"
---
# <a name="ice54"></a><span data-ttu-id="1b3a6-103">ICE54</span><span class="sxs-lookup"><span data-stu-id="1b3a6-103">ICE54</span></span>

<span data-ttu-id="1b3a6-104">ICE54 comprueba los componentes que usan un archivo complementario como su ruta de acceso de clave.</span><span class="sxs-lookup"><span data-stu-id="1b3a6-104">ICE54 checks for components that use a companion file as their key path.</span></span>

<span data-ttu-id="1b3a6-105">El archivo de ruta de acceso de la clave de un componente no debe derivar su versión de un archivo diferente.</span><span class="sxs-lookup"><span data-stu-id="1b3a6-105">The key path file of a component must not derive its version from a different file.</span></span> <span data-ttu-id="1b3a6-106">Esto puede hacer que algunos archivos no se instalen.</span><span class="sxs-lookup"><span data-stu-id="1b3a6-106">This can cause some files to fail to install.</span></span> <span data-ttu-id="1b3a6-107">Vea la [tabla de archivos](file-table.md) para obtener más información acerca de los archivos complementarios.</span><span class="sxs-lookup"><span data-stu-id="1b3a6-107">See the [File table](file-table.md) for more information about companion files.</span></span>

## <a name="result"></a><span data-ttu-id="1b3a6-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="1b3a6-108">Result</span></span>

<span data-ttu-id="1b3a6-109">ICE54 publica una advertencia si algún componente tiene un archivo de ruta de acceso de clave que deriva su versión de otro archivo.</span><span class="sxs-lookup"><span data-stu-id="1b3a6-109">ICE54 posts a warning if any component has a key path file that derives its version from another file.</span></span>

## <a name="example"></a><span data-ttu-id="1b3a6-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1b3a6-110">Example</span></span>

<span data-ttu-id="1b3a6-111">ICE54 devuelve la siguiente advertencia para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="1b3a6-111">ICE54 returns the following warning for the example shown.</span></span>

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

<span data-ttu-id="1b3a6-112">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="1b3a6-112">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="1b3a6-113">Componente</span><span class="sxs-lookup"><span data-stu-id="1b3a6-113">Component</span></span>  | <span data-ttu-id="1b3a6-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="1b3a6-114">Attribute</span></span> | <span data-ttu-id="1b3a6-115">Rutas</span><span class="sxs-lookup"><span data-stu-id="1b3a6-115">KeyPath</span></span> |
|------------|-----------|---------|
| <span data-ttu-id="1b3a6-116">Component1</span><span class="sxs-lookup"><span data-stu-id="1b3a6-116">Component1</span></span> | <span data-ttu-id="1b3a6-117">0</span><span class="sxs-lookup"><span data-stu-id="1b3a6-117">0</span></span>         | <span data-ttu-id="1b3a6-118">Archivo1</span><span class="sxs-lookup"><span data-stu-id="1b3a6-118">File1</span></span>   |



 

<span data-ttu-id="1b3a6-119">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="1b3a6-119">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="1b3a6-120">Archivo</span><span class="sxs-lookup"><span data-stu-id="1b3a6-120">File</span></span>  | <span data-ttu-id="1b3a6-121">Versión</span><span class="sxs-lookup"><span data-stu-id="1b3a6-121">Version</span></span> | <span data-ttu-id="1b3a6-122">Idioma</span><span class="sxs-lookup"><span data-stu-id="1b3a6-122">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="1b3a6-123">Archivo1</span><span class="sxs-lookup"><span data-stu-id="1b3a6-123">File1</span></span> | <span data-ttu-id="1b3a6-124">Archivo2</span><span class="sxs-lookup"><span data-stu-id="1b3a6-124">File2</span></span>   |          |
| <span data-ttu-id="1b3a6-125">Archivo2</span><span class="sxs-lookup"><span data-stu-id="1b3a6-125">File2</span></span> | <span data-ttu-id="1b3a6-126">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="1b3a6-126">1.0.0.0</span></span> | <span data-ttu-id="1b3a6-127">3082</span><span class="sxs-lookup"><span data-stu-id="1b3a6-127">1033</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="1b3a6-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b3a6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b3a6-129">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="1b3a6-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



