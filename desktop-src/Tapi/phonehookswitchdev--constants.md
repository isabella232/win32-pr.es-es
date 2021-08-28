---
description: Las constantes de marca de bits PHONEHOOKSWITCHDEV describen varios dispositivos de E/S de audio, cada uno con su propio conmutador de enlace \_ controlable desde el equipo.
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: PHONEHOOKSWITCHDEV_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77e6b776b89adf6224d6feaef8deeef1f9f71b9888929f3aea08b5342adc1dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796755"
---
# <a name="phonehookswitchdev_-constants"></a>Constantes PHONEHOOKSWITCHDEV \_

Las constantes de marca de bits **PHONEHOOKSWITCHDEV \_** describen varios dispositivos de E/S de audio cada uno con su propio conmutador de enlace controlable desde el equipo.

<dl> <dt>

<span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**PHONEHOOKSWITCHDEV \_ HANDSET**
</dt> <dd> <dl> <dt>



Se trata de un teléfono estándar de auriculares y auriculares.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**CASCO PHONEHOOKSWITCHDEV \_**
</dt> <dd> <dl> <dt>



Se trata de un casco conectado al conjunto de teléfonos.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV \_ SPEAKER**
</dt> <dd> <dl> <dt>



Se trata de un altavoz y micrófono integrados. También podría ser un altavoz adjunto conectado externamente al conjunto de teléfonos.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

Estas constantes se usan en la estructura de datos [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) para indicar las funcionalidades del dispositivo hookswitch de un dispositivo de teléfono. La [**estructura PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) informa del estado de los dispositivos de conmutador de enlace del teléfono. La función [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) y [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) la usan como parámetro para seleccionar el dispositivo de E/S del teléfono.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




