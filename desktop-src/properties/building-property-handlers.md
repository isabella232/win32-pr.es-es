---
description: Obtenga información sobre cómo crear un controlador de propiedades que lee y escribe propiedades en y desde una secuencia de archivos. Cada controlador está asociado a un tipo de archivo determinado.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementar controladores de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf37ae37e43ce14cf69bec44e7f210b32373d38e
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989270"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="22c28-104">Implementar controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="22c28-104">Implementing Property Handlers</span></span>

<span data-ttu-id="22c28-105">En Windows Vista y versiones posteriores, los metadatos se convierten en fundamentales como un método para organizar elementos como archivos, correo electrónico o contactos.</span><span class="sxs-lookup"><span data-stu-id="22c28-105">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="22c28-106">Para habilitar un sistema en el que se puedan buscar elementos en función de sus metadatos y donde los usuarios puedan leer o escribir los metadatos, Windows Vista introdujo un nuevo sistema de propiedades.</span><span class="sxs-lookup"><span data-stu-id="22c28-106">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="22c28-107">Los metadatos de este sistema se representan mediante un conjunto extensible de propiedades.</span><span class="sxs-lookup"><span data-stu-id="22c28-107">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="22c28-108">En este conjunto de temas se describe cómo se puede crear un controlador que lee y escribe propiedades en y desde una secuencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="22c28-108">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="22c28-109">Estos controladores se denominan controladores de propiedades y cada uno de ellos está asociado a tipos de archivo determinados, identificados por la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="22c28-109">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="22c28-110">En los temas siguientes se tratan los requisitos y las estrategias implicados en la definición de las propiedades y los controladores de propiedades.</span><span class="sxs-lookup"><span data-stu-id="22c28-110">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="22c28-111">Descripción de los controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="22c28-111">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="22c28-112">Usar nombres de tipo</span><span class="sxs-lookup"><span data-stu-id="22c28-112">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="22c28-113">Usar listas de propiedades</span><span class="sxs-lookup"><span data-stu-id="22c28-113">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="22c28-114">Inicialización de controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="22c28-114">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="22c28-115">Registro y distribución de controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="22c28-115">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="22c28-116">Procedimientos recomendados y preguntas más frecuentes sobre el controlador de propiedades</span><span class="sxs-lookup"><span data-stu-id="22c28-116">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)

## <a name="related-topics"></a><span data-ttu-id="22c28-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22c28-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22c28-118">Crear propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="22c28-118">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="22c28-119">Esquema de descripción de propiedad</span><span class="sxs-lookup"><span data-stu-id="22c28-119">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
