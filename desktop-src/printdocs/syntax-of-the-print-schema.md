---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Sintaxis del esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2503b3f44ff8b4bdda41f0feefe374c27d78bd41
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105698022"
---
# <a name="syntax-of-the-print-schema"></a><span data-ttu-id="cac18-104">Sintaxis del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="cac18-104">Syntax of the Print Schema</span></span>

<span data-ttu-id="cac18-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="cac18-105">This topic is not current.</span></span> <span data-ttu-id="cac18-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cac18-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cac18-107">El esquema de impresión se expresa en sintaxis XML.</span><span class="sxs-lookup"><span data-stu-id="cac18-107">The Print Schema is expressed in XML syntax.</span></span> <span data-ttu-id="cac18-108">Por tanto, se espera que los lectores estén familiarizados con la sintaxis XML y con términos como elemento, etiqueta de elemento, contenido de elemento, atributo y espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="cac18-108">Readers are therefore expected to be familiar with XML syntax and terms such as element, element tag, element content, attribute, and namespace.</span></span> <span data-ttu-id="cac18-109">El marco de trabajo del esquema de impresión se compone de un número pequeño de tipos de elemento. cada tipo de elemento sirve a un propósito específico en las tecnologías basadas en el esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="cac18-109">The Print Schema Framework is composed of a small number of element types; each element type serves a specific purpose in the technologies built on the Print Schema.</span></span>

<span data-ttu-id="cac18-110">Los tipos de elemento se distinguen por su etiqueta de elemento XML.</span><span class="sxs-lookup"><span data-stu-id="cac18-110">Element types are distinguished by their XML element tag.</span></span> <span data-ttu-id="cac18-111">El marco de trabajo del esquema de impresión define la estructura global y la organización de las tecnologías dependientes, indicando para cada tipo de elemento qué tipos de elemento se permiten como elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="cac18-111">The Print Schema Framework defines the overall structure and organization of the dependent technologies, by denoting for each element type which element types are allowed as child elements.</span></span>

<span data-ttu-id="cac18-112">Muchos tipos de elementos se diferencian de otros del mismo tipo por el atributo name, que desempeña un rol significativo en el esquema.</span><span class="sxs-lookup"><span data-stu-id="cac18-112">Many element types are differentiated from others of the same type by the name attribute, which plays a significant role in the schema.</span></span> <span data-ttu-id="cac18-113">El atributo name sirve para identificar las instancias de cada tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="cac18-113">The name attribute serves to identify instances of each element type.</span></span> <span data-ttu-id="cac18-114">Las palabras clave de esquema de impresión definen un conjunto de valores para el atributo de nombre para muchos de los tipos de elemento.</span><span class="sxs-lookup"><span data-stu-id="cac18-114">The Print Schema Keywords defines a set of values for the name attribute for many of the element types.</span></span> <span data-ttu-id="cac18-115">En la mayoría de los casos, los proveedores pueden asignar sus propios valores al atributo de nombre.</span><span class="sxs-lookup"><span data-stu-id="cac18-115">In most cases, providers can assign their own values to the name attribute.</span></span> <span data-ttu-id="cac18-116">Solo necesitan asegurarse de que los valores sean QNames XML calificados con un espacio de nombres que sea único para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="cac18-116">They need only ensure the values are XML QNames qualified with a namespace that is unique to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cac18-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cac18-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cac18-118">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="cac18-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



