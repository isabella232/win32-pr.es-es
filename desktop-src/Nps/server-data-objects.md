---
title: Objetos de datos del servidor
description: La API de objetos de datos del servidor (SDO) permite configurar y administrar mediante programación un sistema que ejecuta NPS.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eebd0f837f9a8a36af1eb9118189015e677e2af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676425"
---
# <a name="server-data-objects"></a><span data-ttu-id="7a585-103">Objetos de datos del servidor</span><span class="sxs-lookup"><span data-stu-id="7a585-103">Server Data Objects</span></span>

> [!Note]  
> <span data-ttu-id="7a585-104">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="7a585-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="7a585-105">El contenido de este tema se aplica a IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="7a585-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="7a585-106">En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.</span><span class="sxs-lookup"><span data-stu-id="7a585-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="7a585-107">La API de objetos de datos del servidor (SDO) permite configurar y administrar mediante programación un sistema que ejecuta NPS.</span><span class="sxs-lookup"><span data-stu-id="7a585-107">The Server Data Objects (SDO) API makes it possible to programmatically configure and administer a system running NPS.</span></span> <span data-ttu-id="7a585-108">Con SDO, un programador también puede escribir aplicaciones que administren directivas de acceso remoto y perfiles.</span><span class="sxs-lookup"><span data-stu-id="7a585-108">Using SDO, a developer can also write applications that administer remote access policies and profiles.</span></span> <span data-ttu-id="7a585-109">Los perfiles y directivas de acceso remoto se usan en el servicio de enrutamiento y acceso remoto (RRAS), así como en NPS para determinar si un cliente remoto puede conectarse a un servidor de acceso a la red (NAS).</span><span class="sxs-lookup"><span data-stu-id="7a585-109">The remote access policies and profiles are used by the Routing and Remote Access Service (RRAS) as well as NPS to determine whether a remote client is allowed to connect to a network access server (NAS).</span></span>

<span data-ttu-id="7a585-110">La API SDO es aplicable en cualquier entorno que use directivas de acceso remoto o NPS.</span><span class="sxs-lookup"><span data-stu-id="7a585-110">The SDO API is applicable in any environment that uses NPS or Remote Access Policies.</span></span>

<span data-ttu-id="7a585-111">Con la API SDO, un desarrollador puede manipular cualquier elemento de la configuración de NPS que sea accesible a través de la interfaz de usuario de NPS.</span><span class="sxs-lookup"><span data-stu-id="7a585-111">With the SDO API, a developer can manipulate any element of the NPS configuration that is accessible through the NPS user interface.</span></span>

<span data-ttu-id="7a585-112">La API SDO también permite establecer o recuperar cualquiera de los valores accesibles a través de la página de propiedades configuración de marcado del usuario.</span><span class="sxs-lookup"><span data-stu-id="7a585-112">The SDO API also makes it possible to set or retrieve any of the values accessible through the user dial-in settings property page.</span></span>

<span data-ttu-id="7a585-113">La API SDO se compone de interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="7a585-113">The SDO API is composed of COM interfaces.</span></span> <span data-ttu-id="7a585-114">Cada una de las interfaces de la API de SDO hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) de com.</span><span class="sxs-lookup"><span data-stu-id="7a585-114">Each of the interfaces in the SDO API inherits from the COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="7a585-115">La interfaz **IDispatch** permite a los desarrolladores llamar a los métodos de interfaz SDO desde Visual Basic o cualquier cliente de automatización, así como desde C/C++.</span><span class="sxs-lookup"><span data-stu-id="7a585-115">The **IDispatch** interface enables developers to call the SDO interface methods from Visual Basic or any Automation client, as well as from C/C++.</span></span>

<span data-ttu-id="7a585-116">Los desarrolladores también pueden llamar a la API SDO desde lenguajes de scripting como VBScript.</span><span class="sxs-lookup"><span data-stu-id="7a585-116">Developers can also call the SDO API from scripting languages such as VBScript.</span></span> <span data-ttu-id="7a585-117">Sin embargo, dado que VBScript está limitado a usar solo parámetros de tipo variante, no toda la funcionalidad de SDO está disponible.</span><span class="sxs-lookup"><span data-stu-id="7a585-117">However, because VBScript is limited to using VARIANT-type parameters only, not all the functionality of SDO is available.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7a585-118">En esta sección</span><span class="sxs-lookup"><span data-stu-id="7a585-118">In This Section</span></span>

[<span data-ttu-id="7a585-119">Información general</span><span class="sxs-lookup"><span data-stu-id="7a585-119">Overview</span></span>](/windows/desktop/Nps/sdo-about-server-data-objects)

<span data-ttu-id="7a585-120">Información general sobre la API de objetos de datos del servidor.</span><span class="sxs-lookup"><span data-stu-id="7a585-120">General information about the Server Data Objects API.</span></span>

[<span data-ttu-id="7a585-121">Utilizan</span><span class="sxs-lookup"><span data-stu-id="7a585-121">Using</span></span>](/windows/desktop/Nps/sdo-using-server-data-objects)

<span data-ttu-id="7a585-122">Código de ejemplo que muestra cómo usar la API de objetos de datos del servidor.</span><span class="sxs-lookup"><span data-stu-id="7a585-122">Sample code that demonstrates how to use the Server Data Objects API.</span></span>

[<span data-ttu-id="7a585-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="7a585-123">Reference</span></span>](/windows/desktop/Nps/sdo-server-data-objects-reference)

<span data-ttu-id="7a585-124">Documentación de los tipos e interfaces enumerados que componen la API de objetos de datos del servidor.</span><span class="sxs-lookup"><span data-stu-id="7a585-124">Documentation of the enumerated types and interfaces that compose the Server Data Objects API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a585-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a585-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a585-126">Servidor de directivas de redes (servicio de autenticación de Internet)</span><span class="sxs-lookup"><span data-stu-id="7a585-126">Network Policy Server (Internet Authentication Service)</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="7a585-127">Servicio de acceso remoto</span><span class="sxs-lookup"><span data-stu-id="7a585-127">Remote Access Service</span></span>](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 