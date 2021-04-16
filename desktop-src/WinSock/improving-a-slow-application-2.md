---
description: En esta sección se examina una parte de una aplicación de ejemplo que funciona a través de la red muy lentamente. En esta sección, se realizan modificaciones en el código inicial para mejorar su rendimiento.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Mejora de una aplicación lenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae5bbec57791155852a41b1413e0d863f8704c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705610"
---
# <a name="improving-a-slow-application"></a><span data-ttu-id="312f7-104">Mejora de una aplicación lenta</span><span class="sxs-lookup"><span data-stu-id="312f7-104">Improving a Slow Application</span></span>

<span data-ttu-id="312f7-105">En esta sección se examina una parte de una aplicación de ejemplo que funciona a través de la red muy lentamente.</span><span class="sxs-lookup"><span data-stu-id="312f7-105">This section examines a portion of a sample application that operates over the network very slowly.</span></span> <span data-ttu-id="312f7-106">En esta sección, se realizan modificaciones en el código inicial para mejorar su rendimiento.</span><span class="sxs-lookup"><span data-stu-id="312f7-106">Throughout this section, modifications are made to the initial code to improve its performance.</span></span>

<span data-ttu-id="312f7-107">El ejemplo ficticio es la parte actualizada para un juego denominado Life.</span><span class="sxs-lookup"><span data-stu-id="312f7-107">The mock sample is the updated portion for a game called Life.</span></span> <span data-ttu-id="312f7-108">La aplicación se escribe de forma que el cliente realiza los cálculos de las actualizaciones y las envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="312f7-108">The application is written such that the client performs the calculations for the updates and sends them to the server.</span></span> <span data-ttu-id="312f7-109">A continuación, el servidor muestra el campo de vida resultante.</span><span class="sxs-lookup"><span data-stu-id="312f7-109">The server then displays the resulting Life field.</span></span> <span data-ttu-id="312f7-110">La salida del cliente es un flujo de bytes, agrupados en tres (triples), cada triple representa una actualización de celda.</span><span class="sxs-lookup"><span data-stu-id="312f7-110">The output from the client is a stream of bytes, grouped in threes (triplets), each triplet representing one cell update.</span></span> <span data-ttu-id="312f7-111">Los bytes del triple representan la fila, la columna y el valor respectivamente para la celda.</span><span class="sxs-lookup"><span data-stu-id="312f7-111">The bytes in the triplet represent the row, column, and value, respectively, for the cell.</span></span>

<span data-ttu-id="312f7-112">Este ejemplo comienza como una aplicación intencionadamente deficiente, que proporciona la línea base de la que se pueden ilustrar las mejoras de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="312f7-112">This sample begins as an intentionally poor performing application, which provides the baseline from which performance improvements can be illustrated.</span></span> <span data-ttu-id="312f7-113">A partir de ahí, el código se mejora tres veces para solucionar diversos problemas que afectan al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="312f7-113">From there, the code is improved three times to address various issues that affect performance.</span></span> <span data-ttu-id="312f7-114">Estos ejemplos se deben leer en orden, ya que cada iteración mejora en la versión anterior.</span><span class="sxs-lookup"><span data-stu-id="312f7-114">These samples should be read in order, as each iteration improves on the previous version.</span></span>

<span data-ttu-id="312f7-115">El código de línea base y las revisiones que mejoran ese código son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="312f7-115">The baseline code, and the revisions that improve that code, are the following:</span></span>

-   [<span data-ttu-id="312f7-116">La versión de línea base: una aplicación con un rendimiento muy deficiente</span><span class="sxs-lookup"><span data-stu-id="312f7-116">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
-   [<span data-ttu-id="312f7-117">Revisión 1: limpieza del manifiesto</span><span class="sxs-lookup"><span data-stu-id="312f7-117">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
-   [<span data-ttu-id="312f7-118">Revisión 2: rediseño para menos conexiones</span><span class="sxs-lookup"><span data-stu-id="312f7-118">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
-   [<span data-ttu-id="312f7-119">Revisión 3: envío de bloque comprimido</span><span class="sxs-lookup"><span data-stu-id="312f7-119">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
-   [<span data-ttu-id="312f7-120">Mejoras futuras</span><span class="sxs-lookup"><span data-stu-id="312f7-120">Future Improvements</span></span>](future-improvements-2.md)

> [!WARNING]
> <span data-ttu-id="312f7-121">Los primeros ejemplos de la aplicación proporcionan un rendimiento insuficiente intencionadamente, con el fin de mostrar las mejoras de rendimiento posibles con los cambios en el código.</span><span class="sxs-lookup"><span data-stu-id="312f7-121">The first few examples of the application provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="312f7-122">No use estos ejemplos de código en la aplicación; solo tienen fines ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="312f7-122">Do not use these code samples in your application; they are for illustration purposes only.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="312f7-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="312f7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="312f7-124">Aplicaciones de Windows Sockets de alto rendimiento</span><span class="sxs-lookup"><span data-stu-id="312f7-124">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



