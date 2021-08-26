---
description: Un dispositivo de teléfono puede tener varios dispositivos de conmutador de enlace.
ms.assetid: 39e3f24d-55d8-4830-8599-383954c8a107
title: Dispositivos hookswitch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3ca5c9f605731780068b9ad5a5b35d913213006c62d127e6a3b15d1ffc5fe1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013105"
---
# <a name="hookswitch-devices"></a>Dispositivos hookswitch

Un dispositivo de teléfono puede tener varios dispositivos de conmutador de enlace. Un conmutador de enlace es el conmutador que conecta o desconecta un dispositivo de la línea telefónica. Por ejemplo, en un teléfono, este es el conmutador que se activa automáticamente cuando un usuario eleva el receptor del teléfono para obtener un nuevo tono de marcado. TAPI define tres tipos de dispositivos de conmutador de enlace para un teléfono: teléfono, altavoz y casco. Cada dispositivo de conmutador de enlace tiene un altavoz y un componente de micrófono, y funciona en uno de los cuatro modos de conmutador de enlace:

-   **Onhook** El dispositivo de conmutador de enlace está en elhook y su micrófono y altavoz están deshabilitados.
-   **Solo micrófono** El dispositivo hookswitch es offhook, su micrófono está habilitado y su altavoz está silenciado.
-   **Solo altavoz** El dispositivo de conmutador de enlace es offhook, su micrófono está silenciado y su altavoz está habilitado.
-   **Micrófono y altavoz** El dispositivo de conmutador de enlace es offhook y tanto el micrófono como el altavoz están habilitados.

La [**función phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) se usa para establecer el modo hookswitch de uno o varios de los dispositivos hookswitch de un dispositivo de teléfono abierto. Por ejemplo, para silenciar o desactivar el micrófono o el componente de altavoz de un dispositivo de conmutador de enlace, use **phoneSetHookSwitch** con el modo de conmutador de enlace adecuado. La [**función phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) se puede usar para consultar el modo hookswitch de un dispositivo hookswitch de un dispositivo de teléfono abierto.

Cuando el modo del dispositivo de conmutador de enlace de un teléfono cambia manualmente, por ejemplo, al levantar el teléfono de su casa, se envía un mensaje [**PHONE \_ STATE**](phone-state.md) a la aplicación para notificar a la aplicación sobre el cambio de estado. Los parámetros de este mensaje proporcionan una indicación del cambio.

El volumen del componente de altavoz de un dispositivo de conmutador de enlace se puede establecer con [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume). La configuración del volumen es diferente de la exclusión mutua, ya que al silenciar un hablante y, posteriormente, desmutar, se conservará la configuración del volumen del hablante. La [**función phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) se puede usar para devolver la configuración de volumen actual del altavoz de un dispositivo de conmutador de enlace de un dispositivo de teléfono abierto.

El componente de micrófono de un dispositivo de conmutador de enlace también se puede controlar. La configuración de ganancia es diferente de la exclusión mutua, ya que al silenciar un micrófono y, posteriormente, desmutar, se conservará la configuración de ganancia del micrófono. Use [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) para establecer la ganancia del micrófono de un dispositivo de conmutador de enlace de un dispositivo de teléfono abierto y [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) para devolver la configuración de ganancia del micrófono de un dispositivo de conmutador de enlace de un teléfono abierto.

Cuando se cambia el volumen o la ganancia del dispositivo de conmutador de enlace de un teléfono, se envía un mensaje PHONE STATE a la función de aplicación para notificar a la aplicación el cambio \_ de estado. Los parámetros de este mensaje proporcionan una indicación del cambio.

 

 



