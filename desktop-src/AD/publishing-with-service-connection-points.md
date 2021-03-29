---
title: Publicar con puntos de conexión de servicio
description: El esquema de Active Directory define una clase de objeto serviceConnectionPoint (SCP) para facilitar a un servicio la publicación de datos específicos del servicio en el directorio.
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- Publicación con puntos de conexión de servicio AD
- puntos de conexión de servicio AD
- puntos de conexión de servicio AD, publicación con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a458822f6c5e4d764b2e330c7ba084021b586548
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773111"
---
# <a name="publishing-with-service-connection-points"></a><span data-ttu-id="a4f76-106">Publicar con puntos de conexión de servicio</span><span class="sxs-lookup"><span data-stu-id="a4f76-106">Publishing with Service Connection Points</span></span>

<span data-ttu-id="a4f76-107">El esquema de Active Directory define una clase de objeto **serviceConnectionPoint** (SCP) para facilitar a un servicio la publicación de datos específicos del servicio en el directorio.</span><span class="sxs-lookup"><span data-stu-id="a4f76-107">The Active Directory Schema defines a **serviceConnectionPoint** (SCP) object class to make it easy for a service to publish service-specific data in the directory.</span></span> <span data-ttu-id="a4f76-108">Los clientes del servicio usan los datos de un SCP para buscar, conectarse y autenticar una instancia de su servicio.</span><span class="sxs-lookup"><span data-stu-id="a4f76-108">Clients of the service use the data in an SCP to locate, connect to, and authenticate an instance of your service.</span></span>

<span data-ttu-id="a4f76-109">En esta sección se proporciona información general sobre los puntos de conexión de servicio y ejemplos de código que muestran cómo una aplicación de cliente o servicio utiliza los SCP.</span><span class="sxs-lookup"><span data-stu-id="a4f76-109">This section provides an overview of service connection points and code examples that show how a client/service application uses SCPs.</span></span>

<span data-ttu-id="a4f76-110">En el ejemplo de código se siguen estos pasos para implementar la publicación de servicio con SCP.</span><span class="sxs-lookup"><span data-stu-id="a4f76-110">The code example follows these steps to implement service publication with SCPs.</span></span>

<span data-ttu-id="a4f76-111">Para obtener más información y un ejemplo de código que realice estos pasos, consulte [crear un punto de conexión de servicio](creating-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="a4f76-111">For more information and a code example that performs these steps, see [Creating a Service Connection Point](creating-a-service-connection-point.md).</span></span>

<span data-ttu-id="a4f76-112">**Para crear SCP en el directorio en la instalación del servicio**</span><span class="sxs-lookup"><span data-stu-id="a4f76-112">**To create SCPs in the directory at service installation**</span></span>

1.  <span data-ttu-id="a4f76-113">Enlazar al objeto de equipo para el equipo host en el que está instalada la instancia de servicio.</span><span class="sxs-lookup"><span data-stu-id="a4f76-113">Bind to the computer object for the host computer on which the service instance is installed.</span></span>
2.  <span data-ttu-id="a4f76-114">Cree un objeto SCP como elemento secundario del objeto Computer y especifique los valores iniciales de los atributos del SCP.</span><span class="sxs-lookup"><span data-stu-id="a4f76-114">Create an SCP object as a child of the computer object, specifying the initial values for the attributes of the SCP.</span></span>
3.  <span data-ttu-id="a4f76-115">Establezca entradas de control de acceso (ACE) en el descriptor de seguridad del objeto SCP para permitir que el servicio modifique las propiedades de SCP en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a4f76-115">Set access control entries (ACEs) in the security descriptor of the SCP object to enable the service to modify SCP properties at run time.</span></span>
4.  <span data-ttu-id="a4f76-116">Almacene en caché el **objectGUID** del SCP en el registro en el equipo host del servicio.</span><span class="sxs-lookup"><span data-stu-id="a4f76-116">Cache the **objectGUID** of the SCP in the registry on the service's host computer.</span></span>

<span data-ttu-id="a4f76-117">Para obtener más información y un ejemplo de código que realice estos pasos, vea [actualizar un punto de conexión de servicio](updating-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="a4f76-117">For more information and a code example that performs these steps, see [Updating a Service Connection Point](updating-a-service-connection-point.md).</span></span>

<span data-ttu-id="a4f76-118">**Para actualizar los atributos de SCP en el inicio del servicio**</span><span class="sxs-lookup"><span data-stu-id="a4f76-118">**To update the SCP attributes at service startup**</span></span>

1.  <span data-ttu-id="a4f76-119">Recupere el **objectGUID** del registro y úselo para enlazar con el SCP.</span><span class="sxs-lookup"><span data-stu-id="a4f76-119">Retrieve the **objectGUID** from the registry and use it to bind to the SCP.</span></span>
2.  <span data-ttu-id="a4f76-120">Recupere los atributos, como **serviceDNSName** y **SERVICEBINDINGINFORMATION**, del SCP.</span><span class="sxs-lookup"><span data-stu-id="a4f76-120">Retrieve attributes, such as **serviceDNSName** and **serviceBindingInformation**, from the SCP.</span></span> <span data-ttu-id="a4f76-121">Compare estos valores con los valores actuales y actualice el SCP si es necesario.</span><span class="sxs-lookup"><span data-stu-id="a4f76-121">Compare these values to the current values and update the SCP if necessary.</span></span>

<span data-ttu-id="a4f76-122">Para obtener más información y un ejemplo de código que realice estos pasos, vea [cómo los clientes buscan y usan un punto de conexión de servicio](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="a4f76-122">For more information and a code example that performs these steps, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="a4f76-123">**Para buscar y usar un SCP por parte de una aplicación cliente**</span><span class="sxs-lookup"><span data-stu-id="a4f76-123">**To find and use an SCP by a client application**</span></span>

1.  <span data-ttu-id="a4f76-124">Enlazar con el catálogo global y buscar objetos con un atributo **Keywords** que coincida con el GUID del producto del servicio.</span><span class="sxs-lookup"><span data-stu-id="a4f76-124">Bind to the Global Catalog and search for objects with a **keywords** attribute that matches the service's product GUID.</span></span> <span data-ttu-id="a4f76-125">Cada objeto encontrado es una instancia del servicio.</span><span class="sxs-lookup"><span data-stu-id="a4f76-125">Each object found is an instance of the service.</span></span> <span data-ttu-id="a4f76-126">Seleccione una instancia y recupere el nombre distintivo del SCP.</span><span class="sxs-lookup"><span data-stu-id="a4f76-126">Select an instance and retrieve the distinguished name of the SCP.</span></span>
2.  <span data-ttu-id="a4f76-127">Use el nombre completo para establecer un enlace al SCP.</span><span class="sxs-lookup"><span data-stu-id="a4f76-127">Use the distinguished name to bind to the SCP.</span></span>
3.  <span data-ttu-id="a4f76-128">Recupere los valores de varios atributos del SCP, como **serviceDNSName** y **serviceBindingInformation**.</span><span class="sxs-lookup"><span data-stu-id="a4f76-128">Retrieve the values of various attributes from the SCP, such as **serviceDNSName** and **serviceBindingInformation**.</span></span> <span data-ttu-id="a4f76-129">Use estos valores para conectarse a la instancia de servicio y autenticarla.</span><span class="sxs-lookup"><span data-stu-id="a4f76-129">Use these values to connect to and authenticate the service instance.</span></span>

<span data-ttu-id="a4f76-130">Para obtener más información sobre los roles que pueden crear y actualizar un SCP, consulte [problemas de seguridad de la publicación de servicio](security-issues-for-service-publication.md).</span><span class="sxs-lookup"><span data-stu-id="a4f76-130">For more information about what roles can create and update an SCP, see [Security Issues for Service Publication](security-issues-for-service-publication.md).</span></span>

<span data-ttu-id="a4f76-131">Para obtener más información acerca de dónde crear un SCP, consulte [dónde crear un punto de conexión de servicio](where-to-create-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="a4f76-131">For more information about where to create an SCP, see [Where to Create a Service Connection Point](where-to-create-a-service-connection-point.md).</span></span>

<span data-ttu-id="a4f76-132">Para obtener más información sobre el tipo de datos que se almacenan en un SCP, consulte [propiedades de punto de conexión de servicio](service-connection-point-properties.md).</span><span class="sxs-lookup"><span data-stu-id="a4f76-132">For more information about the kind of data to store in an SCP, see [Service Connection Point Properties](service-connection-point-properties.md).</span></span>

<span data-ttu-id="a4f76-133">Para obtener más información sobre cómo un instalador de servicio y el servicio trabajan juntos para mantener los datos actuales en un SCP, vea [crear y mantener un punto de conexión de servicio](creating-and-maintaining-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="a4f76-133">For more information about how a service installer and the service work together to maintain current data in an SCP, see [Creating and Maintaining a Service Connection Point](creating-and-maintaining-a-service-connection-point.md).</span></span>

 

 




