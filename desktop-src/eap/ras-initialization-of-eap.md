---
title: Inicialización de punto de acceso de EAP
description: Tras la inicialización, el punto de acceso (AP) consulta al Registro los protocolos de autenticación instalados.
ms.assetid: e230e01f-27df-4f61-8755-262ec11af660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ff650df29a446527224d8160b4080a252d525d26d32efedae254755ac9514a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984435"
---
# <a name="access-point-initialization-of-eap"></a>Inicialización de punto de acceso de EAP

Tras la inicialización, el punto de acceso (AP) consulta al Registro los protocolos de autenticación instalados. A continuación, ap llama a la [**función exportada RasEapGetInfo para**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) cada protocolo de autenticación. La **función RasEapGetInfo recibe** un único parámetro de tipo PPP EAP [**\_ \_ INFO**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info). Ap usa el miembro **dwEapTypeId de** esta estructura para especificar el protocolo de autenticación. Tenga en cuenta que un solo archivo DLL puede admitir más de un protocolo. Si **RasEapGetInfo** devuelve cualquier valor distinto de **NO \_ ERROR**, la AP asume que el protocolo de autenticación no está disponible.

A la devolución de [**RasEapGetInfo,**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) la estructura [**PPP EAP \_ \_ INFO**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info) contiene punteros a las funciones [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)), [**RasEapBegin,**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))y [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) en el archivo DLL de EAP. El servicio AP usa estas funciones para interoperar con el protocolo de autenticación. El AP llama inmediatamente a **RasEapInitialize para** cada protocolo de autenticación, para inicializarlo. Cuando el servicio se cierra, llama de nuevo a **RasEapInitialize,** esta vez con el parámetro *fInitialize* establecido en **FALSE** para indicar que el protocolo de autenticación debe cerrarse.

 

 