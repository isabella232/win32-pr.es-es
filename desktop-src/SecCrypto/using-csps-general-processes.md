---
description: Al usar los CSP de proveedores de servicios criptográficos, tenga en cuenta las siguientes convenciones.
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 'Uso de CSP: procesos generales'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f067ef0e3cd837b1b347daac3e3da21543047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687076"
---
# <a name="using-csps-general-processes"></a><span data-ttu-id="1613e-103">Uso de CSP: procesos generales</span><span class="sxs-lookup"><span data-stu-id="1613e-103">Using CSPs: General Processes</span></span>

<span data-ttu-id="1613e-104">Al usar los CSP de [*proveedores de servicios criptográficos*](../secgloss/c-gly.md) , tenga en cuenta las siguientes convenciones.</span><span class="sxs-lookup"><span data-stu-id="1613e-104">When using [*cryptographic service providers*](../secgloss/c-gly.md) CSPs, keep the following conventions in mind.</span></span>

## <a name="private-key-caching"></a><span data-ttu-id="1613e-105">Almacenamiento en caché de clave privada</span><span class="sxs-lookup"><span data-stu-id="1613e-105">Private Key Caching</span></span>

<span data-ttu-id="1613e-106">Un CSP puede almacenar en caché algunas [*claves privadas*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1613e-106">A CSP can cache some [*private keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="1613e-107">Es posible controlar este almacenamiento en caché de clave privada de forma global, pero no es específico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1613e-107">It is possible to control this private key caching on a global, but not an application-specific, basis.</span></span> <span data-ttu-id="1613e-108">El almacenamiento en caché de los cambios se realiza modificando ciertos valores del registro.</span><span class="sxs-lookup"><span data-stu-id="1613e-108">Caching changes are made by modifying certain registry settings.</span></span> <span data-ttu-id="1613e-109">Para obtener más información, vea [**constantes de almacenamiento en caché de clave privada**](private-key-caching-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1613e-109">For more information, see [**Private Key Caching Constants**](private-key-caching-constants.md).</span></span>

## <a name="example-code-conventions"></a><span data-ttu-id="1613e-110">Convenciones de código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="1613e-110">Example Code Conventions</span></span>

<span data-ttu-id="1613e-111">Para proporcionar un código más conciso y más legible, algunos de los principios de prácticas recomendadas de programación no siempre se siguen en los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="1613e-111">To provide more concise, more readable code, some principles of good programming practice are not always followed in the examples.</span></span> <span data-ttu-id="1613e-112">En concreto:</span><span class="sxs-lookup"><span data-stu-id="1613e-112">In particular:</span></span>

-   <span data-ttu-id="1613e-113">Solo se muestran las respuestas de error limitadas.</span><span class="sxs-lookup"><span data-stu-id="1613e-113">Only limited error responses are shown.</span></span> <span data-ttu-id="1613e-114">Los programas completos y bien escritos comprueban los códigos de error devueltos y realizan las acciones adecuadas cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="1613e-114">Well-written, complete programs check returned error codes and perform appropriate actions when an error is encountered.</span></span>
-   <span data-ttu-id="1613e-115">Solo se lleva a cabo la administración de memoria y recursos limitados.</span><span class="sxs-lookup"><span data-stu-id="1613e-115">Only limited memory and resource management is done.</span></span> <span data-ttu-id="1613e-116">Programas completos y escritos destruyen todas las claves y [*algoritmos hash*](../secgloss/h-gly.md), liberan toda la memoria asignada, cierran todos los archivos y liberan todos los identificadores.</span><span class="sxs-lookup"><span data-stu-id="1613e-116">Well-written, complete programs destroy all keys and [*hashes*](../secgloss/h-gly.md), free all allocated memory, close all files, and release all handles.</span></span> <span data-ttu-id="1613e-117">En estos ejemplos solo se proporcionan demostraciones limitadas del uso de funciones que realizan estas tareas.</span><span class="sxs-lookup"><span data-stu-id="1613e-117">These examples provide only limited demonstrations of the use of functions that perform these tasks.</span></span> <span data-ttu-id="1613e-118">En estos ejemplos no se realiza ninguna tarea de administración de recursos ni memoria en el caso de la finalización del programa debido a errores.</span><span class="sxs-lookup"><span data-stu-id="1613e-118">These examples perform no memory or resource management tasks in the case of program termination due to errors.</span></span>

<span data-ttu-id="1613e-119">Los temas siguientes presentan información general sobre los ejemplos de procedimientos y el código de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1613e-119">The following topics present general information about procedure examples as well as sample code.</span></span>

-   [<span data-ttu-id="1613e-120">Recuperación de datos de longitud desconocida</span><span class="sxs-lookup"><span data-stu-id="1613e-120">Retrieving Data of Unknown Length</span></span>](retrieving-data-of-unknown-length.md)
-   [<span data-ttu-id="1613e-121">Enumerar protocolos admitidos</span><span class="sxs-lookup"><span data-stu-id="1613e-121">Enumerating Supported Protocols</span></span>](enumerating-supported-protocols.md)

 

 
