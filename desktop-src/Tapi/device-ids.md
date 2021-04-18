---
description: Otras funciones de teléfono TAPI usan un controlador para un dispositivo telefónico abierto para identificar el dispositivo telefónico abierto.
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: Identificadores de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8eb9d43b22ab6cd39a90ab8ed0776c4e043ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677385"
---
# <a name="device-ids"></a><span data-ttu-id="0180a-103">Identificadores de dispositivo</span><span class="sxs-lookup"><span data-stu-id="0180a-103">Device IDs</span></span>

<span data-ttu-id="0180a-104">Otras funciones de teléfono TAPI usan un controlador para un dispositivo telefónico abierto para identificar el dispositivo telefónico abierto.</span><span class="sxs-lookup"><span data-stu-id="0180a-104">Other TAPI phone functions use a handle to an open phone device to identify the open phone device.</span></span> <span data-ttu-id="0180a-105">Las únicas funciones de los dispositivos telefónicos que toman un parámetro de identificador de dispositivo de teléfono (en lugar de un identificador de teléfono) son las funciones [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) y [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) .</span><span class="sxs-lookup"><span data-stu-id="0180a-105">The only functions for phone devices that take a phone device identifier parameter (as opposed to a phone handle) are the [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) and [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) functions.</span></span> <span data-ttu-id="0180a-106">Una aplicación puede recuperar el identificador de dispositivo del teléfono mediante la función [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) con el identificador de teléfono como parámetro.</span><span class="sxs-lookup"><span data-stu-id="0180a-106">An application can retrieve the phone's device identifier by using the [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function with the phone handle as a parameter.</span></span>

<span data-ttu-id="0180a-107">Una aplicación también puede obtener identificadores de dispositivo para varias clases de dispositivos asociadas a un teléfono abierto mediante la invocación de [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span><span class="sxs-lookup"><span data-stu-id="0180a-107">An application can also obtain device identifiers for various device classes associated with an opened phone by invoking [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span></span> <span data-ttu-id="0180a-108">Vea [clases de dispositivos TAPI](tapi-device-classes.md) para nombres de clase de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0180a-108">See [TAPI Device Classes](tapi-device-classes.md) for device class names.</span></span>

<span data-ttu-id="0180a-109">Esta función toma un identificador de teléfono y una descripción de clase de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0180a-109">This function takes a phone handle and a device class description.</span></span> <span data-ttu-id="0180a-110">Devuelve el identificador de dispositivo del dispositivo de la clase de dispositivo especificada que está asociada con el dispositivo telefónico abierto.</span><span class="sxs-lookup"><span data-stu-id="0180a-110">It returns the device identifier for the device of the given device class that is associated with the open phone device.</span></span> <span data-ttu-id="0180a-111">Si la clase de dispositivo es "TAPI/teléfono", se devuelve el identificador de dispositivo del dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="0180a-111">If the device class is "tapi/phone", the device identifier of the phone device is returned.</span></span>

<span data-ttu-id="0180a-112">A diferencia de los dispositivos de línea, para los que los servicios de línea básicos proporcionan el equivalente de los POTS, no se define ningún conjunto de funciones mínimo garantizado para los dispositivos de teléfono.</span><span class="sxs-lookup"><span data-stu-id="0180a-112">In contrast with line devices, for which the basic line services provide the equivalent of POTS, no minimum guaranteed set of functions is defined for phone devices.</span></span> <span data-ttu-id="0180a-113">Aunque cada dispositivo telefónico proporciona al menos las funciones y los mensajes que se describen en esta sección, no ofrecen ninguna operación real en el dispositivo de teléfono físico.</span><span class="sxs-lookup"><span data-stu-id="0180a-113">While each phone device provides at least the functions and messages described in this section, they do not offer any actual operations on the physical phone device.</span></span>

 

 



