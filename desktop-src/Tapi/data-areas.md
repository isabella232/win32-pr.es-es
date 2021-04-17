---
description: Algunos conjuntos de teléfonos admiten la noción de descargar datos desde o cargar datos en el dispositivo telefónico, lo que permite que el conjunto de teléfonos se programe de varias maneras.
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: Áreas de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81376549c63b4fcea92f705246cd58161faeac94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677814"
---
# <a name="data-areas"></a><span data-ttu-id="b80c5-103">Áreas de datos</span><span class="sxs-lookup"><span data-stu-id="b80c5-103">Data Areas</span></span>

<span data-ttu-id="b80c5-104">Algunos conjuntos de teléfonos admiten la noción de descargar datos desde o cargar datos en el dispositivo telefónico, lo que permite que el conjunto de teléfonos se programe de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="b80c5-104">Some phone sets support the notion of downloading data from or uploading data to the phone device, which allows the phone set to be programmed in a variety of ways.</span></span> <span data-ttu-id="b80c5-105">TAPI modela estos conjuntos de teléfonos como una o varias áreas de descarga o carga.</span><span class="sxs-lookup"><span data-stu-id="b80c5-105">TAPI models these phone sets as having one or more download or upload areas.</span></span> <span data-ttu-id="b80c5-106">Cada área se identifica mediante un número comprendido entre cero y el número de áreas de datos disponibles en el teléfono menos uno.</span><span class="sxs-lookup"><span data-stu-id="b80c5-106">Each area is identified by a number that ranges from zero to the number of data areas available on the phone minus one.</span></span> <span data-ttu-id="b80c5-107">Los tamaños de cada área pueden variar.</span><span class="sxs-lookup"><span data-stu-id="b80c5-107">Sizes of each area can vary.</span></span> <span data-ttu-id="b80c5-108">El formato de los propios datos es específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b80c5-108">The format of the data itself is device-specific.</span></span>

<span data-ttu-id="b80c5-109">La función [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) de TAPI descarga un búfer de datos en un área de datos determinada en el dispositivo telefónico, y la función [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) carga el contenido de un área de datos determinada en el dispositivo teléfono en un búfer.</span><span class="sxs-lookup"><span data-stu-id="b80c5-109">The TAPI [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) function downloads a buffer of data to a given data area in the phone device, and the [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) function uploads the contents of a given data area in the phone device to a buffer.</span></span>

<span data-ttu-id="b80c5-110">Cuando se cambia un área de datos de un dispositivo telefónico, se envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) a la aplicación para notificar a la aplicación sobre el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="b80c5-110">When a data area of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="b80c5-111">Los parámetros de este mensaje proporcionan una indicación del cambio.</span><span class="sxs-lookup"><span data-stu-id="b80c5-111">Parameters to this message provide an indication of the change.</span></span>

 

 



