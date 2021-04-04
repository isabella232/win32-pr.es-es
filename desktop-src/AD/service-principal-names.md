---
title: Nombres de entidad de seguridad de servicio
description: Un nombre de entidad de seguridad de servicio (SPN) es un identificador único de una instancia de servicio.
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- Nombres de entidad de seguridad de servicio
- SPN; consulte nombres de entidad de seguridad de servicio
- nombre de entidad de seguridad de servicio AD
- nombre principal de servicio AD, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa34b7d90803a324faced7d67b56c0b6a1f13af
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904469"
---
# <a name="service-principal-names"></a><span data-ttu-id="7be27-107">Nombres de entidad de seguridad de servicio</span><span class="sxs-lookup"><span data-stu-id="7be27-107">Service Principal Names</span></span>

<span data-ttu-id="7be27-108">Un nombre de entidad de seguridad de servicio (SPN) es un identificador único de una instancia de servicio.</span><span class="sxs-lookup"><span data-stu-id="7be27-108">A service principal name (SPN) is a unique identifier of a service instance.</span></span> <span data-ttu-id="7be27-109">La [autenticación Kerberos](mutual-authentication-using-kerberos.md) utiliza los SPN para asociar una instancia de servicio con una cuenta de inicio de sesión de servicio.</span><span class="sxs-lookup"><span data-stu-id="7be27-109">SPNs are used by [Kerberos authentication](mutual-authentication-using-kerberos.md) to associate a service instance with a service logon account.</span></span> <span data-ttu-id="7be27-110">Esto permite a una aplicación cliente solicitar que el servicio autentique una cuenta aunque el cliente no tenga el nombre de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="7be27-110">This allows a client application to request that the service authenticate an account even if the client does not have the account name.</span></span>

<span data-ttu-id="7be27-111">Si instala varias instancias de un servicio en equipos a lo largo de un bosque, cada instancia debe tener su propio SPN.</span><span class="sxs-lookup"><span data-stu-id="7be27-111">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="7be27-112">Una instancia de servicio determinada puede tener varios SPN si hay varios nombres que los clientes pueden usar para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="7be27-112">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span> <span data-ttu-id="7be27-113">Por ejemplo, un SPN incluye siempre el nombre del equipo host en el que se ejecuta la instancia de servicio, por lo que una instancia de servicio podría registrar un SPN para cada nombre o alias de su host.</span><span class="sxs-lookup"><span data-stu-id="7be27-113">For example, an SPN always includes the name of the host computer on which the service instance is running, so a service instance might register an SPN for each name or alias of its host.</span></span> <span data-ttu-id="7be27-114">Para obtener más información sobre el formato de SPN y la creación de un SPN único, vea [formatos de nombre para SPN únicos](name-formats-for-unique-spns.md).</span><span class="sxs-lookup"><span data-stu-id="7be27-114">For more information about SPN format and composing a unique SPN, see [Name Formats for Unique SPNs](name-formats-for-unique-spns.md).</span></span>

<span data-ttu-id="7be27-115">Antes de que el servicio de autenticación Kerberos pueda utilizar un SPN para autenticar un servicio, el SPN debe estar registrado en el objeto de cuenta que la instancia de servicio utiliza para iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="7be27-115">Before the Kerberos authentication service can use an SPN to authenticate a service, the SPN must be registered on the account object that the service instance uses to log on.</span></span> <span data-ttu-id="7be27-116">Un SPN determinado solo se puede registrar en una cuenta.</span><span class="sxs-lookup"><span data-stu-id="7be27-116">A given SPN can be registered on only one account.</span></span> <span data-ttu-id="7be27-117">En el caso de los servicios Win32, un instalador de servicio especifica la cuenta de inicio de sesión cuando se instala una instancia del servicio.</span><span class="sxs-lookup"><span data-stu-id="7be27-117">For Win32 services, a service installer specifies the logon account when an instance of the service is installed.</span></span> <span data-ttu-id="7be27-118">A continuación, el instalador compone los SPN y los escribe como una propiedad del objeto de cuenta en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="7be27-118">The installer then composes the SPNs and writes them as a property of the account object in Active Directory Domain Services.</span></span> <span data-ttu-id="7be27-119">Si la cuenta de inicio de sesión de una instancia de servicio cambia, los SPN deben registrarse de nuevo en la nueva cuenta.</span><span class="sxs-lookup"><span data-stu-id="7be27-119">If the logon account of a service instance changes, the SPNs must be re-registered under the new account.</span></span> <span data-ttu-id="7be27-120">Para obtener más información, vea [cómo un servicio registra sus SPN](how-a-service-registers-its-spns.md).</span><span class="sxs-lookup"><span data-stu-id="7be27-120">For more information, see [How a Service Registers its SPNs](how-a-service-registers-its-spns.md).</span></span>

<span data-ttu-id="7be27-121">Cuando un cliente desea conectarse a un servicio, busca una instancia del servicio, compone un SPN para esa instancia, se conecta al servicio y presenta el SPN para que lo autentique el servicio.</span><span class="sxs-lookup"><span data-stu-id="7be27-121">When a client wants to connect to a service, it locates an instance of the service, composes an SPN for that instance, connects to the service, and presents the SPN for the service to authenticate.</span></span> <span data-ttu-id="7be27-122">Para obtener más información, vea [cómo los clientes componen el SPN de un servicio](how-clients-compose-a-serviceampaposs-spn.md).</span><span class="sxs-lookup"><span data-stu-id="7be27-122">For more information, see [How Clients Compose a Service's SPN](how-clients-compose-a-serviceampaposs-spn.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7be27-123">En esta sección</span><span class="sxs-lookup"><span data-stu-id="7be27-123">In this Section</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7be27-124">En esta sección</span><span class="sxs-lookup"><span data-stu-id="7be27-124">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="7be27-125">Formatos de nombre para SPN únicos</span><span class="sxs-lookup"><span data-stu-id="7be27-125">Name Formats for Unique SPNs</span></span>](name-formats-for-unique-spns.md)
</dt> <dt>

[<span data-ttu-id="7be27-126">Cómo un servicio crea sus SPN</span><span class="sxs-lookup"><span data-stu-id="7be27-126">How a Service Composes its SPNs</span></span>](how-a-service-composes-its-spns.md)
</dt> <dt>

[<span data-ttu-id="7be27-127">Cómo un servicio registra sus SPN</span><span class="sxs-lookup"><span data-stu-id="7be27-127">How a Service Registers its SPNs</span></span>](how-a-service-registers-its-spns.md)
</dt> <dt>

[<span data-ttu-id="7be27-128">Cómo los clientes componen el SPN de un servicio</span><span class="sxs-lookup"><span data-stu-id="7be27-128">How Clients Compose a Service's SPN</span></span>](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="7be27-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7be27-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7be27-130">¿Qué es un SPN y por qué debe preocuparse?</span><span class="sxs-lookup"><span data-stu-id="7be27-130">What is an SPN and why should you care?</span></span>](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[<span data-ttu-id="7be27-131">Autenticación mutua con Kerberos</span><span class="sxs-lookup"><span data-stu-id="7be27-131">Mutual Authentication Using Kerberos</span></span>](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 