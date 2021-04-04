---
title: Controlar el acceso a objetos en Active Directory Domain Services
description: Cada Active Directory objeto de servicio de directorio está protegido por la seguridad de Windows 2000.
ms.assetid: 0821069d-76bd-49cb-a617-8446d26e61d9
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, uso, seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cac744ef63fa95c45d5af535f5155378d479fdb
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/04/2019
ms.locfileid: "104077168"
---
# <a name="controlling-object-access-in-active-directory-domain-services"></a><span data-ttu-id="77cdb-104">Controlar el acceso a objetos en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="77cdb-104">Controlling object access in Active Directory Domain Services</span></span>

<span data-ttu-id="77cdb-105">Cada Active Directory objeto de servicio de directorio está protegido por la seguridad de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="77cdb-105">Each Active Directory directory service object is protected by Windows 2000 security.</span></span> <span data-ttu-id="77cdb-106">Esta protección de seguridad controla las operaciones que cada entidad de seguridad puede realizar en el directorio.</span><span class="sxs-lookup"><span data-stu-id="77cdb-106">This security protection controls the operations that each security principal can perform in the directory.</span></span> <span data-ttu-id="77cdb-107">En las secciones siguientes se describe cómo una aplicación habilitada para directorio puede usar las características de control de acceso en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="77cdb-107">The following sections describe how a directory-enabled application can use the access control features in Active Directory.</span></span>

-   [<span data-ttu-id="77cdb-108">Cómo funciona Access Control en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="77cdb-108">How Access Control Works in Active Directory Domain Services</span></span>](how-access-control-works-in-active-directory-domain-services.md)
-   [<span data-ttu-id="77cdb-109">Cómo afecta el control de acceso a las operaciones de lectura, escritura, creación y eliminación de objetos.</span><span class="sxs-lookup"><span data-stu-id="77cdb-109">How access control affects read operations, write operation, object creation and deletion.</span></span>](how-security-affects-operations-in-active-directory-domain-services.md)
-   [<span data-ttu-id="77cdb-110">Usar las interfaces IADs y IDirectoryObject para trabajar con el descriptor de seguridad de un objeto</span><span class="sxs-lookup"><span data-stu-id="77cdb-110">Using the IADs and IDirectoryObject interfaces to work with an object's security descriptor</span></span>](apis-for-working-with-security-descriptors.md)
-   [<span data-ttu-id="77cdb-111">Modificar los permisos de acceso de un objeto</span><span class="sxs-lookup"><span data-stu-id="77cdb-111">Modifying the access permissions on an object</span></span>](setting-access-rights-on-an-object.md)
-   [<span data-ttu-id="77cdb-112">Cómo se establecen los descriptores de seguridad en los nuevos objetos de directorio</span><span class="sxs-lookup"><span data-stu-id="77cdb-112">How security descriptors are set on new directory objects</span></span>](how-security-descriptors-are-set-on-new-directory-objects.md)
-   [<span data-ttu-id="77cdb-113">Crear un descriptor de seguridad para un nuevo objeto de directorio</span><span class="sxs-lookup"><span data-stu-id="77cdb-113">Creating a Security Descriptor for a New Directory Object</span></span>](creating-a-security-descriptor-for-a-new-directory-object.md)
-   [<span data-ttu-id="77cdb-114">Usar la herencia de permisos de acceso para habilitar el acceso administrativo a un subárbol completo del directorio</span><span class="sxs-lookup"><span data-stu-id="77cdb-114">Using inheritance of access permissions to enable administrative access to an entire subtree of the directory</span></span>](inheritance-and-delegation-of-administration.md)
-   [<span data-ttu-id="77cdb-115">Crear, modificar y leer el descriptor de seguridad predeterminado para una clase de objeto</span><span class="sxs-lookup"><span data-stu-id="77cdb-115">Creating, modifying, and reading the default security descriptor for an object class</span></span>](default-security-descriptor.md)
-   [<span data-ttu-id="77cdb-116">Crear, establecer y comprobar los derechos de acceso de control para las operaciones que van más allá de las que se incluyen en los derechos predefinidos</span><span class="sxs-lookup"><span data-stu-id="77cdb-116">Creating, setting, and checking control access rights for operations that go beyond those covered by the predefined rights</span></span>](control-access-rights.md)
-   [<span data-ttu-id="77cdb-117">Usar DsAddSidHistory</span><span class="sxs-lookup"><span data-stu-id="77cdb-117">Using DsAddSidHistory</span></span>](using-dsaddsidhistory.md)
-   [<span data-ttu-id="77cdb-118">Controlar la visibilidad de los objetos</span><span class="sxs-lookup"><span data-stu-id="77cdb-118">Controlling Object Visibility</span></span>](controlling-object-visibility.md)
-   [<span data-ttu-id="77cdb-119">DACL NULL y listas DACL vacías</span><span class="sxs-lookup"><span data-stu-id="77cdb-119">Null DACLs and Empty DACLs</span></span>](null-dacls-and-empty-dacls.md)

 

 




