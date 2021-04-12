---
title: Ver contenedores como nodos de hoja
description: Cualquier objeto de Active Directory Domain Services puede ser un contenedor de otros objetos.
ms.assetid: 38300ca5-745a-4640-9723-6052a9843f45
ms.tgt_platform: multiple
keywords:
- Ver contenedores como nodos de hoja
- contenedores AD, ver como nodos de hoja
- AD hoja, ver contenedores como nodos hoja
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1631526ed78132829a7576960a997b13cc232b5f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104358795"
---
# <a name="viewing-containers-as-leaf-nodes"></a><span data-ttu-id="83392-106">Ver contenedores como nodos de hoja</span><span class="sxs-lookup"><span data-stu-id="83392-106">Viewing Containers as Leaf Nodes</span></span>

<span data-ttu-id="83392-107">Cualquier objeto de Active Directory Domain Services puede ser un contenedor de otros objetos.</span><span class="sxs-lookup"><span data-stu-id="83392-107">Any object in Active Directory Domain Services can be a container of other objects.</span></span> <span data-ttu-id="83392-108">Esto puede abarrotar la interfaz de usuario, por lo que es posible declarar que un objeto de una clase específica solo se muestre como una hoja en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="83392-108">This can clutter the user interface, so it is possible to declare that an object of a specific class be only be displayed as a leaf in the user interface.</span></span> <span data-ttu-id="83392-109">El atributo **treatAsLeaf** es un atributo de especificador de presentación de un solo valor que determina si los objetos de esa clase deben mostrarse solo como objetos hoja.</span><span class="sxs-lookup"><span data-stu-id="83392-109">The **treatAsLeaf** attribute is a single-valued display specifier attribute that determines if objects of that class should be only be displayed as leaf objects.</span></span> <span data-ttu-id="83392-110">Este atributo es un valor booleano que, si **es true**, indica que los objetos de la clase deben mostrarse solo como elementos hoja.</span><span class="sxs-lookup"><span data-stu-id="83392-110">This attribute is a Boolean value that, if **TRUE**, indicates that objects of the class should only be displayed as leaf elements.</span></span> <span data-ttu-id="83392-111">Si **es false**, indica que los objetos de la clase se pueden mostrar como un contenedor o una hoja.</span><span class="sxs-lookup"><span data-stu-id="83392-111">If **FALSE**, indicates that objects of the class can be displayed as a container or a leaf.</span></span> <span data-ttu-id="83392-112">Al igual que todos los atributos de especificadores de presentación, el atributo **treatAsLeaf** se establece en función de la configuración regional, por lo que este atributo se puede localizar según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="83392-112">Like all display specifier attributes, the **treatAsLeaf** attribute is set on a per-locale basis, so this attribute can be localized as required.</span></span> <span data-ttu-id="83392-113">Por ejemplo, la **visualización de usuario** para el especificador de pantalla Configuración regional en inglés (0409) tiene el atributo **TreatAsLeaf** establecido en **true** de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="83392-113">For example, the **User-Display** for the English locale (0409) display specifier has the **treatAsLeaf** attribute set to **TRUE** by default.</span></span> <span data-ttu-id="83392-114">Esto hace que la interfaz de usuario muestre todos los objetos de **usuario** como objetos hoja.</span><span class="sxs-lookup"><span data-stu-id="83392-114">This causes the user interface to display all **User** objects as leaf objects.</span></span>

<span data-ttu-id="83392-115">\*\*Para establecer el valor del atributo \*\*treatAsLeaf\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="83392-115">**To set the value of the **treatAsLeaf** attribute**</span></span>

1.  <span data-ttu-id="83392-116">Enlazar al atributo de visualización deseado en la configuración regional deseada.</span><span class="sxs-lookup"><span data-stu-id="83392-116">Bind to the desired display attribute in the desired locale.</span></span> <span data-ttu-id="83392-117">Para obtener más información y un ejemplo de código, vea [contenedor DisplaySpecifiers](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="83392-117">For more information and a code example, see [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>
2.  <span data-ttu-id="83392-118">Use el método [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) para establecer el atributo **treatAsLeaf** en **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="83392-118">Use the [**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put) method to set the **treatAsLeaf** attribute to either **TRUE** or **FALSE**.</span></span>
3.  <span data-ttu-id="83392-119">Para confirmar los cambios en el directorio, llame al método [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="83392-119">To commit changes to the directory, call the [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method.</span></span>

 

 