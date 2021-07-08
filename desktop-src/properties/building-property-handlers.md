---
description: Obtenga información sobre cómo crear un controlador de propiedades que lee y escribe propiedades en y desde una secuencia de archivos. Cada controlador está asociado a un tipo de archivo determinado.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementar controladores de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aadfabf451d5a90ba88925d28f3f460aaeeb28f
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481840"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="b95c4-104">Implementar controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="b95c4-104">Implementing Property Handlers</span></span>

<span data-ttu-id="b95c4-105">En Windows Vista y versiones posteriores, los metadatos se convierten en fundamentales como método para organizar elementos como archivos, correo electrónico o contactos.</span><span class="sxs-lookup"><span data-stu-id="b95c4-105">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="b95c4-106">Para habilitar un sistema en el que se pueden buscar elementos en función de sus metadatos y en el que los usuarios puedan leer o escribir los metadatos, Windows Vista introdujo un nuevo sistema de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b95c4-106">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="b95c4-107">Los metadatos de este sistema se representan mediante un conjunto extensible de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b95c4-107">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="b95c4-108">En este conjunto de temas se describe cómo puede crear un controlador que lee y escribe propiedades en y desde una secuencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="b95c4-108">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="b95c4-109">Estos controladores se denominan controladores de propiedades y cada uno de ellos está asociado a tipos de archivo determinados, identificados por la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="b95c4-109">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="b95c4-110">En los temas siguientes se tratan los requisitos y las estrategias implicados en la definición de las propiedades y los controladores de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b95c4-110">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="b95c4-111">Descripción de los controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="b95c4-111">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="b95c4-112">Usar nombres de tipo</span><span class="sxs-lookup"><span data-stu-id="b95c4-112">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="b95c4-113">Usar listas de propiedades</span><span class="sxs-lookup"><span data-stu-id="b95c4-113">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="b95c4-114">Inicialización de controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="b95c4-114">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="b95c4-115">Registro y distribución de controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="b95c4-115">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="b95c4-116">Procedimientos recomendados y preguntas más frecuentes sobre el controlador de propiedades</span><span class="sxs-lookup"><span data-stu-id="b95c4-116">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.yml)

## <a name="related-topics"></a><span data-ttu-id="b95c4-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b95c4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b95c4-118">Crear propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="b95c4-118">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="b95c4-119">Esquema de descripción de propiedad</span><span class="sxs-lookup"><span data-stu-id="b95c4-119">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
