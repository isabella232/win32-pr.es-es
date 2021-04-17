---
description: Managed Object Format (MOF) es el lenguaje que se usa para describir las clases de Modelo de información común (CIM).
ms.assetid: 26494142-2078-4d46-a794-e43973255c2d
ms.tgt_platform: multiple
title: Managed Object Format (MOF)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16f95c6868943a2f41c4326c341207ff26a03af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697540"
---
# <a name="managed-object-format-mof"></a><span data-ttu-id="cd94c-103">Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="cd94c-103">Managed Object Format (MOF)</span></span>

<span data-ttu-id="cd94c-104">Managed Object Format (MOF) es el lenguaje que se usa para describir las clases de [*modelo de información común (CIM)*](gloss-c.md) .</span><span class="sxs-lookup"><span data-stu-id="cd94c-104">Managed Object Format (MOF) is the language used to describe [*Common Information Model (CIM)*](gloss-c.md) classes.</span></span>

<span data-ttu-id="cd94c-105">La manera recomendada para que los proveedores de WMI implementen nuevas clases WMI es en archivos MOF que se compilan mediante [**Mofcomp.exe**](mofcomp.md) en el [*repositorio WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="cd94c-105">The recommended way for WMI providers to implement new WMI classes is in MOF files which are compiled using [**Mofcomp.exe**](mofcomp.md) into the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="cd94c-106">También es posible crear y manipular clases CIM e instancias mediante la [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="cd94c-106">It is also possible to create and manipulate CIM classes and instances using the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="cd94c-107">Un proveedor WMI normalmente consta de un archivo MOF, que define los datos y las clases de eventos para los que el proveedor devuelve datos, y un archivo DLL que contiene el código que proporciona los datos.</span><span class="sxs-lookup"><span data-stu-id="cd94c-107">A WMI provider normally consists of a MOF file, which defines the data and event classes for which the provider returns data, and a DLL file which contains the code that supplies data.</span></span> <span data-ttu-id="cd94c-108">Para obtener más información, consulte [proporcionar datos a WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="cd94c-108">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="cd94c-109">Las aplicaciones y scripts de cliente WMI pueden consultar instancias de clases MOF de proveedor o suscribirse para recibir notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="cd94c-109">WMI client scripts and applications can query for instances of provider MOF classes or subscribe to receive event notifications.</span></span>

<span data-ttu-id="cd94c-110">Puede realizar las siguientes tareas con MOF:</span><span class="sxs-lookup"><span data-stu-id="cd94c-110">You can perform the following tasks with MOF:</span></span>

-   [<span data-ttu-id="cd94c-111">Compilar archivos MOF</span><span class="sxs-lookup"><span data-stu-id="cd94c-111">Compiling MOF Files</span></span>](compiling-mof-files.md)
-   [<span data-ttu-id="cd94c-112">Crear una clase</span><span class="sxs-lookup"><span data-stu-id="cd94c-112">Creating a Class</span></span>](creating-a-class.md)
-   [<span data-ttu-id="cd94c-113">Crear una instancia</span><span class="sxs-lookup"><span data-stu-id="cd94c-113">Creating an Instance</span></span>](creating-an-instance.md)
-   [<span data-ttu-id="cd94c-114">Crear un método</span><span class="sxs-lookup"><span data-stu-id="cd94c-114">Creating a Method</span></span>](creating-a-method.md)
-   [<span data-ttu-id="cd94c-115">Adición de un calificador</span><span class="sxs-lookup"><span data-stu-id="cd94c-115">Adding a Qualifier</span></span>](adding-a-qualifier.md)
-   [<span data-ttu-id="cd94c-116">Crear un comentario</span><span class="sxs-lookup"><span data-stu-id="cd94c-116">Creating a Comment</span></span>](creating-a-comment.md)

## <a name="related-topics"></a><span data-ttu-id="cd94c-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd94c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd94c-118">Acerca de WMI</span><span class="sxs-lookup"><span data-stu-id="cd94c-118">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 



