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
# <a name="phonehookswitchdev_-constants"></a>Constantes de PHONEHOOKSWITCHDEV \_

Las constantes de marcador de bits **PHONEHOOKSWITCHDEV \_** describen varios dispositivos de e/s de audio, cada uno con su propio conmutador controlable desde el equipo.

<dl> <dt>

<span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**auricular de PHONEHOOKSWITCHDEV \_**
</dt> <dd> <dl> <dt>



Se trata de un teléfono estándar de lengüeta y boquilla.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**\_auriculares PHONEHOOKSWITCHDEV**
</dt> <dd> <dl> <dt>



Se trata de un casco conectado al conjunto de teléfonos.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**altavoz de PHONEHOOKSWITCHDEV \_**
</dt> <dd> <dl> <dt>



Se trata de un altavoz y micrófono integrados. También podría ser un orador de complemento conectado externamente al conjunto de teléfonos.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Estas constantes se utilizan en la estructura de datos [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) para indicar las capacidades del dispositivo conmutador de un dispositivo telefónico. La estructura [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) informa del estado de los dispositivos conmutador del teléfono. La función [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) y [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) la usan como parámetro para seleccionar el dispositivo de e/s del teléfono.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




