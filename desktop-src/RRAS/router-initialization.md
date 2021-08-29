---
title: Inicialización del enrutador
description: La información de configuración del enrutador, los administradores de enrutadores y los protocolos o clientes de enrutamiento se divide en información global y por interfaz, y se almacena en el registro y el archivo de la libreta de teléfonos del enrutador, Router.pbk.
ms.assetid: c54541c1-6508-448a-a211-5fca634a184a
keywords:
- enrutadores RRAS, inicialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf3cbb55e4488da750a0fb8e8f813a5a5116a1d9e1caadad81eaefe4e12a79eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081115"
---
# <a name="router-initialization"></a>Inicialización del enrutador

La información de configuración del enrutador, los administradores de enrutadores y los protocolos o clientes de enrutamiento se divide en información global y por interfaz, y se almacena en el registro y el archivo de la libreta de teléfonos del enrutador, Router.pbk.

Cuando se inicia el proceso del enrutador, DIM (Administrador de interfaz dinámica) lee la configuración del enrutador del registro. DIM crea las interfaces especificadas por la información de la interfaz.

DIM también recupera la información del administrador de enrutadores global. DIM inicia los administradores de enrutadores que corresponden a esta información y les pasa la información. Por ejemplo, si DIM encuentra información global para el administrador de enrutadores IP en el registro, DIM inicia el administrador de enrutadores IP y le pasa la información global. Si no hay ninguna información global en el registro de un administrador de enrutadores determinado, DIM no inicia ese administrador de enrutadores.

Los administradores de enrutadores examinan la información global recibida de DIM. Si el administrador de enrutadores encuentra información específica de un cliente determinado dentro de la información global, el administrador de enrutadores carga el archivo DLL para el cliente (por ejemplo, IpNAT.dll) e inicializa el cliente mediante una llamada a las funciones [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) y [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) del cliente. El administrador de enrutadores pasa la información global específica del cliente al cliente en la llamada a [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).

En cada fase, la información que se pasa a la entidad siguiente es opaca para la entidad anterior. Es decir, DIM no interpreta la información global del administrador de enrutadores IP, más allá del hecho de que la información está pensada para el administrador de enrutadores IP. Del mismo modo, el administrador de enrutadores IP no interpreta la información específica de OSPF más allá del hecho de que se trata de información de OSPF.

 

 




