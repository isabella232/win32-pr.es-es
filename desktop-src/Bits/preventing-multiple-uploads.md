---
title: Impedir varias cargas
description: Al cargar un archivo, BITS crea un identificador de sesión que identifica la sesión de carga en el cliente bits y el servidor BITS.
ms.assetid: 97283f8e-d2fa-4383-9b92-a05f46680443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae59bb1d605af7e4dd53b0c1d66618b6816e7886
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167986"
---
# <a name="preventing-multiple-uploads"></a>Impedir varias cargas

Al cargar un archivo, BITS crea un identificador de sesión que identifica la sesión de carga en el cliente bits y el servidor BITS. Si la conexión entre el cliente bits y el servidor se divide mientras BITS carga un archivo, el cliente usará el identificador de sesión para intentar reanudar la carga.

Si el cliente BITS se conecta al mismo servidor que antes, el servidor reconocerá el identificador de sesión y la carga se reanudará desde el punto de interrupción. Sin embargo, si el cliente se conecta a un servidor diferente, el cliente debe iniciar la carga desde el principio porque el nuevo servidor no tiene el contexto de sesión ni los datos cargados anteriormente. BITS puede conectarse a un servidor diferente cuando el servidor BITS se hospeda en una granja de servidores web y la propiedad de extensión IIS bits, [BITSHostId](bits-iis-extension-properties.md), no está establecida. La propiedad BITSHostId impide los reinicios al forzar al cliente bits a conectarse a la dirección única del servidor anterior en lugar de a la dirección del servidor compartido.

El servidor BITS intentará enviar el archivo de carga solo una vez a la aplicación de servidor, pero es posible que el archivo se pueda enviar más de una vez. Esto puede ocurrir, por ejemplo, si el servidor BITS envía el archivo a la aplicación de servidor y, a continuación, finaliza mientras espera la respuesta de la aplicación de servidor. El cliente bits recibirá un código de error de la capa HTTP y volverá a intentar la carga después de un retraso. Si el servidor permanece sin conexión durante más tiempo que el tiempo de espera de [BITSHostIdFallbackTimeout,](bits-iis-extension-properties.md) el cliente finalmente enviará de nuevo la solicitud a la dirección del servidor compartido. un servidor BITS diferente recibirá el archivo y lo volverá a entregar a la aplicación de servidor.

Se puede producir un caso similar incluso con un único servidor front-end. Por ejemplo, cuando el cliente ha cargado todo el archivo en el servidor, el bloque final hace que el servidor reenvía el archivo a la aplicación del servidor. Si el servidor BITS o la aplicación de servidor finalizan después de procesar el archivo pero antes de que se envíe la confirmación al cliente, el cliente recibirá un código de error y volverá a intentarlo más tarde. Cuando el cliente vuelva a intentarlo, el servidor BITS verá que se ha cargado el bloque final y reenviará de nuevo el archivo a la aplicación de servidor. Si recibir el archivo de carga varias veces es un problema para la aplicación de servidor, considere la posibilidad de incluir un identificador de transacción en los datos.

 

 




