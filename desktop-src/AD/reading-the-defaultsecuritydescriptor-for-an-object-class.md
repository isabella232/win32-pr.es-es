---
title: Leer defaultSecurityDescriptor para una clase de objeto
description: Con ADSI, puede obtener el atributo defaultSecurityDescriptor de una clase de objeto con la interfaz IADs.
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, leer defaultSecurityDescriptor para una clase de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e217ae42214c2c07867c2a57427d74fb7636736
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077500"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a><span data-ttu-id="405c4-104">Leer defaultSecurityDescriptor para una clase de objeto</span><span class="sxs-lookup"><span data-stu-id="405c4-104">Reading the defaultSecurityDescriptor for an Object Class</span></span>

<span data-ttu-id="405c4-105">Con ADSI, puede obtener el atributo **defaultSecurityDescriptor** de una clase de objeto con la interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="405c4-105">Using ADSI, you can obtain the **defaultSecurityDescriptor** attribute for an object class with the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="405c4-106">Para obtener el atributo **defaultSecurityDescriptor** de una clase de objeto, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="405c4-106">To obtain the **defaultSecurityDescriptor** attribute for an object class, perform the following steps.</span></span>

1.  <span data-ttu-id="405c4-107">Obtiene un puntero de interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) al objeto **ClassSchema** para la clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="405c4-107">Get an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface pointer to the **classSchema** object for the object class.</span></span>
2.  <span data-ttu-id="405c4-108">Use el método [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) para obtener el descriptor de seguridad predeterminado del objeto.</span><span class="sxs-lookup"><span data-stu-id="405c4-108">Use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to get the default security descriptor of the object.</span></span> <span data-ttu-id="405c4-109">El nombre de la propiedad que contiene el descriptor de seguridad es "defaultSecurityDescriptor".</span><span class="sxs-lookup"><span data-stu-id="405c4-109">The name of the property that contains the security descriptor is "defaultSecurityDescriptor".</span></span> <span data-ttu-id="405c4-110">La propiedad se devolverá como una [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) que contiene un BSTR con el descriptor de seguridad predeterminado en el formato de cadena SDDL.</span><span class="sxs-lookup"><span data-stu-id="405c4-110">The property will be returned as a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) containing a BSTR with the default security descriptor in SDDL string format.</span></span>
3.  <span data-ttu-id="405c4-111">Utilice la función [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para convertir el formato de cadena SDDL en un descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="405c4-111">Use the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function to convert the SDDL string form to a security descriptor.</span></span>
4.  <span data-ttu-id="405c4-112">Use las API de seguridad [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)y [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) para leer los elementos del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="405c4-112">Use the [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner), and [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) Security APIs to read the parts of the security descriptor.</span></span>

<span data-ttu-id="405c4-113">Para ver un ejemplo de código que muestra cómo hacerlo, consulte el [código de ejemplo para leer defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="405c4-113">For a code example that demonstrates how to do this, see [Example Code for Reading defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).</span></span>

 

 