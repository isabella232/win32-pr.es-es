---
title: Creación de un nuevo grupo
description: Joe Worden, el administrador de la empresa, debe crear un nuevo grupo.
ms.assetid: a1bea695-d43f-47e6-af74-ba5abb0116a2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a4f46d595aa892ac75aa67d14bbc0356122271
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995635"
---
# <a name="creating-a-new-group"></a><span data-ttu-id="fc234-103">Creación de un nuevo grupo</span><span class="sxs-lookup"><span data-stu-id="fc234-103">Creating a New Group</span></span>

<span data-ttu-id="fc234-104">Joe Worden, el administrador de la empresa, debe crear un nuevo grupo.</span><span class="sxs-lookup"><span data-stu-id="fc234-104">Joe Worden, the enterprise administrator, must create a new group.</span></span> <span data-ttu-id="fc234-105">Le gustaría proteger algunos recursos, como archivos, Active Directory objetos u otros objetos, en función de la pertenencia de este grupo.</span><span class="sxs-lookup"><span data-stu-id="fc234-105">He would like to secure some resources, such as file, Active Directory objects, or other objects, based on the membership of this group.</span></span> <span data-ttu-id="fc234-106">En el ejemplo de código siguiente se muestra cómo crear un nuevo grupo.</span><span class="sxs-lookup"><span data-stu-id="fc234-106">The following code example shows how to create a new group.</span></span>


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



<span data-ttu-id="fc234-107">Este grupo, administración, se creará en la unidad organizativa ventas.</span><span class="sxs-lookup"><span data-stu-id="fc234-107">This group, Management, will be created in the Sales organizational unit.</span></span> <span data-ttu-id="fc234-108">En primer lugar, Joe debe crear un objeto ADSI para la unidad organizativa sales.</span><span class="sxs-lookup"><span data-stu-id="fc234-108">First, Joe must create an ADSI object for the Sales organizational unit.</span></span> <span data-ttu-id="fc234-109">En segundo lugar, debe establecer el atributo [**samAccountName**](/windows/desktop/AD/group-objects) en este objeto, ya que es un atributo obligatorio por compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="fc234-109">Second, he must set the [**samAccountName**](/windows/desktop/AD/group-objects) attribute on this object, because it is a mandatory attribute for backward compatibility.</span></span> <span data-ttu-id="fc234-110">En este ejemplo, cuando se establece **samAccountName** , las herramientas de Windows NT 4,0 como User Manager ven el atributo como **MGMT** en lugar de **Management**.</span><span class="sxs-lookup"><span data-stu-id="fc234-110">For this example, when **samAccountName** is set, Windows NT 4.0 tools such as User Manager see the attribute as **mgmt** instead of **Management**.</span></span>

<span data-ttu-id="fc234-111">En tercer lugar, Joe debe especificar el tipo de grupo.</span><span class="sxs-lookup"><span data-stu-id="fc234-111">Third, Joe must specify the type of group.</span></span> <span data-ttu-id="fc234-112">En un dominio de Windows 2000, hay tres tipos de grupos: global, local de dominio y universal.</span><span class="sxs-lookup"><span data-stu-id="fc234-112">In a Windows 2000 domain, there are three types of groups: Global, Domain Local, and Universal.</span></span> <span data-ttu-id="fc234-113">Además, el grupo lleva su característica de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fc234-113">In addition, the group carries its security characteristic.</span></span> <span data-ttu-id="fc234-114">Un grupo puede ser un grupo con seguridad habilitada o no protegido.</span><span class="sxs-lookup"><span data-stu-id="fc234-114">A group can be either a security-enabled or a non-secured group.</span></span> <span data-ttu-id="fc234-115">Esencialmente, los grupos con seguridad habilitada son aquellos a los que se puede conceder o denegar derechos de acceso a los recursos, de manera similar a un usuario.</span><span class="sxs-lookup"><span data-stu-id="fc234-115">Essentially, security-enabled groups are those that can be granted or denied access rights to resources, similar to a user.</span></span> <span data-ttu-id="fc234-116">La concesión de acceso a un grupo a un recurso compartido de archivos, por ejemplo, implica que todos los miembros del grupo pueden tener acceso al recurso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="fc234-116">Granting a group access to a file share, for example, implies that all members of the group can access the file share.</span></span> <span data-ttu-id="fc234-117">Las listas de distribución no se pueden usar de forma similar; por ejemplo, no se puede conceder a una lista de distribución el derecho a tener acceso a un recurso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="fc234-117">Distribution lists cannot be used in a similar manner—you cannot, for example, grant a distribution list the right to access a file share.</span></span> <span data-ttu-id="fc234-118">Durante la actualización, los grupos de Windows NT 4,0 se migran como grupos con seguridad habilitada.</span><span class="sxs-lookup"><span data-stu-id="fc234-118">During the upgrade, Windows NT 4.0 groups are migrated as security-enabled groups.</span></span> <span data-ttu-id="fc234-119">Los grupos no seguros en Active Directory son similares a las listas de distribución de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fc234-119">Non-secured groups in Active Directory are similar to distribution lists in Exchange.</span></span> <span data-ttu-id="fc234-120">Por lo tanto, la creación de grupos o listas de distribución es una operación similar en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="fc234-120">Hence, creating groups or distribution lists are similar operations in Windows 2000.</span></span> <span data-ttu-id="fc234-121">En el modo nativo de Windows 2000 (el modo nativo significa que todos los controladores de dominio de un dominio son equipos que ejecutan Windows 2000 Server), los grupos se pueden anidar en cualquier nivel.</span><span class="sxs-lookup"><span data-stu-id="fc234-121">In the Windows 2000 native mode (native mode means that all domain controllers in a domain are computers running Windows 2000 Server), the groups can be nested to any level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc234-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc234-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc234-123">Enumerar objetos</span><span class="sxs-lookup"><span data-stu-id="fc234-123">Enumerating Objects</span></span>](enumerating-objects.md)
</dt> </dl>

 

 