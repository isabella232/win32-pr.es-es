---
title: Creación y optimización de GUID
description: Creación y optimización de GUID
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc113675bae329d862c0b504851d4732243a84c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419099"
---
# <a name="guid-creation-and-optimizations"></a><span data-ttu-id="02b1f-103">Creación y optimización de GUID</span><span class="sxs-lookup"><span data-stu-id="02b1f-103">GUID Creation and Optimizations</span></span>

<span data-ttu-id="02b1f-104">Dado que un CLSID, como un identificador de interfaz (IID), es un GUID, ninguna otra clase, independientemente de quién lo escribe, tiene un CLSID duplicado.</span><span class="sxs-lookup"><span data-stu-id="02b1f-104">Because a CLSID, like an interface identifier (IID), is a GUID, no other class, no matter who writes it, has a duplicate CLSID.</span></span> <span data-ttu-id="02b1f-105">Los implementadores de servidor generalmente obtienen CLSID a través de la función [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) .</span><span class="sxs-lookup"><span data-stu-id="02b1f-105">Server implementers generally obtain CLSIDs through the [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) function.</span></span> <span data-ttu-id="02b1f-106">Se garantiza que esta función genera CLSID únicos, de modo que los implementadores del servidor en todo el mundo pueden desarrollar e implementar de forma independiente su software sin miedo a colisiones accidentales con software escrito por otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="02b1f-106">This function is guaranteed to produce unique CLSIDs, so server implementers across the world can independently develop and deploy their software without fear of accidental collision with software written by others.</span></span>

<span data-ttu-id="02b1f-107">El uso de CLSID únicos evita la posibilidad de que se produzcan conflictos de nombres entre las clases, ya que los CLSID no se conectan a los nombres utilizados en la implementación subyacente.</span><span class="sxs-lookup"><span data-stu-id="02b1f-107">Using unique CLSIDs avoids the possibility of name collisions among classes because CLSIDs are in no way connected to the names used in the underlying implementation.</span></span> <span data-ttu-id="02b1f-108">Por ejemplo, dos proveedores diferentes pueden escribir clases denominadas "StackClass", pero cada una tendría un CLSID único y, por lo tanto, no se pudo confundir.</span><span class="sxs-lookup"><span data-stu-id="02b1f-108">For example, two different vendors can write classes called "StackClass," but each would have a unique CLSID and therefore could not be confused.</span></span>

<span data-ttu-id="02b1f-109">A menudo, COM debe asignar GUID (IID y CLSID) a un conjunto de otros valores arbitrariamente grande.</span><span class="sxs-lookup"><span data-stu-id="02b1f-109">COM frequently must map GUIDs (IIDs and CLSIDs) to some arbitrarily large set of other values.</span></span> <span data-ttu-id="02b1f-110">Como desarrollador de aplicaciones, puede ayudar a acelerar dichas búsquedas y, de este modo, mejorar el rendimiento del sistema mediante la generación de los GUID de la aplicación como un bloque de valores consecutivos.</span><span class="sxs-lookup"><span data-stu-id="02b1f-110">As an application developer, you can help speed up such searches, and thereby enhance system performance, by generating the GUIDs for your application as a block of consecutive values.</span></span>

<span data-ttu-id="02b1f-111">La manera más eficaz de generar un bloque de GUID consecutivos es ejecutar la utilidad uuidgen mediante los modificadores-n y-x, que genera un bloque de UUID, cada uno de los cuales se incrementa en uno.</span><span class="sxs-lookup"><span data-stu-id="02b1f-111">The most efficient way to generate a block of consecutive GUIDs is to run the uuidgen utility using the -n and -x switches, which generates a block of UUIDs, each of whose first DWORD value is incremented by one.</span></span>

<span data-ttu-id="02b1f-112">Por ejemplo, si fuera a escribir</span><span class="sxs-lookup"><span data-stu-id="02b1f-112">For example, if you were to type</span></span>

<span data-ttu-id="02b1f-113">**uuidgen-N5-x**</span><span class="sxs-lookup"><span data-stu-id="02b1f-113">**uuidgen -n5 -x**</span></span>

<span data-ttu-id="02b1f-114">la utilidad uuidgen generaría un bloque de UUID similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="02b1f-114">the uuidgen utility would generate a block of UUIDs similar to the following:</span></span>

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

<span data-ttu-id="02b1f-115">Un método para generar y realizar el seguimiento de los GUID para un proyecto completo comienza con la generación de un bloque de un número de UUID arbitrariamente grande, por ejemplo, 500.</span><span class="sxs-lookup"><span data-stu-id="02b1f-115">One method for generating and tracking GUIDs for an entire project begins with generating a block of some arbitrarily large number of UUIDs, say 500.</span></span> <span data-ttu-id="02b1f-116">Por ejemplo, si fuera a escribir</span><span class="sxs-lookup"><span data-stu-id="02b1f-116">For example, if you were to type</span></span>

<span data-ttu-id="02b1f-117">**uuidgen-N500-x > guids.txt**</span><span class="sxs-lookup"><span data-stu-id="02b1f-117">**uuidgen -n500 -x > guids.txt**</span></span>

<span data-ttu-id="02b1f-118">la utilidad generará 500 UUID consecutivos y los escribirá en el archivo de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="02b1f-118">the utility would generate 500 consecutive UUIDs and write them to the specified text file.</span></span> <span data-ttu-id="02b1f-119">A continuación, podría comprobar este archivo en el árbol de origen, lo que proporciona un único repositorio para todos los GUID que se usarán en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="02b1f-119">You could then check this file into your source tree, providing a single repository for all GUIDs to be used in a project.</span></span> <span data-ttu-id="02b1f-120">A medida que los usuarios requieren GUID para sus partes del proyecto, pueden desproteger el archivo, no usar muchos de los GUID que necesitan y marcarlos como tomados y dejar una nota sobre la ubicación en el código o "especificación" que los están usando.</span><span class="sxs-lookup"><span data-stu-id="02b1f-120">As people require GUIDs for their portions of the project, they can check out the file, take however many GUIDs they need, marking them as taken and leaving a note about where in the code or "spec" they are using them.</span></span>

<span data-ttu-id="02b1f-121">Además de mejorar el rendimiento del sistema, la generación de bloques de GUID consecutivos de esta manera presenta las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="02b1f-121">In addition to improving system performance, generating blocks of consecutive GUIDs in this way has the following benefits:</span></span>

-   <span data-ttu-id="02b1f-122">Un archivo central que contiene todos los GUID de una aplicación facilita el seguimiento de qué GUID son para qué y qué usuarios los están usando.</span><span class="sxs-lookup"><span data-stu-id="02b1f-122">A central file containing all GUIDs for an application makes it easy to keep track of which GUIDs are for what and which people are using them.</span></span>
-   <span data-ttu-id="02b1f-123">Un bloque de GUID consecutivos asociado a una aplicación concreta ayuda a los desarrolladores y evaluadores a reconocer GUID internos durante la depuración y facilita su búsqueda en el registro del sistema porque se almacenan secuencialmente.</span><span class="sxs-lookup"><span data-stu-id="02b1f-123">A block of consecutive GUIDs associated with a particular application helps developers and testers recognize internal GUIDs during debugging and makes it easier to find them in the system registry because they are stored sequentially.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02b1f-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02b1f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02b1f-125">Responsabilidades del servidor COM</span><span class="sxs-lookup"><span data-stu-id="02b1f-125">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 




