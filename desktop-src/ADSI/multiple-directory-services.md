---
title: Varios servicios de directorio
description: Un desafío de trabajar en un entorno informático distribuido es identificar y ubicar recursos como usuarios, grupos, colas de impresión y documentos.
ms.assetid: 66929290-b830-4768-a2ae-604d1a9de5c4
ms.tgt_platform: multiple
keywords:
- ADSI de varios servicios de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc2e174fc1b07564f1cca6c12093a289a0c865a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356706"
---
# <a name="multiple-directory-services"></a><span data-ttu-id="d9814-104">Varios servicios de directorio</span><span class="sxs-lookup"><span data-stu-id="d9814-104">Multiple Directory Services</span></span>

<span data-ttu-id="d9814-105">Un desafío de trabajar en un entorno informático distribuido es identificar y ubicar recursos como usuarios, grupos, colas de impresión y documentos.</span><span class="sxs-lookup"><span data-stu-id="d9814-105">One challenge of working within a distributed computing environment is identifying and locating resources such as users, groups, print queues, and documents.</span></span> <span data-ttu-id="d9814-106">Un servicio de directorio es la parte de un entorno informático distribuido que proporciona una manera de buscar e identificar los usuarios y los recursos disponibles en el sistema.</span><span class="sxs-lookup"><span data-stu-id="d9814-106">A directory service is the part of a distributed computing environment that provides a way to locate and identify the users and resources available in the system.</span></span> <span data-ttu-id="d9814-107">Un servicio de directorio es como un directorio de teléfono.</span><span class="sxs-lookup"><span data-stu-id="d9814-107">A directory service is like a phone directory.</span></span> <span data-ttu-id="d9814-108">Dado un nombre para una persona o un recurso, proporciona los datos necesarios para tener acceso a esa persona o recurso.</span><span class="sxs-lookup"><span data-stu-id="d9814-108">Given a name for a person or a resource, it provides the data necessary to access that person or resource.</span></span> <span data-ttu-id="d9814-109">No es necesario empezar con los datos de enlace para tener acceso a un recurso de la red.</span><span class="sxs-lookup"><span data-stu-id="d9814-109">You do not have to start with binding data to access a resource on the network.</span></span>

<span data-ttu-id="d9814-110">La mayoría de las empresas ya tienen muchos directorios diferentes en su lugar.</span><span class="sxs-lookup"><span data-stu-id="d9814-110">Most enterprises already have many different directories in place.</span></span> <span data-ttu-id="d9814-111">Por ejemplo, los sistemas operativos de red, los sistemas de correo electrónico y los productos de "Groupware" tienen sus propios directorios.</span><span class="sxs-lookup"><span data-stu-id="d9814-111">For example, network operating systems, electronic mail systems, and "groupware" products all have their own directories.</span></span> <span data-ttu-id="d9814-112">Se producen muchos problemas cuando una sola empresa implementa varios directorios.</span><span class="sxs-lookup"><span data-stu-id="d9814-112">Many issues arise when a single enterprise deploys multiple directories.</span></span> <span data-ttu-id="d9814-113">Estos problemas incluyen la facilidad de uso, la coherencia de los datos, el costo de desarrollo y el costo de soporte técnico, entre otros.</span><span class="sxs-lookup"><span data-stu-id="d9814-113">These issues include usability, data consistency, development cost, and support cost, among others.</span></span>

<span data-ttu-id="d9814-114">Estos problemas se abordan en ADSI, en el que se proporciona un único conjunto de interfaces abierto y coherente que se puede usar para administrar y usar cualquier servicio de directorio que tenga un proveedor ADSI.</span><span class="sxs-lookup"><span data-stu-id="d9814-114">These issues are addressed in ADSI, in that there is provided a single, consistent, open set of interfaces that can be used for managing and using any directory service that has an ADSI provider.</span></span>

 

 




