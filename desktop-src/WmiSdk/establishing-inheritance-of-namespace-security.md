---
description: Puede controlar si un espacio de nombres secundario hereda el descriptor de seguridad del espacio de nombres primario.
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: Establecer la herencia de la seguridad del espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e242299b78ede3ff49679305a97823bc022358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707093"
---
# <a name="establishing-inheritance-of-namespace-security"></a><span data-ttu-id="93621-103">Establecer la herencia de la seguridad del espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="93621-103">Establishing Inheritance of Namespace Security</span></span>

<span data-ttu-id="93621-104">Puede controlar si un espacio de nombres secundario hereda el descriptor de seguridad del espacio de nombres primario.</span><span class="sxs-lookup"><span data-stu-id="93621-104">You can control whether a child namespace inherits the security descriptor of the parent namespace.</span></span>

<span data-ttu-id="93621-105">Los espacios de nombres de WMI tienen descriptores de seguridad que controlan quién puede tener acceso al espacio de nombres y a los datos del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="93621-105">WMI namespaces have security descriptors that control who can access the namespace and the data of the namespace.</span></span> <span data-ttu-id="93621-106">Cada descriptor de seguridad tiene una lista de control de acceso discrecional (DACL) y una lista de control de acceso (SACL) de seguridad.</span><span class="sxs-lookup"><span data-stu-id="93621-106">Each security descriptor has a discretionary access control list (DACL) and a security access control list (SACL).</span></span> <span data-ttu-id="93621-107">Estas listas contienen entradas de control de acceso (ACE).</span><span class="sxs-lookup"><span data-stu-id="93621-107">These lists contain access control entries (ACE).</span></span>

<span data-ttu-id="93621-108">Dependiendo de las [**constantes de marca ACE del espacio de nombres**](namespace-ace-flag-constants.md) que se establezcan, los permisos que se aplican a un espacio de nombres pueden ser heredados por todos los espacios de nombres secundarios de ese espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="93621-108">Depending on the [**Namespace ACE Flag Constants**](namespace-ace-flag-constants.md) that are set, permissions that are applied to a namespace may be inherited by all the child namespaces of that namespace.</span></span> <span data-ttu-id="93621-109">Un espacio de nombres secundario hereda el descriptor de seguridad de su espacio de nombres primario cuando se crea el espacio de nombres secundario si el **contenedor hereda la marca \_ \_ ACE** en el descriptor de seguridad del espacio de nombres primario.</span><span class="sxs-lookup"><span data-stu-id="93621-109">A child namespace inherits the security descriptor of its parent namespace when the child namespace is created if the **CONTAINER\_INHERIT\_ACE** flag is in the parent namespace security descriptor.</span></span> <span data-ttu-id="93621-110">Si **Container \_ Inherits \_ ACE no se establece \| \_ propagándose \_ inherit \_ ACE** , solo el espacio de nombres secundario hereda el descriptor de seguridad, no los espacios de nombres terciarios.</span><span class="sxs-lookup"><span data-stu-id="93621-110">If **CONTAINER\_INHERIT\_ACE\|NO\_PROPOGATE\_INHERIT\_ACE** is set, then only the child namespace inherits the security descriptor, not grandchild namespaces.</span></span> <span data-ttu-id="93621-111">Los espacios de nombres secundarios pueden invalidar los permisos de seguridad de su elemento primario llamando a los métodos de la clase [**\_ \_ SystemSecurity**](--systemsecurity.md) para escribir un nuevo descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="93621-111">Child namespaces can override the security permissions of their parent by calling methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class to write a new security descriptor.</span></span> <span data-ttu-id="93621-112">No se puede cambiar la configuración de seguridad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="93621-112">The default security settings cannot be changed.</span></span> <span data-ttu-id="93621-113">Para obtener más información, consulte [configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md). Para obtener más información acerca de las DACL, consulte [listas de Access Control (ACL)](/windows/desktop/SecAuthZ/access-control-lists) y [**constantes de tipo ACE de espacio de nombres**](namespace-ace-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="93621-113">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).For more information about DACLs, see [Access Control Lists (ACL)](/windows/desktop/SecAuthZ/access-control-lists) and [**Namespace ACE Type Constants**](namespace-ace-type-constants.md).</span></span>

<span data-ttu-id="93621-114">Tenga en cuenta que los permisos predeterminados no se pueden cambiar.</span><span class="sxs-lookup"><span data-stu-id="93621-114">Note that the default permissions cannot be changed.</span></span> <span data-ttu-id="93621-115">Además, la configuración de la marca de **\_ DACL \_ protegida con DACL** al establecer el descriptor de seguridad (SD) no se usa para agregar un SD especializado a un espacio de nombres secundario.</span><span class="sxs-lookup"><span data-stu-id="93621-115">Furthermore, setting the **SE\_DACL\_PROTECTED** flag while setting the security descriptor (SD) is not used to add a specialized SD to a child namespace.</span></span> <span data-ttu-id="93621-116">Para invalidar un SD heredado, basta con establecer uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="93621-116">To override an inherited SD, simply set a new one.</span></span> <span data-ttu-id="93621-117">Para heredar la SD a un espacio de nombres secundario, pase la marca **\_ inherit inherit \_ ACE** en el descriptor de seguridad del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="93621-117">To inherit that SD to a child namespace, pass the **CONTAINER\_INHERIT\_ACE** flag in the namespace security descriptor.</span></span> <span data-ttu-id="93621-118">Para heredar solo el elemento secundario, y no los descendientes, pase `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`</span><span class="sxs-lookup"><span data-stu-id="93621-118">To inherit to just the child, and not the descendants, pass `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`</span></span>

<span data-ttu-id="93621-119">.</span><span class="sxs-lookup"><span data-stu-id="93621-119">.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93621-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="93621-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93621-121">Configuración de descriptores de seguridad de espacio</span><span class="sxs-lookup"><span data-stu-id="93621-121">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="93621-122">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="93621-122">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 
