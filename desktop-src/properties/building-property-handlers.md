---
description: En Windows Vista y versiones posteriores, los metadatos se convierten en centrales como un método para organizar elementos como archivos, correo electrónico o contactos.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementar controladores de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcef615ce1ebb5041d79dd9c6ccf8cf129d189aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277823"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="3b0db-103">Implementar controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="3b0db-103">Implementing Property Handlers</span></span>

<span data-ttu-id="3b0db-104">En Windows Vista y versiones posteriores, los metadatos se convierten en centrales como un método para organizar elementos como archivos, correo electrónico o contactos.</span><span class="sxs-lookup"><span data-stu-id="3b0db-104">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="3b0db-105">Para habilitar un sistema en el que se puedan buscar elementos en función de sus metadatos y de que los usuarios puedan leer o escribir esos metadatos, Windows Vista presentó un nuevo sistema de propiedades.</span><span class="sxs-lookup"><span data-stu-id="3b0db-105">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="3b0db-106">Los metadatos de este sistema se representan mediante un conjunto extensible de propiedades.</span><span class="sxs-lookup"><span data-stu-id="3b0db-106">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="3b0db-107">En este conjunto de temas se describe cómo se puede crear un controlador que lea y escriba propiedades en una secuencia de archivo.</span><span class="sxs-lookup"><span data-stu-id="3b0db-107">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="3b0db-108">Estos controladores se denominan controladores de propiedades y cada uno está asociado a un tipo de archivo determinado, identificado por la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="3b0db-108">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="3b0db-109">En los temas siguientes se describen los requisitos y las estrategias que conlleva la definición de las propiedades y los controladores de propiedades.</span><span class="sxs-lookup"><span data-stu-id="3b0db-109">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="3b0db-110">Descripción de los controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="3b0db-110">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="3b0db-111">Usar nombres de tipo</span><span class="sxs-lookup"><span data-stu-id="3b0db-111">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="3b0db-112">Usar listas de propiedades</span><span class="sxs-lookup"><span data-stu-id="3b0db-112">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="3b0db-113">Inicializar controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="3b0db-113">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="3b0db-114">Registrar y distribuir controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="3b0db-114">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="3b0db-115">Prácticas recomendadas y preguntas más frecuentes sobre controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="3b0db-115">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)

## <a name="related-topics"></a><span data-ttu-id="3b0db-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b0db-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b0db-117">Crear propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="3b0db-117">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="3b0db-118">Esquema de descripción de propiedad</span><span class="sxs-lookup"><span data-stu-id="3b0db-118">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
