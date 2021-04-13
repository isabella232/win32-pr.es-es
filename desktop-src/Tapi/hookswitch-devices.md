---
description: Un dispositivo telefónico puede tener varios dispositivos conmutador.
ms.assetid: 39e3f24d-55d8-4830-8599-383954c8a107
title: Dispositivos conmutador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69ad6f839ec9078831ffe0b04849be2a4393c9d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543494"
---
# <a name="hookswitch-devices"></a>Dispositivos conmutador

Un dispositivo telefónico puede tener varios dispositivos conmutador. Un conmutador es el conmutador que conecta o desconecta un dispositivo de la línea telefónica. En un teléfono, por ejemplo, este es el conmutador que se activa automáticamente cuando un usuario levanta el receptor del soporte de conexión para obtener un nuevo tono de marcado. TAPI define tres tipos de dispositivos conmutador para un teléfono: auricular, altavoz y auriculares. Cada dispositivo conmutador tiene un altavoz y un componente de micrófono y funciona en uno de cuatro modos conmutador:

-   **Enlace** El dispositivo conmutador está enlazado y el micrófono y el altavoz están deshabilitados.
-   **Solo micrófono** El dispositivo conmutador es OffHook, su micrófono está habilitado y su altavoz es silenciado.
-   **Solo altavoz** El dispositivo conmutador es OffHook, el micrófono es silenciado y su altavoz está habilitado.
-   **Micrófono y altavoz** El dispositivo conmutador es OffHook y el micrófono y el altavoz están habilitados.

La función [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) se usa para establecer el modo conmutador de uno o varios de los dispositivos conmutador de un dispositivo telefónico abierto. Por ejemplo, para silenciar o dessilenciar el micrófono o el componente de altavoz de un dispositivo conmutador, use **phoneSetHookSwitch** con el modo conmutador adecuado. La función [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) se puede usar para consultar el modo conmutador de un dispositivo conmutador de un dispositivo telefónico abierto.

Cuando se cambia manualmente el modo del dispositivo conmutador de un teléfono, por ejemplo, al levantar el auricular del soporte de la base, se envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) a la aplicación para notificar a la aplicación sobre el cambio de estado. Los parámetros de este mensaje proporcionan una indicación del cambio.

El volumen del componente de altavoz de un dispositivo conmutador se puede establecer con [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume). La configuración del volumen es diferente de silenciar en que silenciar un altavoz y después dessilenciarlo conservará la configuración de volumen del altavoz. La función [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) se puede usar para devolver la configuración de volumen actual del altavoz de un dispositivo conmutador de un dispositivo teléfono abierto.

También se puede controlar el componente de micrófono de un dispositivo conmutador. La configuración de ganancia es diferente de silenciar en que silenciar un micrófono y después dessilenciarlo conservará el valor de ganancia del micrófono. Use [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) para establecer la ganancia del micrófono de un dispositivo conmutador de un dispositivo teléfono abierto y [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) para devolver el valor de ganancia del micrófono de un dispositivo conmutador de un teléfono abierto.

Cuando se cambia el volumen o la ganancia del dispositivo conmutador de un teléfono, \_ se envía un mensaje de estado de teléfono a la función de aplicación para notificar a la aplicación sobre el cambio de estado. Los parámetros de este mensaje proporcionan una indicación del cambio.

 

 



