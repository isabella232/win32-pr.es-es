---
description: En estos artículos se proporciona información más detallada sobre el significado y el uso de los tipos de elementos Print Schema.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Marco de esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570701df700954ad85fb724b9528b7e7912f3174
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407168"
---
# <a name="print-schema-framework"></a><span data-ttu-id="092c2-103">Marco de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="092c2-103">Print Schema Framework</span></span>

<span data-ttu-id="092c2-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="092c2-104">This topic is not current.</span></span> <span data-ttu-id="092c2-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="092c2-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="092c2-106">En esta sección se proporciona información más detallada sobre el significado y el uso de los tipos de elemento Print Schema.</span><span class="sxs-lookup"><span data-stu-id="092c2-106">This section provides more detailed information on the meaning and usage of the Print Schema element types.</span></span> <span data-ttu-id="092c2-107">El enfoque principal de la versión inicial de Print Schema Framework es representar las configuraciones y las funcionalidades de los atributos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="092c2-107">The main focus of the initial version of the Print Schema Framework is to represent configurations and capabilities of device attributes.</span></span> <span data-ttu-id="092c2-108">En un nivel alto, este marco ofrece dos estilos diferentes para describir un atributo de dispositivo: como una construcción feature/option o como una construcción de parámetros.</span><span class="sxs-lookup"><span data-stu-id="092c2-108">At a high level, this framework offers two different styles of describing a device attribute: as a Feature/Option construct, or as a parameter construct.</span></span> <span data-ttu-id="092c2-109">Si un atributo de dispositivo tiene un número pequeño de valores o estados disponibles, el atributo debe caracterizarse como una característica con los valores o estados permitidos denominados elementos Option.</span><span class="sxs-lookup"><span data-stu-id="092c2-109">If a device attribute has a small number of available values or states, then the attribute should be characterized as a Feature with the allowed values or states referred to as Option elements.</span></span> <span data-ttu-id="092c2-110">Por el contrario, si un atributo de dispositivo tiene un gran número de valores o estados disponibles y el conjunto de todos los valores posibles se define fácilmente sin recurrir a la enumeración explícita, el atributo de dispositivo debe caracterizarse como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="092c2-110">Conversely, if a device attribute has a large number of available values or states and the set of all possible values is easily defined without resorting to explicit enumeration, the device attribute should be characterized as a parameter.</span></span> <span data-ttu-id="092c2-111">(Un parámetro se define mediante un elemento ParameterDef y una instancia de parámetro se inicializa mediante un elemento ParameterInit). Los elementos property se usan en las construcciones feature/option y de parámetros para proporcionar un nivel más fino de diferenciación.</span><span class="sxs-lookup"><span data-stu-id="092c2-111">(A parameter is defined by means of a ParameterDef element, and a parameter instance is initialized by means of a ParameterInit element.) Property elements are used within Feature/Option and parameter constructs to provide a finer level of differentiation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="092c2-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="092c2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="092c2-113">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="092c2-113">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



