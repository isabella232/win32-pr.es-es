---
title: Asociar iconos a una categoría
description: Asociar iconos a una categoría
ms.assetid: 5e5c3c10-07cf-4a34-9822-97ec940b3117
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c7a662ab3aaf578f037ff246207d03e4fcd688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075249"
---
# <a name="associating-icons-with-a-category"></a><span data-ttu-id="70261-103">Asociar iconos a una categoría</span><span class="sxs-lookup"><span data-stu-id="70261-103">Associating Icons with a Category</span></span>

<span data-ttu-id="70261-104">La creación de una interfaz de usuario que permita al usuario seleccionar categorías de componentes dentro de una categoría requiere la posibilidad de mostrar una imagen significativa para una categoría determinada.</span><span class="sxs-lookup"><span data-stu-id="70261-104">Building a user interface that allows the user to select component categories within a category requires the ability to display a meaningful image for a particular category.</span></span> <span data-ttu-id="70261-105">Para asociar un icono a una categoría de componente, cree una clave para el CATId de la categoría y rellene esa clave con una subclave [DefaultIcon](defaulticon.md) .</span><span class="sxs-lookup"><span data-stu-id="70261-105">To associate an icon with a component category, create a key for the category's CATID and populate that key with a [DefaultIcon](defaulticon.md) subkey.</span></span> <span data-ttu-id="70261-106">La entrada del registro es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="70261-106">The registry entry is as follows:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

<span data-ttu-id="70261-107">El nombre de archivo al que hace referencia la clave DefaultIcon puede ser un archivo EXE o un archivo DLL (DLL de solo recursos).</span><span class="sxs-lookup"><span data-stu-id="70261-107">The filename referenced by the DefaultIcon key can be either an EXE or a DLL file (resource-only DLL).</span></span>

<span data-ttu-id="70261-108">Para asociar un pequeño mapa de bits del cuadro de herramientas de 16x16 con una categoría de componente, cree una clave en **HKEY \_ clases \_ raíz \\ CLSID** para el CATID de la categoría y rellene esa clave con una subclave [ToolBoxBitmap32](toolboxbitmap32.md) , como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="70261-108">To associate a small 16x16 "toolbox bitmap" with a component category, create a key in **HKEY\_CLASSES\_ROOT\\CLSID** for the category's CATID and populate that key with a [ToolBoxBitmap32](toolboxbitmap32.md) subkey, as shown in the following example:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

<span data-ttu-id="70261-109">El nombre de archivo al que hace referencia la clave [ToolBoxBitmap32](toolboxbitmap32.md) también puede ser un archivo exe o DLL (dll de solo recursos).</span><span class="sxs-lookup"><span data-stu-id="70261-109">The filename referenced by the [ToolBoxBitmap32](toolboxbitmap32.md) key can also be an EXE or DLL file (resource-only DLL).</span></span>

## <a name="related-topics"></a><span data-ttu-id="70261-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="70261-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70261-111">Categorización por funcionalidad de componentes</span><span class="sxs-lookup"><span data-stu-id="70261-111">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="70261-112">Clasificar por capacidades de contenedor</span><span class="sxs-lookup"><span data-stu-id="70261-112">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="70261-113">Clases y asociaciones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="70261-113">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="70261-114">Definir categorías de componentes</span><span class="sxs-lookup"><span data-stu-id="70261-114">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="70261-115">**ICatInformation**</span><span class="sxs-lookup"><span data-stu-id="70261-115">**ICatInformation**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[<span data-ttu-id="70261-116">**ICatRegister**</span><span class="sxs-lookup"><span data-stu-id="70261-116">**ICatRegister**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[<span data-ttu-id="70261-117">Administrador de categorías de componentes</span><span class="sxs-lookup"><span data-stu-id="70261-117">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




