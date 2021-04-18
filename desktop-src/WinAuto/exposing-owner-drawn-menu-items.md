---
title: Exponer Owner-Drawn elementos de menú
description: Exponer Owner-Drawn elementos de menú
ms.assetid: 93b51cbb-b7b4-4a38-ba69-d6345a269944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79668115cedd5fb6b8c20b0d4df361d6d1d800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532302"
---
# <a name="exposing-owner-drawn-menu-items"></a><span data-ttu-id="eb6db-103">Exponer Owner-Drawn elementos de menú</span><span class="sxs-lookup"><span data-stu-id="eb6db-103">Exposing Owner-Drawn Menu Items</span></span>

<span data-ttu-id="eb6db-104">Los desarrolladores de aplicaciones pueden usar la estructura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) para exponer los nombres de los elementos de menú dibujados por el propietario.</span><span class="sxs-lookup"><span data-stu-id="eb6db-104">Application developers can use the [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure to expose the names of owner-drawn menu items.</span></span> <span data-ttu-id="eb6db-105">Al asociar esta estructura con los datos del elemento de menú dibujado por el propietario, no es necesario exponer los elementos de menú con [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="eb6db-105">By associating this structure with the owner-drawn menu item data, you do not need to expose the menu items with [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span>

<span data-ttu-id="eb6db-106">Al crear un menú dibujado por el propietario, defina una clase o estructura para los datos de elemento de menú dibujados por el propietario y cree instancias de esta clase para cada elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="eb6db-106">When creating an owner-drawn menu, define a class or structure for the owner-drawn menu item data and create instances of this class for each menu item.</span></span> <span data-ttu-id="eb6db-107">Pase un puntero a los datos del elemento al agregar elementos al menú.</span><span class="sxs-lookup"><span data-stu-id="eb6db-107">Pass in a pointer to the item data when adding items to the menu.</span></span>

<span data-ttu-id="eb6db-108">Para exponer los nombres de los elementos de menú, la estructura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) debe ser el primer miembro de la estructura que define los datos de los elementos específicos de la aplicación, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="eb6db-108">To expose the names of the menu items, the [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure must be the first member of the structure that defines the application-specific item data, as shown in the following example:</span></span>


```C++
// Application-specific owner-drawn menu info struct. Owner-drawn data 
// is a pointer to one of these.
struct MenuEntry
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //   separator item 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //   for separator 
};
```



<span data-ttu-id="eb6db-109">La estructura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) no puede ser un miembro de una clase que contenga funciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="eb6db-109">The [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure cannot be a member in a class that contains virtual functions.</span></span> <span data-ttu-id="eb6db-110">Cuando se compila el código, el primer miembro de la clase siempre es un puntero generado por el compilador a una tabla de las funciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="eb6db-110">When the code is compiled, the first member of the class is always a compiler-generated pointer to a table of the virtual functions.</span></span> <span data-ttu-id="eb6db-111">Para solucionar este problema, cree una estructura de datos de elemento que contenga **MSAAMENUINFO** como primer miembro.</span><span class="sxs-lookup"><span data-stu-id="eb6db-111">To work around this problem, create an item data structure that contains **MSAAMENUINFO** as the first member.</span></span> <span data-ttu-id="eb6db-112">El segundo miembro es un puntero a una instancia de la clase que define los datos dibujados por el propietario.</span><span class="sxs-lookup"><span data-stu-id="eb6db-112">The second member is a pointer to an instance of the class that defines the owner-drawn data.</span></span> <span data-ttu-id="eb6db-113">En el ejemplo siguiente se muestra esta técnica.</span><span class="sxs-lookup"><span data-stu-id="eb6db-113">The following example demonstrates this technique.</span></span>


```C++
// Application-defined class that contains the owner-drawn data and 
//  virtual functions that operate on that data.  
class MenuEntry
{
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //  separator item. 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //  separator item 
    virtual void m_AnimateIcon();  
    virtual void m_ChangeIconColor();
}

// Application-defined struct that contains MSAAMENUINFO as first 
//  member. Second member points to owner-drawn data. 
struct MenuInfo
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    MenuEntry *pMenuData;      // Points to the owner-drawn data 
}
```



<span data-ttu-id="eb6db-114">Al agregar elementos al menú, pase un puntero a una instancia de la estructura que contiene [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) para exponer los nombres de los elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="eb6db-114">When adding items to the menu, pass a pointer to an instance of the structure that contains [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) to expose the names of the menu items.</span></span>

 

 




