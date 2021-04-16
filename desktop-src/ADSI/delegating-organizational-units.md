---
title: Delegación de unidades organizativas
description: La compañía de Fabrikam contrata dos administradores, Mike y Paul, para administrar las unidades organizativas este y oeste, respectivamente.
ms.assetid: ecf71ae6-9b6f-4e3c-878a-2c6fd193da33
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9928884c8be19f9668d6f81ed9462f6fb757286f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656187"
---
# <a name="delegating-organizational-units"></a><span data-ttu-id="22311-103">Delegación de unidades organizativas</span><span class="sxs-lookup"><span data-stu-id="22311-103">Delegating Organizational Units</span></span>

<span data-ttu-id="22311-104">La compañía de Fabrikam contrata dos administradores, Mike y Paul, para administrar las unidades organizativas este y oeste, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="22311-104">The Fabrikam company hires two administrators, Mike and Paul, to manage the East and West organizational units, respectively.</span></span> <span data-ttu-id="22311-105">Joe delega sus responsabilidades administrativas en ellos para que puedan crear y eliminar usuarios en sus unidades organizativas respectivas.</span><span class="sxs-lookup"><span data-stu-id="22311-105">Joe delegates his administrative responsibilities to them so that they can create and delete users in their respective organizational units.</span></span>

<span data-ttu-id="22311-106">Antes de ver cómo configurar estas unidades organizativas en Mike y Paul, debe entender cómo configurar el acceso a los objetos en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="22311-106">Before seeing how to set up these organizational units under Mike and Paul, you must understand how to set up access to objects in Active Directory.</span></span> <span data-ttu-id="22311-107">Cada objeto de Active Directory tiene un descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="22311-107">Each object in Active Directory has a security descriptor.</span></span> <span data-ttu-id="22311-108">Con el descriptor de seguridad, puede modificar los permisos en el objeto, propagar los permisos, habilitar la auditoría, etc.</span><span class="sxs-lookup"><span data-stu-id="22311-108">With the security descriptor, you can modify permissions on the object, propagate permissions, enable auditing, and so on.</span></span> <span data-ttu-id="22311-109">El propio descriptor de seguridad tiene dos listas de control de acceso (ACL): una ACL discrecional (DACL) y una ACL del sistema (SACL).</span><span class="sxs-lookup"><span data-stu-id="22311-109">The security descriptor itself has two access control lists (ACLs): a discretionary ACL (DACL) and a system ACL (SACL).</span></span> <span data-ttu-id="22311-110">Cada ACL puede contener entradas de control de acceso (ACE).</span><span class="sxs-lookup"><span data-stu-id="22311-110">Each ACL can contain access control entries (ACEs).</span></span> <span data-ttu-id="22311-111">Con una ACE, puede establecer el acceso permitido o denegado en un objeto.</span><span class="sxs-lookup"><span data-stu-id="22311-111">With an ACE, you can set allowed or denied access on an object.</span></span> <span data-ttu-id="22311-112">Además, puede especificar acciones específicas para permitir o denegar.</span><span class="sxs-lookup"><span data-stu-id="22311-112">In addition, you can specify specific actions to allow or deny.</span></span> <span data-ttu-id="22311-113">Algunos ejemplos de acciones son crear secundaria, eliminar secundaria, leer propiedad y escribir propiedad.</span><span class="sxs-lookup"><span data-stu-id="22311-113">Examples of actions include Create Child, Delete Child, Read Property, and Write Property.</span></span> <span data-ttu-id="22311-114">Estos derechos se especifican con [**AccessMask**](iadsaccesscontrolentry-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="22311-114">These rights are specified with the [**AccessMask**](iadsaccesscontrolentry-property-methods.md).</span></span>

<span data-ttu-id="22311-115">A continuación, puede especificar las clases o los atributos a los que está asociada esta ACE.</span><span class="sxs-lookup"><span data-stu-id="22311-115">Next, you may specify the classes or attributes to which this ACE is associated.</span></span> <span data-ttu-id="22311-116">En el ejemplo de Fabrikam siguiente, Joe selecciona la clase de usuario para que cada administrador pueda agregar usuarios al sistema.</span><span class="sxs-lookup"><span data-stu-id="22311-116">In the Fabrikam example that follows, Joe picks the user class so that each administrator can add users to the system.</span></span> <span data-ttu-id="22311-117">A continuación, debe responder a la pregunta: "¿quién será el beneficiario de esta ACE?"</span><span class="sxs-lookup"><span data-stu-id="22311-117">Next, you must answer the question: "Who will be the beneficiary of this ACE?"</span></span> <span data-ttu-id="22311-118">Joe especificará Mike.</span><span class="sxs-lookup"><span data-stu-id="22311-118">Joe will specify Mike.</span></span>

<span data-ttu-id="22311-119">Por último, puede establecer el comportamiento de la herencia ACE; por ejemplo, se pueden especificar ACE para propagar hacia abajo en la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="22311-119">Finally, you can set the ACE inheritance behavior—for example, ACEs can be specified to propagate down the hierarchy.</span></span> <span data-ttu-id="22311-120">En Resumen, el ejemplo anterior hará que Mike sea capaz de crear y eliminar objetos de usuario en la unidad organizativa de ventas del este.</span><span class="sxs-lookup"><span data-stu-id="22311-120">In summary, the previous example will result in Mike being able to create and delete user objects under the East Sales organizational unit.</span></span>

<span data-ttu-id="22311-121">Joe usa el siguiente ejemplo de código para configurar las ACE y las ACL en la unidad organizativa East.</span><span class="sxs-lookup"><span data-stu-id="22311-121">Joe uses the following code example to set up the ACEs and ACLs on the East organizational unit.</span></span>


```VB
Set ou = GetObject("LDAP://OU=East, OU=Sales, DC=Fabrikam,DC=COM")
Set sec = ou.Get("ntSecurityDescriptor")
Set acl = sec.DiscretionaryAcl

Set ace = CreateObject("AccessControlEntry") 
' You can also use Set ace = new ADsAccessControlEntry.

' Grant access to the object.
ace.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT 

' Create and delete child objects.
ace.AccessMask = ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD 
' Create the user object with the user schema IDGUID.
ace.ObjectType = "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 
' Propagate the ACE down.  
ace.AceFlags = ADS_ACEFLAG_INHERIT_ACE
' Provide an option that notifies that the objectType is filled.
ace.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT 
' Show the beneficiary of this ACE.
ace.Trustee = "FABRIKAM\Mike" 
acl.AddAce ace

sec.DiscretionaryAcl = acl
ou.Put "ntSecurityDescriptor", Array(sec)
' Use SetInfo to commit the data to Active Directory.
ou.SetInfo 

' Release the objects.
Set ace = Nothing
Set acl  = Nothing
Set sec = Nothing
```



<span data-ttu-id="22311-122">En la ilustración siguiente se muestra el Active Directory menú **crear nueva vista** después de que se ejecute el código.</span><span class="sxs-lookup"><span data-stu-id="22311-122">The following figure shows the Active Directory **Create New View** menu after the code runs.</span></span> <span data-ttu-id="22311-123">Cuando Joe, el administrador inicia sesión, ve varias clases que puede crear.</span><span class="sxs-lookup"><span data-stu-id="22311-123">When Joe, the administrator, logs on, he sees several classes that he can create.</span></span> <span data-ttu-id="22311-124">Sin embargo, cuando Mike inicia sesión, solo puede crear objetos de usuario.</span><span class="sxs-lookup"><span data-stu-id="22311-124">However, when Mike logs on, he is able only to create user objects.</span></span>

![crear nuevo menú de opciones de vista](images/adadsi5.png)

<span data-ttu-id="22311-126">Para obtener más información, vea [modelo de seguridad ADSI](adsi-security-model.md).</span><span class="sxs-lookup"><span data-stu-id="22311-126">For more information, see [ADSI Security Model](adsi-security-model.md).</span></span>

 

 




