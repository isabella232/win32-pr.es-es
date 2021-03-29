---
title: Ventajas del almacenamiento estructurado
description: COM proporciona un conjunto de servicios denominados colectivamente almacenamiento estructurado.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- Strctd de almacenamiento estructurado STG, ventajas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68b954fda33e18f654ccc0360f58ddb14e5d110
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773746"
---
# <a name="benefits-of-structured-storage"></a><span data-ttu-id="0dde6-104">Ventajas del almacenamiento estructurado</span><span class="sxs-lookup"><span data-stu-id="0dde6-104">Benefits of Structured Storage</span></span>

<span data-ttu-id="0dde6-105">COM proporciona un conjunto de servicios denominados colectivamente almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="0dde6-105">COM provides a set of services collectively called structured storage.</span></span> <span data-ttu-id="0dde6-106">Entre las ventajas de estos servicios se reduce la reducción del rendimiento y la sobrecarga asociada al almacenamiento de objetos independientes en un archivo plano.</span><span class="sxs-lookup"><span data-stu-id="0dde6-106">Among the benefits of these services is the reduction of performance penalties and overhead associated with storing separate objects in a flat file.</span></span> <span data-ttu-id="0dde6-107">En lugar de un archivo sin formato, COM almacena los objetos independientes en un único archivo estructurado que consta de dos elementos principales: objetos de almacenamiento y objetos de secuencia.</span><span class="sxs-lookup"><span data-stu-id="0dde6-107">Instead of a flat file, COM stores the separate objects in a single, structured file consisting of two main elements: storage objects and stream objects.</span></span> <span data-ttu-id="0dde6-108">Juntos, funcionan como un sistema de archivos dentro de un archivo.</span><span class="sxs-lookup"><span data-stu-id="0dde6-108">Together, they function like a file system within a file.</span></span>

<span data-ttu-id="0dde6-109">El almacenamiento estructurado resuelve los problemas de rendimiento al eliminar la necesidad de reescribir completamente un archivo en el almacenamiento cada vez que se agrega un nuevo objeto a un archivo compuesto, o cuando un objeto existente aumenta de tamaño.</span><span class="sxs-lookup"><span data-stu-id="0dde6-109">Structured storage solves performance problems by eliminating the need to totally rewrite a file to storage whenever a new object is added to a compound file, or an existing object increases in size.</span></span> <span data-ttu-id="0dde6-110">Los nuevos datos se escriben en la siguiente ubicación disponible en el almacenamiento permanente y el objeto de almacenamiento actualiza la tabla de punteros que mantiene para realizar el seguimiento de las ubicaciones de sus objetos de almacenamiento y objetos de secuencia.</span><span class="sxs-lookup"><span data-stu-id="0dde6-110">The new data is written to the next available location in permanent storage, and the storage object updates the table of pointers it maintains to track the locations of its storage objects and stream objects.</span></span> <span data-ttu-id="0dde6-111">Al mismo tiempo, el almacenamiento estructurado permite a los usuarios finales interactuar y administrar un archivo compuesto como si fuera un único archivo en lugar de una jerarquía anidada de objetos independientes.</span><span class="sxs-lookup"><span data-stu-id="0dde6-111">At the same time, structured storage enables end users to interact and manage a compound file as if it were a single file rather than a nested hierarchy of separate objects.</span></span>

<span data-ttu-id="0dde6-112">El almacenamiento estructurado también tiene otras ventajas:</span><span class="sxs-lookup"><span data-stu-id="0dde6-112">Structured storage also has other benefits:</span></span>

-   <span data-ttu-id="0dde6-113">**Acceso incremental**.</span><span class="sxs-lookup"><span data-stu-id="0dde6-113">**Incremental access**.</span></span> <span data-ttu-id="0dde6-114">Si un usuario necesita tener acceso a un objeto dentro de un archivo compuesto, el usuario puede cargar y guardar solo ese objeto, en lugar de todo el archivo.</span><span class="sxs-lookup"><span data-stu-id="0dde6-114">If a user needs access to an object within a compound file, the user can load and save only that object, rather than the entire file.</span></span>
-   <span data-ttu-id="0dde6-115">**Uso múltiple**.</span><span class="sxs-lookup"><span data-stu-id="0dde6-115">**Multiple use**.</span></span> <span data-ttu-id="0dde6-116">Más de un usuario final o una aplicación pueden leer y escribir información simultáneamente en el mismo archivo compuesto.</span><span class="sxs-lookup"><span data-stu-id="0dde6-116">More than one end user or application can concurrently read and write information in the same compound file.</span></span>
-   <span data-ttu-id="0dde6-117">**Procesamiento de transacciones**.</span><span class="sxs-lookup"><span data-stu-id="0dde6-117">**Transaction processing**.</span></span> <span data-ttu-id="0dde6-118">Los usuarios pueden leer o escribir en archivos compuestos COM en modo de transacción, donde los cambios realizados en el archivo se almacenan en búfer y, posteriormente, pueden confirmarse en el archivo o invertirse.</span><span class="sxs-lookup"><span data-stu-id="0dde6-118">Users can read or write to COM compound files in transacted mode, where changes made to the file are buffered and can subsequently either be committed to the file or reversed.</span></span>
-   <span data-ttu-id="0dde6-119">**Ahorro de memoria insuficiente**.</span><span class="sxs-lookup"><span data-stu-id="0dde6-119">**Low-memory saves**.</span></span> <span data-ttu-id="0dde6-120">El almacenamiento estructurado proporciona funciones para guardar archivos en situaciones de memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="0dde6-120">Structured storage provides facilities for saving files in low-memory situations.</span></span>

 

 




