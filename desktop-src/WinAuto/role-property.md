---
title: Role (propiedad)
description: La propiedad role describe el elemento de la interfaz de usuario de un objeto. Todos los objetos admiten la propiedad role.
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f2b285d9242542f83c6b4478df93e888a7a23cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704588"
---
# <a name="role-property"></a><span data-ttu-id="857f5-104">Role (propiedad)</span><span class="sxs-lookup"><span data-stu-id="857f5-104">Role Property</span></span>

<span data-ttu-id="857f5-105">La propiedad **role** describe el elemento de la interfaz de usuario de un objeto.</span><span class="sxs-lookup"><span data-stu-id="857f5-105">The **Role** property describes an object's user interface element.</span></span> <span data-ttu-id="857f5-106">Todos los objetos admiten la propiedad **role** .</span><span class="sxs-lookup"><span data-stu-id="857f5-106">All objects support the **Role** property.</span></span>

<span data-ttu-id="857f5-107">En muchos casos, el rol del objeto es obvio.</span><span class="sxs-lookup"><span data-stu-id="857f5-107">In many cases, the object's role is obvious.</span></span> <span data-ttu-id="857f5-108">Por ejemplo, las ventanas tienen el rol de [**\_ \_ ventana del sistema de rol**](object-roles.md) y los botones de la función de pulsador del [**\_ sistema \_ de rol**](object-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="857f5-108">For example, windows have the [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) role and push buttons have the [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md) role.</span></span>

<span data-ttu-id="857f5-109">La propiedad **role** se recupera llamando a [**IAccessible:: get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).</span><span class="sxs-lookup"><span data-stu-id="857f5-109">The **Role** property is retrieved by calling [**IAccessible::get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).</span></span>

## <a name="identifying-an-objects-role"></a><span data-ttu-id="857f5-110">Identificar el rol de un objeto</span><span class="sxs-lookup"><span data-stu-id="857f5-110">Identifying an Object's Role</span></span>

<span data-ttu-id="857f5-111">Microsoft Active Accessibility proporciona [constantes de rol](object-roles.md), definidas en oleacc. h, que identifican roles de objeto comunes.</span><span class="sxs-lookup"><span data-stu-id="857f5-111">Microsoft Active Accessibility provides [role constants](object-roles.md), defined in oleacc.h, that identify common object roles.</span></span> <span data-ttu-id="857f5-112">Se recomienda que los desarrolladores de servidores utilicen estos valores de roles predefinidos.</span><span class="sxs-lookup"><span data-stu-id="857f5-112">It is recommended that server developers use these predefined role values.</span></span> <span data-ttu-id="857f5-113">Si se devuelve una constante de rol predefinida, los clientes utilizan la función [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) para recuperar una cadena localizada que describe el rol.</span><span class="sxs-lookup"><span data-stu-id="857f5-113">If a predefined role constant is returned, clients use the [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) function to retrieve a localized string that describes the role.</span></span>

<span data-ttu-id="857f5-114">En el caso de los controles de animación, como el control de animación que se muestra al copiar archivos, use la [**\_ \_ animación del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="857f5-114">For animation controls, such as the animation control displayed when copying files, use [**ROLE\_SYSTEM\_ANIMATION**](object-roles.md).</span></span> <span data-ttu-id="857f5-115">Los gráficos que se animan ocasionalmente se describen como un [**\_ \_ gráfico de sistema de roles**](object-roles.md) con la propiedad [**State**](state-property.md) establecida en [**Estado de \_ sistema \_ animado**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="857f5-115">Graphics that are occasionally animated are described as [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md) with the [**State**](state-property.md) property set to [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md).</span></span>

<span data-ttu-id="857f5-116">Tenga en cuenta que algunos roles no son fáciles de describir.</span><span class="sxs-lookup"><span data-stu-id="857f5-116">Note that some roles are not easy to describe.</span></span> <span data-ttu-id="857f5-117">Por ejemplo, la vista de iconos grandes de una carpeta permite la organización arbitraria de iconos, por lo que su rol podría describirse como [**\_ \_ agrupación del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="857f5-117">For example, a folder's large-icon view allows arbitrary arrangement of icons, so its role could be described as [**ROLE\_SYSTEM\_GROUPING**](object-roles.md).</span></span> <span data-ttu-id="857f5-118">O bien, un control que proporciona elementos en filas y columnas fijas podría tener el rol de [**\_ \_ tabla del sistema de rol**](object-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="857f5-118">Or, a control that provides items in fixed rows and columns could have the [**ROLE\_SYSTEM\_TABLE**](object-roles.md) role.</span></span> <span data-ttu-id="857f5-119">Puesto que un rol se usa para comunicar el modelo de uso a un usuario final, es importante usar el rol adecuado.</span><span class="sxs-lookup"><span data-stu-id="857f5-119">Since a role is used to communicate the use model to an end user, it is important to use the appropriate role.</span></span> <span data-ttu-id="857f5-120">Por ejemplo, si el control actúa como un botón, use [**\_ \_ PUSHBUTTON del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="857f5-120">For example, if your control acts like a button, then use [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md).</span></span>

 

 




