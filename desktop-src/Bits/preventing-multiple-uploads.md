---
title: Impedir varias cargas
description: Cuando se carga un archivo, BITS crea un identificador de sesión que identifica la sesión de carga en el cliente BITS y el servidor BITS.
ms.assetid: 97283f8e-d2fa-4383-9b92-a05f46680443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae59bb1d605af7e4dd53b0c1d66618b6816e7886
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075171"
---
# <a name="preventing-multiple-uploads"></a>Impedir varias cargas

Cuando se carga un archivo, BITS crea un identificador de sesión que identifica la sesión de carga en el cliente BITS y el servidor BITS. Si la conexión entre el cliente BITS y el servidor se interrumpe mientras BITS carga un archivo, el cliente usará el ID. de sesión para intentar reanudar la carga.

Si el cliente de BITS se conecta al mismo servidor que antes, el servidor reconocerá el identificador de sesión y la carga se reanudará desde el punto de interrupción. Sin embargo, si el cliente se conecta a un servidor diferente, el cliente debe iniciar la carga desde el principio porque el nuevo servidor no tiene el contexto de la sesión o los datos cargados previamente. BITS puede conectarse a un servidor diferente cuando el servidor BITS está hospedado en una granja de servidores web y la propiedad de extensión de IIS de BITS, [BITSHostId](bits-iis-extension-properties.md), no está establecida. La propiedad BITSHostId evita los reinicios forzando al cliente de BITS a conectarse a la dirección única del servidor anterior en lugar de a la dirección del servidor compartido.

El servidor BITS intentará enviar el archivo de carga una sola vez a la aplicación de servidor, pero es posible que el archivo se envíe más de una vez. Esto puede ocurrir, por ejemplo, si el servidor BITS envía el archivo a la aplicación de servidor y, a continuación, finaliza mientras se espera la respuesta de la aplicación de servidor. El cliente de BITS recibirá un código de error de la capa HTTP y volverá a intentar la carga después de un retraso. Si el servidor permanece sin conexión durante más tiempo que el tiempo de espera de [BITSHostIdFallbackTimeout](bits-iis-extension-properties.md) , el cliente volverá a enviar la solicitud a la dirección del servidor compartido; un servidor BITS distinto recibirá el archivo y lo entregará de nuevo a la aplicación de servidor.

Un caso similar puede producirse incluso con un solo servidor front-end. Por ejemplo, cuando el cliente ha cargado el archivo completo en el servidor, el bloque final hace que el servidor reenvíe el archivo a la aplicación de servidor. Si el servidor BITS o la aplicación de servidor terminan después de procesarse el archivo, pero antes de que se envíe la confirmación al cliente, el cliente recibirá un código de error y volverá a intentarlo más tarde. Cuando el cliente vuelva a intentarlo, el servidor BITS verá que se ha cargado el bloque final y volverá a enviar el archivo a la aplicación de servidor. Si recibir el archivo de carga varias veces es un problema para su aplicación de servidor, considere la posibilidad de incluir un identificador de transacción en los datos.

 

 




