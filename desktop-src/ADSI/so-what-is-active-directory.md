---
title: Información general del tutorial ADSI con Visual Basic
description: Active Directory es una base de datos de uso especial \ 8212; no es un reemplazo del registro.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607d9da26d1c96d7cb6f83a799c7633404e5bb4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104559779"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a><span data-ttu-id="2bc03-103">Información general del tutorial: ADSI con Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2bc03-103">Tutorial Overview: ADSI with Visual Basic</span></span>

> [!Note]  
> <span data-ttu-id="2bc03-104">La siguiente documentación es parte de una descripción del escenario extendido para los desarrolladores de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2bc03-104">The following documentation is part of an extended scenario description for Visual Basic developers.</span></span> <span data-ttu-id="2bc03-105">Si está buscando una introducción general de Active Directory, consulte los [documentos de profesionales de TI en TechNet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="2bc03-105">If you are looking for a general overview of Active Directory, see the [IT Pro docs on Technet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)).</span></span> <span data-ttu-id="2bc03-106">Para obtener una visión más detallada del lado de desarrollo de Active Directory, vea [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="2bc03-106">For a more in-depth look at the development side of Active Directory, see [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services).</span></span> <span data-ttu-id="2bc03-107">Para obtener una introducción más grande a las interfaces de servicio de Active Directory, vea el tema principal de este tema: Active Directory de las [interfaces de servicio](active-directory-service-interfaces-adsi.md), así como el tema relacionado: [acerca de las interfaces de servicio de Active Directory](about-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="2bc03-107">For a larger introduction to Active Directory Service Interfaces, see this topic's parent topic: [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md), as well as the sibling topic: [About Active Directory Service Interfaces](about-adsi.md).</span></span>

 

<span data-ttu-id="2bc03-108">Active Directory es una base de datos Especial, no es un reemplazo del registro.</span><span class="sxs-lookup"><span data-stu-id="2bc03-108">Active Directory is a special-purpose database — it is not a registry replacement.</span></span> <span data-ttu-id="2bc03-109">El directorio está diseñado para controlar un gran número de operaciones de lectura y búsqueda y un número significativamente menor de cambios y actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="2bc03-109">The directory is designed to handle a large number of read and search operations and a significantly smaller number of changes and updates.</span></span> <span data-ttu-id="2bc03-110">Active Directory datos son jerárquicos, replicados y extensibles.</span><span class="sxs-lookup"><span data-stu-id="2bc03-110">Active Directory data is hierarchical, replicated, and extensible.</span></span> <span data-ttu-id="2bc03-111">Dado que se replica, no desea almacenar los datos dinámicos, como los precios de las acciones corporativas o el rendimiento de la CPU.</span><span class="sxs-lookup"><span data-stu-id="2bc03-111">Because it is replicated, you do not want to store dynamic data, such as corporate stock prices or CPU performance.</span></span> <span data-ttu-id="2bc03-112">Si los datos son específicos de la máquina, almacene los datos en el registro.</span><span class="sxs-lookup"><span data-stu-id="2bc03-112">If your data is machine-specific, store the data in the registry.</span></span> <span data-ttu-id="2bc03-113">Algunos ejemplos típicos de los datos almacenados en el directorio son los datos de la cola de impresión, los datos de contacto de usuario y los datos de configuración de red o equipo.</span><span class="sxs-lookup"><span data-stu-id="2bc03-113">Typical examples of data stored in the directory include printer queue data, user contact data, and network/computer configuration data.</span></span> <span data-ttu-id="2bc03-114">La base de datos Active Directory consta de objetos y atributos.</span><span class="sxs-lookup"><span data-stu-id="2bc03-114">The Active Directory database consists of objects and attributes.</span></span> <span data-ttu-id="2bc03-115">Los objetos y las definiciones de atributo se almacenan en el esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2bc03-115">Objects and attribute definitions are stored in the Active Directory schema.</span></span>

<span data-ttu-id="2bc03-116">Es posible que se pregunte qué objetos están almacenados actualmente en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2bc03-116">You may be wondering what objects are currently stored in Active Directory.</span></span> <span data-ttu-id="2bc03-117">Active Directory tiene tres particiones.</span><span class="sxs-lookup"><span data-stu-id="2bc03-117">Active Directory has three partitions.</span></span> <span data-ttu-id="2bc03-118">También se conocen como contextos de nomenclatura: dominio, esquema y configuración.</span><span class="sxs-lookup"><span data-stu-id="2bc03-118">These are also known as naming contexts: domain, schema, and configuration.</span></span> <span data-ttu-id="2bc03-119">La partición de dominio contiene usuarios, grupos, contactos, equipos, unidades organizativas y muchos otros tipos de objetos.</span><span class="sxs-lookup"><span data-stu-id="2bc03-119">The domain partition contains users, groups, contacts, computers, organizational units, and many other object types.</span></span> <span data-ttu-id="2bc03-120">Dado que Active Directory es extensible, también puede agregar sus propios atributos y clases.</span><span class="sxs-lookup"><span data-stu-id="2bc03-120">Because Active Directory is extensible, you can also add your own classes and/or attributes.</span></span> <span data-ttu-id="2bc03-121">La partición del esquema contiene clases y definiciones de atributos.</span><span class="sxs-lookup"><span data-stu-id="2bc03-121">The schema partition contains classes and attribute definitions.</span></span> <span data-ttu-id="2bc03-122">La partición de configuración incluye datos de configuración de servicios, particiones y sitios.</span><span class="sxs-lookup"><span data-stu-id="2bc03-122">The configuration partition includes configuration data for services, partitions, and sites.</span></span>

<span data-ttu-id="2bc03-123">En la captura de pantalla siguiente se muestra la Active Directory partición de dominio.</span><span class="sxs-lookup"><span data-stu-id="2bc03-123">The following screen shot shows the Active Directory domain partition.</span></span>

![partición de dominio de Active Directory](images/adadsi1.png)

## <a name="related-topics"></a><span data-ttu-id="2bc03-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2bc03-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bc03-126">Obtener acceso a Active Directory mediante Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2bc03-126">Accessing Active Directory Using Visual Basic</span></span>](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[<span data-ttu-id="2bc03-127">Escenario: fabrikam Corporation</span><span class="sxs-lookup"><span data-stu-id="2bc03-127">Scenario: The Fabrikam Corporation</span></span>](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[<span data-ttu-id="2bc03-128">Temas avanzados</span><span class="sxs-lookup"><span data-stu-id="2bc03-128">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 