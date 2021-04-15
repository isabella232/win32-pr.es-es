---
title: Creación de nuevos usuarios en la unidad organizativa
description: Tomás Adams se contrató en la organización de ventas de fabrikam. Su informe directo es Patrick Hines.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Creación de nuevos usuarios en la unidad organizativa ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45f9dc91f1c36493a4ae8e1c9bb1a69268c9987
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486566"
---
# <a name="creating-new-users-in-the-organizational-unit"></a><span data-ttu-id="536c5-105">Creación de nuevos usuarios en la unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="536c5-105">Creating New Users in the Organizational Unit</span></span>

<span data-ttu-id="536c5-106">Tomás Adams se contrató en la organización de ventas de fabrikam.</span><span class="sxs-lookup"><span data-stu-id="536c5-106">Terry Adams was hired into the Fabrikam Sales organization.</span></span> <span data-ttu-id="536c5-107">Su informe directo es Patrick Hines.</span><span class="sxs-lookup"><span data-stu-id="536c5-107">His direct report is Patrick Hines.</span></span>

<span data-ttu-id="536c5-108">Como se muestra en el ejemplo de código siguiente, Joe Andreshak, el administrador de la empresa, creará una nueva cuenta para él.</span><span class="sxs-lookup"><span data-stu-id="536c5-108">As shown in the following code example, Joe Andreshak, the enterprise administrator, will create a new account for him.</span></span>


```VB
Dim salesOU as IADsContainer
Set salesOU = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set usr = salesOU.Create("user", "CN=Terry Adams")
usr.Put "sAMAccountName", "terryadams"
usr.Put "userPrincipalName", "terryadams@fabrikam.com" 
usr.Put "title" "Marketing Manager"
usr.SetInfo

usr.SetPassword "seahorse"
usr.AccountDisabled = False
usr.SetInfo
```



<span data-ttu-id="536c5-109">Al crear un nuevo usuario, debe especificar un **samAccountName**.</span><span class="sxs-lookup"><span data-stu-id="536c5-109">When creating a new user, you must specify a **sAMAccountName**.</span></span> <span data-ttu-id="536c5-110">Este es un atributo obligatorio para la clase User.</span><span class="sxs-lookup"><span data-stu-id="536c5-110">This is a mandatory attribute for the user class.</span></span> <span data-ttu-id="536c5-111">Antes de que se pueda crear una instancia de un objeto, se deben establecer todos los atributos obligatorios.</span><span class="sxs-lookup"><span data-stu-id="536c5-111">Before an instance of an object can be created, all mandatory attributes must be set.</span></span> <span data-ttu-id="536c5-112">El **samAccountName** se generará automáticamente si no se especifica uno para un nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="536c5-112">The **sAMAccountName** will automatically be generated if one is not specified for a new user.</span></span>

<span data-ttu-id="536c5-113">Al crear un nuevo usuario, todos los atributos necesarios se deben establecer en la memoria caché local antes de que se llame al método [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="536c5-113">When creating a new user, all of the required attributes must be set in the local cache before the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span>

<span data-ttu-id="536c5-114">Joe, como administrador, puede asignar la contraseña de Tomás mediante el método [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) .</span><span class="sxs-lookup"><span data-stu-id="536c5-114">Joe, as an administrator, can assign Terry's password using the [**IADsUser.SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) method.</span></span> <span data-ttu-id="536c5-115">El método **IADsUser. SetPassword** no funcionará hasta que se haya llamado al método [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="536c5-115">The **IADsUser.SetPassword** method will not work until the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method has been called.</span></span>

<span data-ttu-id="536c5-116">A continuación, Joe habilita la cuenta de usuario estableciendo la propiedad [**IADsUser. AccountDisabled**](iadsuser-property-methods.md) en **false**.</span><span class="sxs-lookup"><span data-stu-id="536c5-116">Then, Joe enables the user account by setting the [**IADsUser.AccountDisabled**](iadsuser-property-methods.md) property to **FALSE**.</span></span>

<span data-ttu-id="536c5-117">En el ejemplo de código siguiente se muestra cómo establecer Tomás como administrador de Patrick.</span><span class="sxs-lookup"><span data-stu-id="536c5-117">The following code example shows how to set Terry as Patrick's manager.</span></span>


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



<span data-ttu-id="536c5-118">Es posible que se pregunte qué sucede si Terry cambia su nombre, se desplaza a otra organización o deja la empresa.</span><span class="sxs-lookup"><span data-stu-id="536c5-118">You may wonder what happens if Terry changes his name, moves to a different organization, or leaves the company.</span></span> <span data-ttu-id="536c5-119">¿Quién mantiene este vínculo de informe de administrador-directo?</span><span class="sxs-lookup"><span data-stu-id="536c5-119">Who maintains this manager-direct report link?</span></span> <span data-ttu-id="536c5-120">Para obtener más información y la solución a este problema, vea [reorganización](reorganization.md).</span><span class="sxs-lookup"><span data-stu-id="536c5-120">For more information, and the solution to this problem, see [Reorganization](reorganization.md).</span></span> <span data-ttu-id="536c5-121">Dado que el esquema de Active Directory es extensible, puede modelar los objetos para que incluyan relaciones similares de estilo de informe directo entre administradores.</span><span class="sxs-lookup"><span data-stu-id="536c5-121">Because the Active Directory schema is extensible, you can model your objects to include similar manager-direct report style relationships.</span></span>

<span data-ttu-id="536c5-122">Antes de pasar a la tarea siguiente, consulte un ejemplo de código que muestra cómo Joe vería los informes directos de Terry.</span><span class="sxs-lookup"><span data-stu-id="536c5-122">Before going on to the next task, look at a code example that shows how Joe would view Terry's direct reports.</span></span>


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



<span data-ttu-id="536c5-123">En este ejemplo de código, Patrick se mostrará como el informe directo de Terry, aunque el atributo **directReports** no se haya modificado nunca.</span><span class="sxs-lookup"><span data-stu-id="536c5-123">In this code example, Patrick will display as Terry's direct report, even though the **directReports** attribute was never modified.</span></span> <span data-ttu-id="536c5-124">Active Directory lo hace automáticamente.</span><span class="sxs-lookup"><span data-stu-id="536c5-124">Active Directory does this automatically.</span></span>

<span data-ttu-id="536c5-125">En el mundo del directorio, un atributo puede tener uno o varios valores.</span><span class="sxs-lookup"><span data-stu-id="536c5-125">In the directory world, an attribute can have single or multiple values.</span></span> <span data-ttu-id="536c5-126">Dado que **directReports** tiene varios valores, puede obtener esta información examinando el esquema, es más fácil usar el método [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) , que devuelve una matriz de valores independientemente de si se devuelve uno o varios valores.</span><span class="sxs-lookup"><span data-stu-id="536c5-126">Because **directReports** has multiple values, you can get this information by looking at the schema, it is easier to use the [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method, which returns an array of values regardless of whether single or multiple values are returned.</span></span>

<span data-ttu-id="536c5-127">El complemento usuarios y equipos de Active Directory permite ver informes directos y relaciones de administrador en la página de propiedades del usuario.</span><span class="sxs-lookup"><span data-stu-id="536c5-127">The Active Directory Users and Computers snap-in lets you view direct reports and manager relationships on the user's property page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="536c5-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="536c5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="536c5-129">Agregar usuarios a un grupo</span><span class="sxs-lookup"><span data-stu-id="536c5-129">Adding Users to a Group</span></span>](adding-users-to-a-group.md)
</dt> </dl>

 

 




