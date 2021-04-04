---
title: Descriptor de seguridad predeterminado
description: Con Active Directory Domain Services, también puede especificar la seguridad predeterminada para cada tipo de objeto.
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- Descriptor de seguridad predeterminado AD
- descriptores de seguridad (AD), predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372f285c3e8c17b481811d7356c40ae07316801d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077537"
---
# <a name="default-security-descriptor"></a><span data-ttu-id="13d51-105">Descriptor de seguridad predeterminado</span><span class="sxs-lookup"><span data-stu-id="13d51-105">Default Security Descriptor</span></span>

<span data-ttu-id="13d51-106">Con Active Directory Domain Services, también puede especificar la seguridad predeterminada para cada tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="13d51-106">With Active Directory Domain Services, you can also specify default security for each type of object.</span></span> <span data-ttu-id="13d51-107">Esto se especifica en el atributo [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) de la definición del objeto [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) en el [esquema de Active Directory](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="13d51-107">This is specified in the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) attribute in the [**classSchema**](/windows/desktop/ADSchema/c-classschema) object definition in the [Active Directory schema](active-directory-schema.md).</span></span> <span data-ttu-id="13d51-108">Este descriptor de seguridad se usa para proporcionar protección predeterminada en el objeto si no se especifica ningún descriptor de seguridad durante la creación del objeto.</span><span class="sxs-lookup"><span data-stu-id="13d51-108">This security descriptor is used to provide default protection on the object if there is no security descriptor specified during the creation of the object.</span></span>

> [!Note]  
> <span data-ttu-id="13d51-109">Las ACE de un descriptor de seguridad predeterminado se administran como si se hubieran especificado como parte de la creación de objetos.</span><span class="sxs-lookup"><span data-stu-id="13d51-109">ACEs from a default security descriptor are handled as if they were specified as part of object creation.</span></span> <span data-ttu-id="13d51-110">Por lo tanto, las ACE predeterminadas se colocan delante de las ACE heredadas y las reemplazan según corresponda.</span><span class="sxs-lookup"><span data-stu-id="13d51-110">Therefore, the default ACEs are placed preceding inherited ACEs and override them as appropriate.</span></span> <span data-ttu-id="13d51-111">Para obtener más información, vea [orden de las ACE en una DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="13d51-111">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

<span data-ttu-id="13d51-112">[**DefaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) se especifica en un formato de cadena especial mediante el [lenguaje de definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).</span><span class="sxs-lookup"><span data-stu-id="13d51-112">The [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) is specified in a special string format using the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).</span></span> <span data-ttu-id="13d51-113">Se pueden usar dos funciones para convertir el formato binario del descriptor de seguridad al formato de cadena y viceversa.</span><span class="sxs-lookup"><span data-stu-id="13d51-113">Two functions can be used to convert binary form of the security descriptor to string format and vice versa.</span></span> <span data-ttu-id="13d51-114">Estas funciones son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="13d51-114">These functions are:</span></span>

-   [<span data-ttu-id="13d51-115">ConvertSecurityDescriptorToStringSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="13d51-115">ConvertSecurityDescriptorToStringSecurityDescriptor</span></span>](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [<span data-ttu-id="13d51-116">ConvertStringSecurityDescriptorToSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="13d51-116">ConvertStringSecurityDescriptorToSecurityDescriptor</span></span>](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

<span data-ttu-id="13d51-117">Para obtener más información y los descriptores de seguridad predeterminados de las clases de objeto predefinidas, vea las páginas de referencia de la clase en la Active Directory referencia de esquema de la [referencia de Active Directory Domain Services](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="13d51-117">For more information and the default security descriptors of the predefined object classes, see the class reference pages in the Active Directory Schema Reference of the [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

<span data-ttu-id="13d51-118">Para obtener más información y un ejemplo de código que lee o modifica la propiedad [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) de una clase de objeto, vea [leer el DefaultSecurityDescriptor de una clase de objeto](reading-the-defaultsecuritydescriptor-for-an-object-class.md) y [modificar DefaultSecurityDescriptor para una clase de objeto](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).</span><span class="sxs-lookup"><span data-stu-id="13d51-118">For more information and a code example that reads or modifies the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) property of an object class, see [Reading the defaultSecurityDescriptor for an Object Class](reading-the-defaultsecuritydescriptor-for-an-object-class.md) and [Modifying the defaultSecurityDescriptor for an Object Class](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).</span></span>

 

 