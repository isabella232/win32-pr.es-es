---
description: Asignar roles a componentes, interfaces o métodos
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: Asignar roles a componentes, interfaces o métodos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5efb66c9de865cbfcdc6e9cb047af92c95f6bc0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423411"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a><span data-ttu-id="87b35-103">Asignar roles a componentes, interfaces o métodos</span><span class="sxs-lookup"><span data-stu-id="87b35-103">Assigning Roles to Components, Interfaces, or Methods</span></span>

<span data-ttu-id="87b35-104">Puede asignar explícitamente un rol a cualquier elemento de una aplicación COM+ que esté visible a través de la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="87b35-104">You can explicitly assign a role to any item within a COM+ application that is visible through the Component Services administrative tool.</span></span> <span data-ttu-id="87b35-105">Esto garantiza que todos los usuarios que sean miembros del rol tendrán acceso a ese elemento y a cualquier otro elemento que contenga.</span><span class="sxs-lookup"><span data-stu-id="87b35-105">Doing so ensures that any users that are members of the role will be permitted access to that item and any other items that it contains.</span></span> <span data-ttu-id="87b35-106">Por ejemplo, si asigna el rol "lectores" a un componente, se permite que cualquier miembro de "lectores" tenga acceso a ese componente y a cualquier interfaz y método que exponga.</span><span class="sxs-lookup"><span data-stu-id="87b35-106">For example, if you assign the role "Readers" to a component, any member of "Readers" is allowed access to that component and any interfaces and methods it exposes.</span></span> <span data-ttu-id="87b35-107">Los "lectores" se mostrarán como un rol heredado para cualquiera de esas interfaces y métodos.</span><span class="sxs-lookup"><span data-stu-id="87b35-107">"Readers" will show up as an Inherited role for any of those interfaces and methods.</span></span>

<span data-ttu-id="87b35-108">Solo se puede tener acceso a un método a los llamadores si se le asigna un rol, ya sea asignando explícitamente el rol directamente al método o asignando un rol a la interfaz del método o al componente del método, en cuyo caso el rol lo heredará el método.</span><span class="sxs-lookup"><span data-stu-id="87b35-108">A method is accessible to callers only if you assign a role to it, either by explicitly assigning the role directly to the method or by assigning a role to the method's interface or the method's component, in which case the role will be inherited by the method.</span></span> <span data-ttu-id="87b35-109">Si no se asigna ningún rol y las comprobaciones de acceso están habilitadas, se producirá un error en todas las llamadas al método.</span><span class="sxs-lookup"><span data-stu-id="87b35-109">If no role is assigned and if access checks are enabled, all calls to the method will fail.</span></span>

<span data-ttu-id="87b35-110">Antes de poder asignar un rol, debe [definirlo](defining-roles-for-an-application.md) para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="87b35-110">Before you can assign a role, you must [define](defining-roles-for-an-application.md) it for the application.</span></span> <span data-ttu-id="87b35-111">Todos los roles definidos para la aplicación aparecerán en los **roles establecidos explícitamente para la ventana elementos seleccionados** en la pestaña **seguridad** para todos los componentes, métodos e interfaces dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="87b35-111">All roles defined for the application will appear in the **Roles explicitly set for selected item(s)** window on the **Security** tab for any components, methods, and interfaces within the application.</span></span>

<span data-ttu-id="87b35-112">**Para asignar roles a un componente, método o interfaz**</span><span class="sxs-lookup"><span data-stu-id="87b35-112">**To assign roles to a component, method, or interface**</span></span>

1.  <span data-ttu-id="87b35-113">En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ para la que se ha definido el rol.</span><span class="sxs-lookup"><span data-stu-id="87b35-113">In the console tree of the Component Services administrative tool, locate the COM+ application for which the role has been defined.</span></span> <span data-ttu-id="87b35-114">Expanda el árbol para ver los componentes, las interfaces o los métodos de la aplicación, en función de la asignación de la función.</span><span class="sxs-lookup"><span data-stu-id="87b35-114">Expand the tree to view the application's components, interfaces, or methods, depending on what you are assigning the role to.</span></span>

2.  <span data-ttu-id="87b35-115">Haga clic con el botón secundario en el elemento al que desea asignar el rol y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="87b35-115">Right-click the item to which you want to assign the role, and then click **Properties**.</span></span>

3.  <span data-ttu-id="87b35-116">En el cuadro de diálogo Propiedades, haga clic en la pestaña **seguridad** .</span><span class="sxs-lookup"><span data-stu-id="87b35-116">In the properties dialog box, click the **Security** tab.</span></span>

4.  <span data-ttu-id="87b35-117">En el cuadro los **roles se establecen explícitamente para los elementos seleccionados** , seleccione los roles que desea asignar al elemento.</span><span class="sxs-lookup"><span data-stu-id="87b35-117">In the **Roles explicitly set for selected item(s)** box, select the roles that you want to assign to the item.</span></span>

5.  <span data-ttu-id="87b35-118">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="87b35-118">Click **OK**.</span></span>

<span data-ttu-id="87b35-119">Cualquier rol que se haya establecido explícitamente para un elemento será heredado por los elementos de nivel inferior que contenga y se mostrará en la ventana de **roles heredados por** los elementos seleccionados para esos elementos.</span><span class="sxs-lookup"><span data-stu-id="87b35-119">Any roles that you have explicitly set for an item will be inherited by any lower-level items it contains and will show up in the **Roles inherited by selected item(s)** window for those items.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87b35-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="87b35-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87b35-121">Configuración de la seguridad de Role-Based</span><span class="sxs-lookup"><span data-stu-id="87b35-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="87b35-122">Definición de roles para una aplicación</span><span class="sxs-lookup"><span data-stu-id="87b35-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="87b35-123">Habilitación de las comprobaciones de acceso para una aplicación</span><span class="sxs-lookup"><span data-stu-id="87b35-123">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="87b35-124">Habilitar comprobaciones de acceso en el nivel de componente</span><span class="sxs-lookup"><span data-stu-id="87b35-124">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="87b35-125">Establecimiento de un nivel de seguridad para las comprobaciones de acceso</span><span class="sxs-lookup"><span data-stu-id="87b35-125">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



