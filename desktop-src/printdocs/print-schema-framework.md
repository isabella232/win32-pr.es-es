---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Marco de esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617f747b950676f2359645684c9e672fb5c87ee3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279848"
---
# <a name="print-schema-framework"></a><span data-ttu-id="425b5-104">Marco de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="425b5-104">Print Schema Framework</span></span>

<span data-ttu-id="425b5-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="425b5-105">This topic is not current.</span></span> <span data-ttu-id="425b5-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="425b5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="425b5-107">En esta sección se proporciona información más detallada sobre el significado y el uso de los tipos de elemento de esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="425b5-107">This section provides more detailed information on the meaning and usage of the Print Schema element types.</span></span> <span data-ttu-id="425b5-108">El enfoque principal de la versión inicial del marco de trabajo del esquema de impresión es representar las configuraciones y las capacidades de los atributos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="425b5-108">The main focus of the initial version of the Print Schema Framework is to represent configurations and capabilities of device attributes.</span></span> <span data-ttu-id="425b5-109">En un nivel alto, este marco de trabajo ofrece dos estilos diferentes para describir un atributo de dispositivo: como una construcción de característica/opción o como una construcción de parámetro.</span><span class="sxs-lookup"><span data-stu-id="425b5-109">At a high level, this framework offers two different styles of describing a device attribute: as a Feature/Option construct, or as a parameter construct.</span></span> <span data-ttu-id="425b5-110">Si un atributo de dispositivo tiene un pequeño número de valores o Estados disponibles, el atributo debe caracterizarse como una característica con los valores permitidos o los Estados a los que se hace referencia como elementos de opción.</span><span class="sxs-lookup"><span data-stu-id="425b5-110">If a device attribute has a small number of available values or states, then the attribute should be characterized as a Feature with the allowed values or states referred to as Option elements.</span></span> <span data-ttu-id="425b5-111">Por el contrario, si un atributo de dispositivo tiene un gran número de valores o Estados disponibles y el conjunto de todos los valores posibles se define fácilmente sin recurrir a la enumeración explícita, el atributo de dispositivo se debe caracterizar como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="425b5-111">Conversely, if a device attribute has a large number of available values or states and the set of all possible values is easily defined without resorting to explicit enumeration, the device attribute should be characterized as a parameter.</span></span> <span data-ttu-id="425b5-112">(Un parámetro se define por medio de un elemento ParameterDef, y una instancia de parámetro se inicializa mediante un elemento ParameterInit). Los elementos de propiedad se utilizan en las construcciones de características, opciones y parámetros para proporcionar un nivel de diferenciación más preciso.</span><span class="sxs-lookup"><span data-stu-id="425b5-112">(A parameter is defined by means of a ParameterDef element, and a parameter instance is initialized by means of a ParameterInit element.) Property elements are used within Feature/Option and parameter constructs to provide a finer level of differentiation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="425b5-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="425b5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="425b5-114">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="425b5-114">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



