---
description: Obtenga información sobre la sintaxis del esquema de impresión, que se expresa en sintaxis XML y se compone de un pequeño número de tipos de elementos.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Sintaxis del esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef52dbdbdfacc2d3cc947b46558319577a75b1b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405298"
---
# <a name="syntax-of-the-print-schema"></a><span data-ttu-id="e8ee0-103">Sintaxis del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e8ee0-103">Syntax of the Print Schema</span></span>

<span data-ttu-id="e8ee0-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="e8ee0-104">This topic is not current.</span></span> <span data-ttu-id="e8ee0-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e8ee0-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e8ee0-106">El esquema de impresión se expresa en sintaxis XML.</span><span class="sxs-lookup"><span data-stu-id="e8ee0-106">The Print Schema is expressed in XML syntax.</span></span> <span data-ttu-id="e8ee0-107">Por lo tanto, se espera que los lectores estén familiarizados con la sintaxis y los términos XML, como el elemento, la etiqueta de elemento, el contenido del elemento, el atributo y el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="e8ee0-107">Readers are therefore expected to be familiar with XML syntax and terms such as element, element tag, element content, attribute, and namespace.</span></span> <span data-ttu-id="e8ee0-108">El marco de esquema de impresión se compone de un pequeño número de tipos de elementos; Cada tipo de elemento tiene un propósito específico en las tecnologías creadas en el esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="e8ee0-108">The Print Schema Framework is composed of a small number of element types; each element type serves a specific purpose in the technologies built on the Print Schema.</span></span>

<span data-ttu-id="e8ee0-109">Los tipos de elemento se distinguen por su etiqueta de elemento XML.</span><span class="sxs-lookup"><span data-stu-id="e8ee0-109">Element types are distinguished by their XML element tag.</span></span> <span data-ttu-id="e8ee0-110">Print Schema Framework define la estructura general y la organización de las tecnologías dependientes, indicando para cada tipo de elemento qué tipos de elemento se permiten como elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="e8ee0-110">The Print Schema Framework defines the overall structure and organization of the dependent technologies, by denoting for each element type which element types are allowed as child elements.</span></span>

<span data-ttu-id="e8ee0-111">Muchos tipos de elementos se diferencian de otros del mismo tipo por el atributo name, que desempeña un papel importante en el esquema.</span><span class="sxs-lookup"><span data-stu-id="e8ee0-111">Many element types are differentiated from others of the same type by the name attribute, which plays a significant role in the schema.</span></span> <span data-ttu-id="e8ee0-112">El atributo name sirve para identificar instancias de cada tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="e8ee0-112">The name attribute serves to identify instances of each element type.</span></span> <span data-ttu-id="e8ee0-113">Las palabras clave de esquema de impresión definen un conjunto de valores para el atributo name para muchos de los tipos de elemento.</span><span class="sxs-lookup"><span data-stu-id="e8ee0-113">The Print Schema Keywords defines a set of values for the name attribute for many of the element types.</span></span> <span data-ttu-id="e8ee0-114">En la mayoría de los casos, los proveedores pueden asignar sus propios valores al atributo name.</span><span class="sxs-lookup"><span data-stu-id="e8ee0-114">In most cases, providers can assign their own values to the name attribute.</span></span> <span data-ttu-id="e8ee0-115">Solo necesitan asegurarse de que los valores son QName XML calificados con un espacio de nombres que es único para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="e8ee0-115">They need only ensure the values are XML QNames qualified with a namespace that is unique to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8ee0-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8ee0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8ee0-117">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e8ee0-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



