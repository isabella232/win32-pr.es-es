---
description: Las \_ constantes de marcador de bits PHONEHOOKSWITCHDEV describen varios dispositivos de e/s de audio, cada uno con su propio conmutador controlable desde el equipo.
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: Constantes de PHONEHOOKSWITCHDEV_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a6727bf8103c35402bebc048de4ed9286650be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681289"
---
# <a name="phonehookswitchdev_-constants"></a><span data-ttu-id="399e9-103">Constantes de PHONEHOOKSWITCHDEV \_</span><span class="sxs-lookup"><span data-stu-id="399e9-103">PHONEHOOKSWITCHDEV\_ Constants</span></span>

<span data-ttu-id="399e9-104">Las constantes de marcador de bits **PHONEHOOKSWITCHDEV \_** describen varios dispositivos de e/s de audio, cada uno con su propio conmutador controlable desde el equipo.</span><span class="sxs-lookup"><span data-stu-id="399e9-104">The **PHONEHOOKSWITCHDEV\_** bit-flag constants describe various audio I/O devices each with its own hookswitch controllable from the computer.</span></span>

<dl> <dt>

<span data-ttu-id="399e9-105"><span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**auricular de PHONEHOOKSWITCHDEV \_**</span><span class="sxs-lookup"><span data-stu-id="399e9-105"><span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**PHONEHOOKSWITCHDEV\_HANDSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="399e9-106">Se trata de un teléfono estándar de lengüeta y boquilla.</span><span class="sxs-lookup"><span data-stu-id="399e9-106">This is a standard ear- and mouthpiece phone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="399e9-107"><span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**\_auriculares PHONEHOOKSWITCHDEV**</span><span class="sxs-lookup"><span data-stu-id="399e9-107"><span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**PHONEHOOKSWITCHDEV\_HEADSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="399e9-108">Se trata de un casco conectado al conjunto de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="399e9-108">This is a headset connected to the phone set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="399e9-109"><span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**altavoz de PHONEHOOKSWITCHDEV \_**</span><span class="sxs-lookup"><span data-stu-id="399e9-109"><span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV\_SPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="399e9-110">Se trata de un altavoz y micrófono integrados.</span><span class="sxs-lookup"><span data-stu-id="399e9-110">This is a built-in loudspeaker and microphone.</span></span> <span data-ttu-id="399e9-111">También podría ser un orador de complemento conectado externamente al conjunto de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="399e9-111">This could also be an externally connected adjunct speaker to the telephone set.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="399e9-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="399e9-112">Remarks</span></span>

<span data-ttu-id="399e9-113">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="399e9-113">No extensibility.</span></span> <span data-ttu-id="399e9-114">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="399e9-114">All 32 bits are reserved.</span></span>

<span data-ttu-id="399e9-115">Estas constantes se utilizan en la estructura de datos [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) para indicar las capacidades del dispositivo conmutador de un dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="399e9-115">These constants are used in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) data structure to indicate the hookswitch device capabilities of a phone device.</span></span> <span data-ttu-id="399e9-116">La estructura [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) informa del estado de los dispositivos conmutador del teléfono.</span><span class="sxs-lookup"><span data-stu-id="399e9-116">The [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) structure reports the state of the phone's hookswitch devices.</span></span> <span data-ttu-id="399e9-117">La función [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) y [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) la usan como parámetro para seleccionar el dispositivo de e/s del teléfono.</span><span class="sxs-lookup"><span data-stu-id="399e9-117">The function [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) and [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) use it as a parameter to select the phone's I/O device.</span></span>

## <a name="requirements"></a><span data-ttu-id="399e9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="399e9-118">Requirements</span></span>



| <span data-ttu-id="399e9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="399e9-119">Requirement</span></span> | <span data-ttu-id="399e9-120">Value</span><span class="sxs-lookup"><span data-stu-id="399e9-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="399e9-121">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="399e9-121">TAPI version</span></span><br/> | <span data-ttu-id="399e9-122">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="399e9-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="399e9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="399e9-123">Header</span></span><br/>       | <dl> <span data-ttu-id="399e9-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="399e9-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




