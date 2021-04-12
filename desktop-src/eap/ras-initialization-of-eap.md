---
title: Inicialización de punto de acceso de EAP
description: Tras la inicialización, el punto de acceso (AP) consulta el registro para obtener los protocolos de autenticación instalados.
ms.assetid: e230e01f-27df-4f61-8755-262ec11af660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185557c4b908780c09714aa9cc7fa4c80399812f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420722"
---
# <a name="access-point-initialization-of-eap"></a>Inicialización de punto de acceso de EAP

Tras la inicialización, el punto de acceso (AP) consulta el registro para obtener los protocolos de autenticación instalados. A continuación, el AP llama a la función exportada [**RasEapGetInfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) para cada protocolo de autenticación. La función **RasEapGetInfo** recibe un parámetro único de tipo [**PPP \_ EAP \_ info**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info). El AP usa el miembro **dwEapTypeId** de esta estructura para especificar el protocolo de autenticación. Tenga en cuenta que un único archivo DLL puede admitir más de un protocolo. Si **RasEapGetInfo** devuelve cualquier valor que **no sea ningún \_ error**, el AP supone que el protocolo de autenticación no está disponible.

En la devolución [**de RasEapGetInfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) , la estructura de [**\_ \_ información de EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info) contiene punteros a las funciones [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)), [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))y [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) en el archivo dll de EAP. El servicio AP utiliza estas funciones para interoperar con el protocolo de autenticación. El AP llama inmediatamente a **RasEapInitialize** para cada protocolo de autenticación, para inicializarlo. Cuando el servicio se cierra, llama de nuevo a **RasEapInitialize** , esta vez con el parámetro *FInitialize* establecido en **false** para indicar que el protocolo de autenticación debe cerrarse.

 

 