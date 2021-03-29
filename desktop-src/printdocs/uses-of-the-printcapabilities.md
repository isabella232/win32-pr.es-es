---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Usos de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dda5b21d1472ec8d4162c8d7229ff47264fb55
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104003467"
---
# <a name="uses-of-the-printcapabilities"></a><span data-ttu-id="0e89e-104">Usos de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="0e89e-104">Uses of the PrintCapabilities</span></span>

<span data-ttu-id="0e89e-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="0e89e-105">This topic is not current.</span></span> <span data-ttu-id="0e89e-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0e89e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0e89e-107">La PrintCapabilities está pensada para representar atributos de dispositivo configurables como construcciones de características o de opciones o construcciones de parámetros.</span><span class="sxs-lookup"><span data-stu-id="0e89e-107">The PrintCapabilities are intended to represent configurable device attributes as either Feature/Option constructs or parameter constructs.</span></span> <span data-ttu-id="0e89e-108">Esta información define el espacio de configuración del dispositivo y puede ser utilizado por un cliente de la interfaz de usuario (UI) para construir una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="0e89e-108">This information defines the configuration space of the device and can be used by a user interface (UI) client to construct a UI.</span></span> <span data-ttu-id="0e89e-109">Las palabras clave del esquema de impresión definen un conjunto de instancias de características estándar, instancias de opciones para las instancias de características estándar e instancias de ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="0e89e-109">The Print Schema Keywords define a set of standard Feature instances, Option instances for the standard Feature instances, and ParameterDef instances.</span></span>

<span data-ttu-id="0e89e-110">Las construcciones de características, opciones o parámetros de PrintCapabilities están pensadas para contener instancias de propiedad o ScoredProperty que describen un dispositivo y que son compatibles con el subsistema de cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="0e89e-110">The Feature/Option or parameter constructs in the PrintCapabilities are intended to hold Property or ScoredProperty instances that describe a device, and that are supported by the spooler subsystem.</span></span> <span data-ttu-id="0e89e-111">Estas instancias de propiedad y ScoredProperty son de interés general para los clientes del dispositivo y contienen la información proporcionada por las funciones DevCaps de Win32.</span><span class="sxs-lookup"><span data-stu-id="0e89e-111">These Property and ScoredProperty instances are of general interest to clients of the device, and contain the information that is provided by the Win32 DevCaps functions.</span></span> <span data-ttu-id="0e89e-112">Las palabras clave de esquema de impresión definen un conjunto de instancias de ScoredProperty y de propiedades estándar.</span><span class="sxs-lookup"><span data-stu-id="0e89e-112">The Print Schema Keywords define a set of standard Property and ScoredProperty instances.</span></span>

<span data-ttu-id="0e89e-113">Se debe resaltar que el documento de PrintCapabilities está diseñado para representar solo datos de valor único: datos que no dependen de una configuración determinada del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e89e-113">It should be emphasized that the PrintCapabilities document is intended to represent only single-valued data: data that does not depend on a particular configuration of the device.</span></span> <span data-ttu-id="0e89e-114">El documento de PrintCapabilities solo proporciona una instantánea de los datos dependientes de la configuración.</span><span class="sxs-lookup"><span data-stu-id="0e89e-114">The PrintCapabilities document provides only a snapshot of configuration-dependent data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e89e-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e89e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e89e-116">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="0e89e-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



