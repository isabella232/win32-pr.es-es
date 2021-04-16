---
description: El Servicio de instantáneas de volumen (VSS) es un conjunto de API de COM y C++ que permiten realizar copias de seguridad de volumen mientras las aplicaciones del sistema (denominadas escritores) continúan escribiendo en los volúmenes.
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: Referencia de la API de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8651c987c01ce67f1383f2ab1a24ca3fea8bbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541750"
---
# <a name="volume-shadow-copy-api-reference"></a><span data-ttu-id="8603e-103">Referencia de la API de instantáneas de volumen</span><span class="sxs-lookup"><span data-stu-id="8603e-103">Volume Shadow Copy API Reference</span></span>

<span data-ttu-id="8603e-104">El Servicio de instantáneas de volumen (VSS) es un conjunto de API de COM y C++ que permiten realizar copias de seguridad de volumen mientras las aplicaciones del sistema (denominadas escritores) continúan escribiendo en los volúmenes.</span><span class="sxs-lookup"><span data-stu-id="8603e-104">The Volume Shadow Copy Service (VSS) is a set of COM and C++ APIs that enable volume backups to be performed while applications on the system (called writers) continue to write to the volumes.</span></span>

<span data-ttu-id="8603e-105">VSS admite estas copias de seguridad a través de la creación de instantáneas, un duplicado del volumen original en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="8603e-105">VSS supports these backups through the creation of shadow copies, a duplicate of the original volume at a given point in time.</span></span>

<span data-ttu-id="8603e-106">Los desarrolladores de terceros pueden usar la API de VSS para crear solicitantes (por ejemplo, una aplicación de copia de seguridad) para crear y administrar instantáneas.</span><span class="sxs-lookup"><span data-stu-id="8603e-106">Third-party developers can use the VSS API to create requesters (such as a backup application) to create and manage shadow copies.</span></span>

<span data-ttu-id="8603e-107">Las aplicaciones de nivel de sistema conocidas como proveedores llevan a cabo el trabajo real de creación y representación de las instantáneas.</span><span class="sxs-lookup"><span data-stu-id="8603e-107">The actual work of creating and representing shadow copies is conducted by system-level applications known as providers.</span></span>

<span data-ttu-id="8603e-108">Los desarrolladores también pueden usar la API para construir escritores: aplicaciones compatibles con VSS que pueden coordinar las operaciones de e/s con la creación y manipulación de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="8603e-108">Developers can also use the API to construct writers: VSS-aware applications that are able to coordinate I/O operations with the creation and manipulation of shadow copies.</span></span>

-   [<span data-ttu-id="8603e-109">Clases de API de instantáneas de volumen</span><span class="sxs-lookup"><span data-stu-id="8603e-109">Volume Shadow Copy API Classes</span></span>](volume-shadow-copy-api-classes.md)
-   [<span data-ttu-id="8603e-110">Tipos de datos de la API de instantáneas de volumen</span><span class="sxs-lookup"><span data-stu-id="8603e-110">Volume Shadow Copy API Data Types</span></span>](volume-shadow-copy-api-data-types.md)
-   [<span data-ttu-id="8603e-111">Enumeraciones de la API de instantáneas de volumen</span><span class="sxs-lookup"><span data-stu-id="8603e-111">Volume Shadow Copy API Enumerations</span></span>](volume-shadow-copy-api-enumeration-types.md)
-   [<span data-ttu-id="8603e-112">Funciones de la API de instantáneas de volumen</span><span class="sxs-lookup"><span data-stu-id="8603e-112">Volume Shadow Copy API Functions</span></span>](volume-shadow-copy-api-functions.md)
-   [<span data-ttu-id="8603e-113">Interfaces de la API de instantáneas de volumen</span><span class="sxs-lookup"><span data-stu-id="8603e-113">Volume Shadow Copy API Interfaces</span></span>](volume-shadow-copy-api-interfaces.md)
-   [<span data-ttu-id="8603e-114">Estructuras de API de instantáneas de volumen</span><span class="sxs-lookup"><span data-stu-id="8603e-114">Volume Shadow Copy API Structures</span></span>](volume-shadow-copy-api-structures.md)
-   [<span data-ttu-id="8603e-115">Glosario de instantáneas de volumen</span><span class="sxs-lookup"><span data-stu-id="8603e-115">Volume Shadow Copy Glossary</span></span>](volume-shadow-copy-glossary.md)

<span data-ttu-id="8603e-116">Para obtener más información sobre la escritura de solicitantes y escritores, vea [usar el servicio de instantáneas de volumen](using-the-volume-shadow-copy-service.md).</span><span class="sxs-lookup"><span data-stu-id="8603e-116">For more information on writing requesters and writers, see [Using the Volume Shadow Copy Service](using-the-volume-shadow-copy-service.md).</span></span>

 

 



