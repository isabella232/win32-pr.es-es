---
description: Obtenga información sobre los usos de PrintCapabilities. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Usos de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09882d42814930ef5ba08e087f1df87e0d0e9bc
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119430"
---
# <a name="uses-of-the-printcapabilities"></a><span data-ttu-id="39ed0-105">Usos de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="39ed0-105">Uses of the PrintCapabilities</span></span>

<span data-ttu-id="39ed0-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="39ed0-106">This topic is not current.</span></span> <span data-ttu-id="39ed0-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="39ed0-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="39ed0-108">PrintCapabilities está diseñado para representar atributos de dispositivo configurables como construcciones de características o opciones o construcciones de parámetros.</span><span class="sxs-lookup"><span data-stu-id="39ed0-108">The PrintCapabilities are intended to represent configurable device attributes as either Feature/Option constructs or parameter constructs.</span></span> <span data-ttu-id="39ed0-109">Esta información define el espacio de configuración del dispositivo y lo puede usar un cliente de interfaz de usuario (UI) para construir una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="39ed0-109">This information defines the configuration space of the device and can be used by a user interface (UI) client to construct a UI.</span></span> <span data-ttu-id="39ed0-110">Las palabras clave de esquema de impresión definen un conjunto de instancias de características estándar, instancias de opción para las instancias de feature estándar e instancias parameterdef.</span><span class="sxs-lookup"><span data-stu-id="39ed0-110">The Print Schema Keywords define a set of standard Feature instances, Option instances for the standard Feature instances, and ParameterDef instances.</span></span>

<span data-ttu-id="39ed0-111">Las construcciones de característica/opción o parámetro de PrintCapabilities están diseñadas para contener instancias de Property o ScoredProperty que describen un dispositivo y que son compatibles con el subsistema de cola.</span><span class="sxs-lookup"><span data-stu-id="39ed0-111">The Feature/Option or parameter constructs in the PrintCapabilities are intended to hold Property or ScoredProperty instances that describe a device, and that are supported by the spooler subsystem.</span></span> <span data-ttu-id="39ed0-112">Estas instancias de Property y ScoredProperty son de interés general para los clientes del dispositivo y contienen la información proporcionada por las funciones DevCaps de Win32.</span><span class="sxs-lookup"><span data-stu-id="39ed0-112">These Property and ScoredProperty instances are of general interest to clients of the device, and contain the information that is provided by the Win32 DevCaps functions.</span></span> <span data-ttu-id="39ed0-113">Las palabras clave de esquema de impresión definen un conjunto de instancias de Property y ScoredProperty estándar.</span><span class="sxs-lookup"><span data-stu-id="39ed0-113">The Print Schema Keywords define a set of standard Property and ScoredProperty instances.</span></span>

<span data-ttu-id="39ed0-114">Debe destacarse que el documento PrintCapabilities está pensado para representar solo datos de un solo valor: datos que no dependen de una configuración determinada del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39ed0-114">It should be emphasized that the PrintCapabilities document is intended to represent only single-valued data: data that does not depend on a particular configuration of the device.</span></span> <span data-ttu-id="39ed0-115">El documento PrintCapabilities proporciona solo una instantánea de los datos dependientes de la configuración.</span><span class="sxs-lookup"><span data-stu-id="39ed0-115">The PrintCapabilities document provides only a snapshot of configuration-dependent data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39ed0-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="39ed0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39ed0-117">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="39ed0-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



