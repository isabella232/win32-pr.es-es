---
description: Administrar el uso compartido de ensamblados y el control de versiones de DLL en el almacén de ensamblados en paralelo de los sistemas desde programas. Escriba manifiestos de ensamblado y aplicaciones autodescriptivas para el uso compartido de ensamblados y redirección de dll.
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: Aplicaciones aisladas y ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59abfbd5392040856c66ef9eb786b66d2a84500f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154098"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="4b253-104">Aplicaciones aisladas y ensamblados en paralelo</span><span class="sxs-lookup"><span data-stu-id="4b253-104">Isolated Applications and Side-by-side Assemblies</span></span>

## <a name="purpose"></a><span data-ttu-id="4b253-105">Propósito</span><span class="sxs-lookup"><span data-stu-id="4b253-105">Purpose</span></span>

<span data-ttu-id="4b253-106">Las aplicaciones aisladas y los ensamblados en paralelo son una solución de Microsoft Windows que reduce los conflictos de control de versiones en las aplicaciones cliente de Windows.</span><span class="sxs-lookup"><span data-stu-id="4b253-106">Isolated Applications and Side-by-side Assemblies is a Microsoft Windows solution that reduces versioning conflicts in Windows-client applications.</span></span> <span data-ttu-id="4b253-107">Con Windows, los desarrolladores de aplicaciones pueden crear aplicaciones aisladas que son totalmente autodescriptivas y no se ven afectadas por los cambios en el registro, en otras aplicaciones o en otras versiones de los ensamblados que se ejecutan en el sistema.</span><span class="sxs-lookup"><span data-stu-id="4b253-107">With Windows, application developers can build isolated applications that are fully self-describing and unaffected by changes to the registry, other applications, or other versions of assemblies running on the system.</span></span> <span data-ttu-id="4b253-108">Los autores y los administradores de aplicaciones pueden usar manifiestos para administrar el uso compartido de ensamblados en paralelo después de la implementación en base o por aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b253-108">Application authors and administrators can use manifests to manage the sharing of side-by-side assemblies after deployment on either a global or per-application basis.</span></span> <span data-ttu-id="4b253-109">Los clientes se benefician de las aplicaciones aisladas que son más estables y se actualizan de forma más confiable.</span><span class="sxs-lookup"><span data-stu-id="4b253-109">Customers benefit from isolated applications that are more stable and more reliably updated.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="4b253-110">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="4b253-110">Where applicable</span></span>

<span data-ttu-id="4b253-111">Las aplicaciones aisladas y el uso compartido de ensamblados en paralelo se pueden usar para desarrollar aplicaciones que compartan de forma segura ensamblados del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4b253-111">Isolated applications and side-by-side assembly sharing can be used to develop applications that safely share operating system assemblies.</span></span> <span data-ttu-id="4b253-112">Los desarrolladores pueden usar esta tecnología para corregir los conflictos de control de versiones de DLL causados por una versión incompatible de un ensamblado compartido.</span><span class="sxs-lookup"><span data-stu-id="4b253-112">Developers can use this technology to correct DLL versioning conflicts caused by an incompatible version of a shared assembly.</span></span>

<span data-ttu-id="4b253-113">Si su aplicación debe obtener sistemáticamente la versión de un componente que ha probado, es posible aislar la aplicación para que se ejecute siempre con la versión probada del componente en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="4b253-113">If your application must consistently get the version of a component you have tested, it is possible to isolate your application so that it will always be run with the tested version of the component on the user's computer.</span></span>

<span data-ttu-id="4b253-114">Las aplicaciones aisladas y los ensamblados en paralelo están diseñados para el desarrollo de aplicaciones de estilo de escritorio.</span><span class="sxs-lookup"><span data-stu-id="4b253-114">Isolated Applications and Side-by-side Assemblies is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="4b253-115">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="4b253-115">Developer audience</span></span>

<span data-ttu-id="4b253-116">Esta documentación está destinada principalmente a desarrolladores de software, desarrolladores de aplicaciones y administradores de red:</span><span class="sxs-lookup"><span data-stu-id="4b253-116">This documentation is primarily intended for software developers, application developers, and network administrators:</span></span>

-   <span data-ttu-id="4b253-117">Los desarrolladores de software que desean crear aplicaciones aisladas que usarán los ensamblados en paralelo disponibles por Microsoft y otros publicadores de ensamblados en paralelo.</span><span class="sxs-lookup"><span data-stu-id="4b253-117">Software developers who want to create isolated applications that will use the side-by-side assemblies made available by Microsoft and other side-by-side assembly publishers.</span></span>
-   <span data-ttu-id="4b253-118">Los desarrolladores de aplicaciones interesados en crear sus propios ensamblados en paralelo para aislar sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4b253-118">Application developers who are interested in creating their own side-by-side assemblies to isolate their applications.</span></span>
-   <span data-ttu-id="4b253-119">Administradores de red que desean obtener más información sobre las aplicaciones aisladas.</span><span class="sxs-lookup"><span data-stu-id="4b253-119">Network administrators who want more information about isolated applications.</span></span>

<span data-ttu-id="4b253-120">Como referencia principal para el uso compartido de ensamblados en paralelo y aplicaciones aisladas, esta documentación proporciona información general sobre la creación de manifiestos y ensamblados en paralelo, la instalación de aplicaciones aisladas y ensamblados en paralelo, y el uso de la API de contexto de activación.</span><span class="sxs-lookup"><span data-stu-id="4b253-120">As the primary reference for side-by-side assembly sharing and isolated applications, this documentation provides general background information about authoring manifests and side-by-side assemblies, installing isolated applications and side-by-side assemblies, and using the Activation Context API.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="4b253-121">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="4b253-121">Run-time requirements</span></span>

<span data-ttu-id="4b253-122">Se requiere Windows Server 2003 y versiones posteriores o Windows XP y versiones posteriores para usar ensamblados y manifiestos en paralelo para aislar las aplicaciones y usar la API de contexto de activación.</span><span class="sxs-lookup"><span data-stu-id="4b253-122">Windows Server 2003 and later or Windows XP and later is required to use side-by-side assemblies and manifests to isolate applications and to use the Activation Context API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4b253-123">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4b253-123">In this section</span></span>



| <span data-ttu-id="4b253-124">Tema</span><span class="sxs-lookup"><span data-stu-id="4b253-124">Topic</span></span>                                                         | <span data-ttu-id="4b253-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b253-125">Description</span></span>                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="4b253-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="4b253-126">Reference</span></span>](side-by-side-assemblies-reference.md)<br/> | <span data-ttu-id="4b253-127">Documentación de aplicaciones aisladas y ensamblados en paralelo.</span><span class="sxs-lookup"><span data-stu-id="4b253-127">Documentation of Isolated Applications and Side-by-side Assemblies.</span></span><br/> |



 

 

 




