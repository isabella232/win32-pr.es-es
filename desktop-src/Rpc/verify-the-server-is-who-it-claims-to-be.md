---
title: Compruebe que el servidor Quién que dice ser
description: Es mejor usar la autenticación mutua y, por tanto, comprobar la identidad del servidor.
ms.assetid: 6636a865-0e3b-4e52-81bb-0df48285e928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57c11716f94ec4a8c2184c45486e31f6d3cfda9642b346f8bf464c1a3f85944
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010533"
---
# <a name="verify-the-server-is-who-it-claims-to-be"></a>Compruebe que el servidor Quién que dice ser

Es mejor usar la autenticación mutua y, por tanto, comprobar la identidad del servidor. Un ejemplo de un error común que no puede hacerlo son las aplicaciones que tienen un servicio local al que llaman los clientes. En algunas configuraciones, un administrador puede decidir que el servicio del sistema no es realmente útil y puede optar por detenerlo. Un atacante malintencionado en un equipo de terminal Server puede iniciar un proceso que escucha en el mismo punto de conexión y, cuando un cliente se conecta a un punto de conexión, lo que permite la suplantación en el servidor sin autenticar mutuamente el servidor, el atacante puede suplantar al cliente y acceder a los datos del cliente, o realizar llamadas de red en nombre del cliente. La mayoría de los servicios del sistema se ejecutan con una cuenta conocida, como LocalSysyem, LocalService o NetworkService, que se pueden comprobar mediante autenticación mutua.

 

 




