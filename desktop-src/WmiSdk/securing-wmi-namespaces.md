---
description: Los descriptores de seguridad controlan el acceso a los espacios de nombres de WMI y sus datos.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Proteger los espacios de nombres de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f605a6cd1136e70d6c5243b9e143fdb167d41808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715755"
---
# <a name="securing-wmi-namespaces"></a><span data-ttu-id="34aa9-103">Proteger los espacios de nombres de WMI</span><span class="sxs-lookup"><span data-stu-id="34aa9-103">Securing WMI Namespaces</span></span>

<span data-ttu-id="34aa9-104">Los [*descriptores de seguridad*](gloss-s.md)controlan el acceso a los espacios de nombres de WMI y sus datos.</span><span class="sxs-lookup"><span data-stu-id="34aa9-104">Access to WMI namespaces and their data is controlled by [*security descriptors*](gloss-s.md).</span></span> <span data-ttu-id="34aa9-105">Puede proteger los datos de los [*espacios de nombres*](gloss-n.md) ajustando el descriptor de seguridad del espacio de nombres para controlar quién tiene acceso a los datos y métodos.</span><span class="sxs-lookup"><span data-stu-id="34aa9-105">You can protect data in your [*namespaces*](gloss-n.md) by adjusting the namespace security descriptor to control who has access to the data and methods.</span></span> <span data-ttu-id="34aa9-106">Para obtener más información, vea [acceso a objetos protegibles de WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="34aa9-106">For more information, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>


<span data-ttu-id="34aa9-107">En los temas siguientes se describe la seguridad del espacio de nombres WMI y cómo controlar el acceso a los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="34aa9-107">The following topics describe WMI namespace security and how to control access to namespaces.</span></span>

<dl> <dt>

<span data-ttu-id="34aa9-108"><span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md)</span><span class="sxs-lookup"><span data-stu-id="34aa9-108"><span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Access to WMI Namespaces](access-to-wmi-namespaces.md)</span></span>
</dt> <dd>

<span data-ttu-id="34aa9-109">La seguridad del espacio de nombres WMI se basa en los [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) de usuario (SID) y listas de control de acceso estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="34aa9-109">WMI namespace security relies on standard Windows user [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) and access control lists.</span></span> <span data-ttu-id="34aa9-110">Los administradores y los usuarios tienen permisos predeterminados diferentes.</span><span class="sxs-lookup"><span data-stu-id="34aa9-110">Administrators and users have different default permissions.</span></span>

</dd> <dt>

<span data-ttu-id="34aa9-111"><span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Configuración de descriptores de seguridad de espacios de nombres](setting-namespace-security-descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="34aa9-111"><span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md)</span></span>
</dt> <dd>

<span data-ttu-id="34aa9-112">Después de que exista un espacio de nombres en el repositorio WMI, puede cambiar la seguridad en el espacio de nombres mediante el control WMI o llamando a los métodos de [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="34aa9-112">After a namespace exists in the WMI repository, you can change the security on the namespace by using the WMI Control or by calling the methods of [**\_\_SystemSecurity**](--systemsecurity.md).</span></span>

</dd> <dt>

<span data-ttu-id="34aa9-113"><span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="34aa9-113"><span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md)</span></span>
</dt> <dd>

<span data-ttu-id="34aa9-114">El calificador **RequiresEncryption** de un espacio de nombres requiere que la aplicación cliente WMI o el script utilicen el nivel de autenticación que cifra las llamadas a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="34aa9-114">The **RequiresEncryption** qualifier on a namespace requires the WMI client application or script to use the authentication level which encrypts remote procedure calls.</span></span> <span data-ttu-id="34aa9-115">Las solicitudes de datos entrantes y las devoluciones de llamada asincrónicas se deben cifrar.</span><span class="sxs-lookup"><span data-stu-id="34aa9-115">Both incoming data requests and asynchronous callbacks must be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="34aa9-116"><span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Establecer la herencia de la seguridad del espacio de nombres](establishing-inheritance-of-namespace-security.md)</span><span class="sxs-lookup"><span data-stu-id="34aa9-116"><span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Establishing Inheritance of Namespace Security](establishing-inheritance-of-namespace-security.md)</span></span>
</dt> <dd>

<span data-ttu-id="34aa9-117">Puede controlar si un espacio de nombres secundario hereda el descriptor de seguridad del espacio de nombres primario.</span><span class="sxs-lookup"><span data-stu-id="34aa9-117">You can control whether a child namespace inherits the security descriptor of the parent namespace.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="34aa9-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="34aa9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34aa9-119">Mantenimiento de la seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="34aa9-119">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="34aa9-120">Conexión a WMI en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="34aa9-120">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="34aa9-121">Crear un espacio de nombres con la API de WMI</span><span class="sxs-lookup"><span data-stu-id="34aa9-121">Creating a Namespace with the WMI API</span></span>](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[<span data-ttu-id="34aa9-122">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="34aa9-122">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
