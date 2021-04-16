---
description: Para escribir un proveedor seguro es necesario tener en cuenta cómo se hospeda el proveedor, cómo el proveedor controla la suplantación y cómo asegurarse de que los usuarios tienen los derechos de acceso a los datos.
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: Protección del proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6b8fef1e90f09bc09488c058240b7fd1a88ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706082"
---
# <a name="securing-your-provider"></a><span data-ttu-id="04bd9-103">Protección del proveedor</span><span class="sxs-lookup"><span data-stu-id="04bd9-103">Securing Your Provider</span></span>

<span data-ttu-id="04bd9-104">Para escribir un proveedor seguro es necesario tener en cuenta cómo se hospeda el proveedor, cómo el proveedor controla la suplantación y cómo asegurarse de que los usuarios tienen los derechos de acceso a los datos.</span><span class="sxs-lookup"><span data-stu-id="04bd9-104">Writing a secure provider requires considering how the provider is hosted, how the provider handles impersonation, and ensuring that users are checked for access rights to data.</span></span> <span data-ttu-id="04bd9-105">Puede proteger los datos en el espacio de nombres del proveedor requiriendo que los datos se cifren antes de enviarlos a través de una red.</span><span class="sxs-lookup"><span data-stu-id="04bd9-105">You can secure the data in your provider namespace by requiring that data be encrypted authentication before sending it over a network.</span></span> <span data-ttu-id="04bd9-106">Para obtener más información, vea [requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="04bd9-106">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="04bd9-107">Si un usuario tiene acceso de **\_ escritura completo** en cualquier espacio de nombres, el usuario puede crear suscripciones entre espacios de nombres para los datos de un espacio de nombres en el que el usuario está restringido.</span><span class="sxs-lookup"><span data-stu-id="04bd9-107">If a user has **FULL\_WRITE** access in any namespace, then the user can create cross-namespace subscriptions for data in a namespace in which the user is restricted.</span></span> <span data-ttu-id="04bd9-108">Dado que un proveedor se puede cargar en cualquier espacio de nombres y ejecutarse en cualquier contexto de seguridad, el proveedor debe realizar sus propias comprobaciones de acceso para asegurarse de que solo los usuarios autorizados tienen permiso de acceso a los datos o para ejecutar métodos.</span><span class="sxs-lookup"><span data-stu-id="04bd9-108">Because a provider can be loaded into any namespace and be executing in any security context, the provider should perform its own access checks to ensure that only authorized users are allowed access to data or to execute methods.</span></span> <span data-ttu-id="04bd9-109">Para obtener más información, vea [realizar comprobaciones de acceso](performing-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="04bd9-109">For more information, see [Performing Access Checks](performing-access-checks.md).</span></span>

<span data-ttu-id="04bd9-110">En los temas siguientes se describe la seguridad del proveedor:</span><span class="sxs-lookup"><span data-stu-id="04bd9-110">The following topics discuss provider security:</span></span>

-   [<span data-ttu-id="04bd9-111">Hospedaje y seguridad de proveedores</span><span class="sxs-lookup"><span data-stu-id="04bd9-111">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
-   [<span data-ttu-id="04bd9-112">Realización de comprobaciones de acceso</span><span class="sxs-lookup"><span data-stu-id="04bd9-112">Performing Access Checks</span></span>](performing-access-checks.md)
-   [<span data-ttu-id="04bd9-113">Claves del registro para controlar la seguridad del proveedor</span><span class="sxs-lookup"><span data-stu-id="04bd9-113">Registry Keys for Controlling Provider Security</span></span>](registry-keys-for-controlling-provider-security-.md)
-   [<span data-ttu-id="04bd9-114">Acceso a los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="04bd9-114">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
-   [<span data-ttu-id="04bd9-115">Suplantar a un cliente</span><span class="sxs-lookup"><span data-stu-id="04bd9-115">Impersonating a Client</span></span>](impersonating-a-client.md)

<span data-ttu-id="04bd9-116">En los temas siguientes se describe cómo interactúan los clientes y scripts con la seguridad del proveedor:</span><span class="sxs-lookup"><span data-stu-id="04bd9-116">The following topics discuss how clients and scripts interact with provider security:</span></span>

-   [<span data-ttu-id="04bd9-117">Configuración de la autenticación en WMI</span><span class="sxs-lookup"><span data-stu-id="04bd9-117">Setting Authentication in WMI</span></span>](setting-authentication-in-wmi.md)
-   [<span data-ttu-id="04bd9-118">Conexión entre distintos sistemas operativos</span><span class="sxs-lookup"><span data-stu-id="04bd9-118">Connecting Between Different Operating Systems</span></span>](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [<span data-ttu-id="04bd9-119">Establecer el nivel de seguridad de proceso predeterminado mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="04bd9-119">Setting the Default Process Security Level Using VBScript</span></span>](setting-the-default-process-security-level-using-vbscript.md)
-   [<span data-ttu-id="04bd9-120">Establecer la seguridad del proceso de la aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="04bd9-120">Setting Client Application Process Security</span></span>](setting-client-application-process-security.md)

## <a name="related-topics"></a><span data-ttu-id="04bd9-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04bd9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04bd9-122">Mantenimiento de la seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="04bd9-122">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="04bd9-123">Usar WMI</span><span class="sxs-lookup"><span data-stu-id="04bd9-123">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
