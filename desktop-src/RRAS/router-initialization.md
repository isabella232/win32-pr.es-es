---
title: Inicialización del enrutador
description: La información de configuración del enrutador, los administradores de enrutadores y los protocolos/clientes de enrutamiento se divide en información global y por interfaz, y se almacena en el registro y en el archivo de libreta de teléfonos del enrutador. pbk.
ms.assetid: c54541c1-6508-448a-a211-5fca634a184a
keywords:
- enrutadores RRAS, inicialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d45c10ef7b44b6dfe9d2d84149c77c81c5752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772583"
---
# <a name="router-initialization"></a>Inicialización del enrutador

La información de configuración del enrutador, los administradores de enrutadores y los protocolos/clientes de enrutamiento se divide en información global y por interfaz, y se almacena en el registro y en el archivo de libreta de teléfonos del enrutador. pbk.

Cuando se inicia el proceso del enrutador, DIM (Dynamic interface Manager) lee la configuración del enrutador del registro. DIM crea las interfaces especificadas por la información de la interfaz.

DIM también recupera la información global del administrador de enrutador. DIM inicia los administradores de enrutadores que corresponden a esta información y los pasa a la información. Por ejemplo, si DIM busca información global para el administrador de enrutadores IP en el registro, DIM inicia el administrador de enrutadores IP y le pasa la información global. Si no hay información global en el registro para un administrador de enrutador determinado, la dimensión no inicia ese administrador de enrutador.

Los administradores de enrutadores examinan la información global recibida de DIM. Si el administrador de enrutadores encuentra información específica de un cliente determinado dentro de la información global, el administrador de enrutador carga el archivo DLL para el cliente (por ejemplo IpNAT.dll) e inicializa el cliente llamando a las funciones [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) y [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) del cliente. El administrador de enrutadores pasa la información global específica del cliente al cliente en la llamada a [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).

En cada fase, la información que se pasa a la siguiente entidad es opaca en la entidad que lo precede. Es decir, la dimensión no interpreta la información global para el administrador de enrutadores IP, más allá del hecho de que la información está pensada para el administrador de enrutadores IP. Del mismo modo, el administrador de enrutamiento IP no interpreta la información específica de OSPF más allá del hecho de que es información de OSPF.

 

 




