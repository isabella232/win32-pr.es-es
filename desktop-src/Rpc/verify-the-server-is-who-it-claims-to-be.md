---
title: Compruebe que el servidor Quién que dice ser
description: Es mejor usar la autenticación mutua y, por tanto, comprobar la identidad del servidor.
ms.assetid: 6636a865-0e3b-4e52-81bb-0df48285e928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e16ae6a87134a9fbc783d35216a1c4df56ce2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169022"
---
# <a name="verify-the-server-is-who-it-claims-to-be"></a>Compruebe que el servidor Quién que dice ser

Es mejor usar la autenticación mutua y, por tanto, comprobar la identidad del servidor. Un ejemplo de un error común que no puede hacerlo son las aplicaciones que tienen un servicio local al que llaman los clientes. En algunas configuraciones, un administrador puede decidir que el servicio del sistema no es realmente útil y puede optar por detenerlo. Un atacante inventariado en un equipo de terminal Server puede iniciar un proceso que escucha en el mismo punto de conexión y, cuando un cliente se conecta a un punto de conexión, lo que permite la suplantación en el servidor sin autenticar mutuamente el servidor, el atacante puede suplantar al cliente y acceder a los datos del cliente, o realizar llamadas de red en nombre del cliente. La mayoría de los servicios del sistema se ejecutan con una cuenta conocida, como LocalSysyem, LocalService o NetworkService, que se pueden comprobar mediante la autenticación mutua.

 

 




