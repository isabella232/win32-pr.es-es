---
description: Una nueva característica interesante de Tablet PC es el sistema de entrada manuscrita.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Entrada de lápiz, tinta y reconocimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d865e40d1779edaa2607b1754c45659609b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558862"
---
# <a name="pen-input-ink-and-recognition"></a><span data-ttu-id="7fa2d-103">Entrada de lápiz, tinta y reconocimiento</span><span class="sxs-lookup"><span data-stu-id="7fa2d-103">Pen Input, Ink, and Recognition</span></span>

<span data-ttu-id="7fa2d-104">Una nueva característica interesante de Tablet PC es el sistema de entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="7fa2d-104">One interesting new feature of Tablet PC is the pen input system.</span></span> <span data-ttu-id="7fa2d-105">Todos los equipos de Tablet PC tienen un digitalizador debajo de la pantalla que acepta entradas manuscritas.</span><span class="sxs-lookup"><span data-stu-id="7fa2d-105">All Tablet PC computers have a digitizer beneath the screen that accepts pen input.</span></span> <span data-ttu-id="7fa2d-106">Este nuevo mecanismo de entrada requiere que piense en cómo crear aplicaciones específicamente para Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="7fa2d-106">This new input mechanism requires you to think about how to build applications specifically for Tablet PC.</span></span> <span data-ttu-id="7fa2d-107">La interfaz de programación de aplicaciones (API) de la plataforma de Tablet PC le ayuda a hacerlo.</span><span class="sxs-lookup"><span data-stu-id="7fa2d-107">The Tablet PC platform application programming interface (API) helps you do this.</span></span>

## <a name="collection-data-management-and-recognition"></a><span data-ttu-id="7fa2d-108">Recopilación, Administración de datos y reconocimiento</span><span class="sxs-lookup"><span data-stu-id="7fa2d-108">Collection, Data Management, and Recognition</span></span>

<span data-ttu-id="7fa2d-109">La plataforma de Tablet PC se puede dividir en tres áreas distintas:</span><span class="sxs-lookup"><span data-stu-id="7fa2d-109">The Tablet PC platform can be divided into three distinct areas:</span></span>

-   <span data-ttu-id="7fa2d-110">Colección de entradas manuscritas (objetos que se usan para recopilar entradas manuscritas del digitalizador).</span><span class="sxs-lookup"><span data-stu-id="7fa2d-110">Ink collection (objects that are used to collect ink from the digitizer).</span></span>
-   <span data-ttu-id="7fa2d-111">Administración de datos de tinta (objetos que se usan para administrar la entrada de lápiz recopilada).</span><span class="sxs-lookup"><span data-stu-id="7fa2d-111">Ink data management (objects that are used to manage the collected ink).</span></span>
-   <span data-ttu-id="7fa2d-112">Reconocimiento de entradas manuscritas (objetos que se usan para convertir la entrada manuscrita recopilada en otros tipos de datos, como texto).</span><span class="sxs-lookup"><span data-stu-id="7fa2d-112">Ink recognition (objects that are used to convert the collected ink into other types of data, such as text).</span></span>

<span data-ttu-id="7fa2d-113">En la siguiente imagen se muestra, en un nivel alto, cómo la API de recopilación de tintas (lápiz API), la API de Ink Administración de datos (API de tinta) y la API de reconocimiento de tinta (API de reconocimiento) funcionan en conjunto en la plataforma de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="7fa2d-113">The following image shows, at a high level, how the Ink Collection API (Pen API), Ink Data Management API (Ink API), and Ink Recognition API (Recognition API) work together in the Tablet PC platform.</span></span>

![Ilustración que muestra cómo la API de lápiz, la API de tinta y la API de reconocimiento funcionan juntas](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

<span data-ttu-id="7fa2d-115">La API de la plataforma de Tablet PC está disponible en las API administradas y en una biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="7fa2d-115">The Tablet PC platform API is available in Managed APIs as well as a COM library.</span></span> <span data-ttu-id="7fa2d-116">En los temas siguientes se describen los objetos de la API y se ilustra cómo usan estos objetos:</span><span class="sxs-lookup"><span data-stu-id="7fa2d-116">The following topics describe the objects in the API and illustrate how applications use these objects:</span></span>

-   [<span data-ttu-id="7fa2d-117">Colección de entradas manuscritas</span><span class="sxs-lookup"><span data-stu-id="7fa2d-117">Ink Collection</span></span>](ink-collection.md)
-   [<span data-ttu-id="7fa2d-118">Datos de tinta</span><span class="sxs-lookup"><span data-stu-id="7fa2d-118">Ink Data</span></span>](ink-data.md)
-   [<span data-ttu-id="7fa2d-119">Reconocimiento de tinta</span><span class="sxs-lookup"><span data-stu-id="7fa2d-119">Ink Recognition</span></span>](ink-recognition.md)
-   [<span data-ttu-id="7fa2d-120">Análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="7fa2d-120">Ink Analysis</span></span>](ink-analysis.md)
-   [<span data-ttu-id="7fa2d-121">Reconocimiento de escritura a mano en Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7fa2d-121">Handwriting Recognition in Windows Server 2008 R2</span></span>](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



