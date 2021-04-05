---
title: Clasificar por capacidades de contenedor
description: A menudo, los componentes requieren cierta funcionalidad del contenedor y no funcionarán con un contenedor que no proporcione la compatibilidad.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987546c20ff77a40666bb74689466a15fab989a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076290"
---
# <a name="categorizing-by-container-capabilities"></a><span data-ttu-id="57f24-103">Clasificar por capacidades de contenedor</span><span class="sxs-lookup"><span data-stu-id="57f24-103">Categorizing by Container Capabilities</span></span>

<span data-ttu-id="57f24-104">A menudo, los componentes requieren cierta funcionalidad del contenedor y no funcionarán con un contenedor que no proporcione la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="57f24-104">Components often require certain functionality from the container and will not work with a container that does not provide the support.</span></span> <span data-ttu-id="57f24-105">La interfaz de usuario debe filtrar los componentes que requieren funcionalidad que el contenedor no admite.</span><span class="sxs-lookup"><span data-stu-id="57f24-105">The user interface should filter out components that require functionality the container does not support.</span></span> <span data-ttu-id="57f24-106">Para ello, los componentes se pueden clasificar por la funcionalidad de contenedor requerida.</span><span class="sxs-lookup"><span data-stu-id="57f24-106">To accomplish this, components can be categorized by the required container functionality.</span></span>

<span data-ttu-id="57f24-107">Un ejemplo de componentes que requieren funcionalidad del contenedor y que no funcionan en contenedores que no admiten esa funcionalidad son controles OLE de marco sencillos.</span><span class="sxs-lookup"><span data-stu-id="57f24-107">An example of components that require functionality from the container and do not work in containers that do not support that functionality are simple frame OLE controls.</span></span> <span data-ttu-id="57f24-108">La categorización por funciones de contenedor se realiza mediante una clave del registro adicional dentro de la clave CLSID del componente:</span><span class="sxs-lookup"><span data-stu-id="57f24-108">Categorizing by container capabilities is accomplished by an additional registry key within the component's CLSID key:</span></span>

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

<span data-ttu-id="57f24-109">Como se muestra en este ejemplo, un componente puede pertenecer a categorías de componentes que indican la funcionalidad admitida, así como a las categorías de componentes que indican la funcionalidad requerida.</span><span class="sxs-lookup"><span data-stu-id="57f24-109">As shown in this example, a component can belong to component categories that indicate supported functionality as well as to component categories that indicate required functionality.</span></span>

<span data-ttu-id="57f24-110">En el ejemplo siguiente, el control de botón es un control OLE genérico que no admite ninguna funcionalidad adicional.</span><span class="sxs-lookup"><span data-stu-id="57f24-110">In the following example, the button control is a generic OLE control that supports no additional functionality.</span></span> <span data-ttu-id="57f24-111">Funcionará en cualquier contenedor de controles OLE.</span><span class="sxs-lookup"><span data-stu-id="57f24-111">It will work in any OLE control container.</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

<span data-ttu-id="57f24-112">Compare el ejemplo anterior con el siguiente ejemplo en el que MyDBControl puede usar Visual Basic enlace de datos si el contenedor lo admite.</span><span class="sxs-lookup"><span data-stu-id="57f24-112">Compare the preceding example with the next example in which the MyDBControl can use Visual Basic data binding if the container supports it.</span></span> <span data-ttu-id="57f24-113">Sin embargo, se ha definido para que funcione en contenedores que no admiten el enlace de datos de Visual Basic (quizás por otra API de base de datos):</span><span class="sxs-lookup"><span data-stu-id="57f24-113">However, it has been defined so that it will work in containers that do not support Visual Basic data binding (perhaps by a different database API):</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

<span data-ttu-id="57f24-114">El control GroupBox es un control Frame simple.</span><span class="sxs-lookup"><span data-stu-id="57f24-114">The GroupBox control is a simple frame control.</span></span> <span data-ttu-id="57f24-115">Se basa en el contenedor que implementa la interfaz [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) y funcionará correctamente solo en estos contenedores:</span><span class="sxs-lookup"><span data-stu-id="57f24-115">It relies on the container implementing the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface and will work correctly only in such containers:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

<span data-ttu-id="57f24-116">Un contenedor que admite Visual Basic controles enlazados a datos pero no admite controles de fotogramas simples especificaría \_ el control CATID y CATID \_ VBDatabound en la interfaz de usuario del control de inserción.</span><span class="sxs-lookup"><span data-stu-id="57f24-116">A container that supports Visual Basic data bound controls but does not support simple frame controls would specify CATID\_Control and CATID\_VBDatabound to the insert control user interface.</span></span> <span data-ttu-id="57f24-117">La lista de controles que se muestran al usuario contiene el \_ botón CLSID y el CLSID \_ MyDBControl.</span><span class="sxs-lookup"><span data-stu-id="57f24-117">The list of controls displayed to the user would contain the CLSID\_Button and CLSID\_MyDBControl.</span></span> <span data-ttu-id="57f24-118">\_No se mostraría el GroupBox de CLSID.</span><span class="sxs-lookup"><span data-stu-id="57f24-118">CLSID\_GroupBox would not be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57f24-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57f24-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57f24-120">Asociar iconos a una categoría</span><span class="sxs-lookup"><span data-stu-id="57f24-120">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="57f24-121">Categorización por funcionalidad de componentes</span><span class="sxs-lookup"><span data-stu-id="57f24-121">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="57f24-122">Clases y asociaciones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="57f24-122">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="57f24-123">Definir categorías de componentes</span><span class="sxs-lookup"><span data-stu-id="57f24-123">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="57f24-124">Administrador de categorías de componentes</span><span class="sxs-lookup"><span data-stu-id="57f24-124">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




