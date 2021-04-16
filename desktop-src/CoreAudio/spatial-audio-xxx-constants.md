---
description: Las \_ constantes de audio espacial \_ XXX definen valores relacionados con las características de sonido espacial.
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: Constantes de SPATIAL_AUDIO_XXX (SpatialAudioMetadata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2c92b970f69cf84e0744f21a41932a8851efed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650021"
---
# <a name="spatial_audio_xxx-constants"></a><span data-ttu-id="b2b6a-103">\_Constantes de audio espacial \_ XXX</span><span class="sxs-lookup"><span data-stu-id="b2b6a-103">SPATIAL\_AUDIO\_XXX Constants</span></span>

<span data-ttu-id="b2b6a-104">Las \_ constantes de audio espacial \_ XXX definen valores relacionados con las características de sonido espacial.</span><span class="sxs-lookup"><span data-stu-id="b2b6a-104">The SPATIAL\_AUDIO\_XXX constants define values related to spatial sound features.</span></span>



| <span data-ttu-id="b2b6a-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="b2b6a-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="b2b6a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2b6a-106">Description</span></span>                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <span data-ttu-id="b2b6a-107"><dt>**Espacial \_ \_Posición de AUDIO**</dt> <dt>200</dt></span><span class="sxs-lookup"><span data-stu-id="b2b6a-107"><dt>**SPATIAL\_AUDIO\_POSITION**</dt> <dt>200</dt></span></span> </dl>                                                   | <span data-ttu-id="b2b6a-108">Un comando estándar de metadatos de audio espacial definido por Microsoft que representa la posición del agente de escucha en el modelo estándar usado por [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) , donde el encabezado del agente de escucha se coloca en las coordenadas (0,0), definido en metros.</span><span class="sxs-lookup"><span data-stu-id="b2b6a-108">A standard Microsoft-defined spatial audio metadata command which represents the listener position in the standard model used by [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) where the listener's head is position at coordinates (0,0,0), defined in meters.</span></span><br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <span data-ttu-id="b2b6a-109"><dt>**Espacial \_ \_ \_ \_ Número de bytes de posición de audio**</dt> <dt>sizeof (float) \* 3</dt></span><span class="sxs-lookup"><span data-stu-id="b2b6a-109"><dt>**SPATIAL\_AUDIO\_POSITION\_BYTE\_COUNT**</dt> <dt>sizeof(float) \* 3</dt></span></span> </dl> | <span data-ttu-id="b2b6a-110">Especifica el tamaño del valor **de \_ \_ posición de audio espacial** .</span><span class="sxs-lookup"><span data-stu-id="b2b6a-110">Specifies the size of the **SPATIAL\_AUDIO\_POSITION** value.</span></span><br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <span data-ttu-id="b2b6a-111"><dt>**Espacial \_ \_Comandos estándar de audio \_ \_ Start**</dt> <dt>200</dt></span><span class="sxs-lookup"><span data-stu-id="b2b6a-111"><dt>**SPATIAL\_AUDIO\_STANDARD\_COMMANDS\_START**</dt> <dt>200</dt></span></span> </dl>    | <span data-ttu-id="b2b6a-112">Especifica el inicio del intervalo de comandos de metadatos de audio espaciales reservados de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b2b6a-112">Specifies the start of the range of Microsoft-reserved spatial audio metadata commands.</span></span> <span data-ttu-id="b2b6a-113">Los comandos de metadatos personalizados están restringidos a los identificadores de comando 0-199.</span><span class="sxs-lookup"><span data-stu-id="b2b6a-113">Custom metadata commands are restricted to command IDs 0 - 199.</span></span> <span data-ttu-id="b2b6a-114">Los comandos 200-255 están reservados para su uso por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b2b6a-114">Commands 200 - 255 are reserved for Microsoft use.</span></span><br/>                                                           |



## <a name="requirements"></a><span data-ttu-id="b2b6a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2b6a-115">Requirements</span></span>



| <span data-ttu-id="b2b6a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2b6a-116">Requirement</span></span> | <span data-ttu-id="b2b6a-117">Value</span><span class="sxs-lookup"><span data-stu-id="b2b6a-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b6a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2b6a-118">Header</span></span><br/> | <dl> <span data-ttu-id="b2b6a-119"><dt>SpatialAudioMetadata. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2b6a-119"><dt>SpatialAudioMetadata.h</dt></span></span> </dl> |



 

 




