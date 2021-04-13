---
description: Algunos sistemas usan firewalls de Internet o servidores proxy que requieren autenticación para todo el tráfico de Internet.
ms.assetid: b79e9a6f-2ffb-4ec0-ac2d-63e79ecfc26c
title: Servidor de símbolos y firewalls de Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2a85a5d0ee2d41e6ffee40bbb275155bdf1e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538452"
---
# <a name="symbol-server-and-internet-firewalls"></a>Servidor de símbolos y firewalls de Internet

Algunos sistemas usan firewalls de Internet o servidores proxy que requieren autenticación para todo el tráfico de Internet. Las versiones tempranas del servidor de símbolos no podían tener acceso a los símbolos desde Internet a menos que el sistema usara un cliente de firewall que controlaba la autenticación de forma transparente.

A partir de DbgHelp 6,1, el servidor de símbolos admite servidores proxy que requieren dicha autenticación. El servidor de símbolos usa el servidor que esté configurado como valor predeterminado en la configuración de LAN del equipo. Para encontrarlo, abra el elemento **Opciones de Internet** en el panel de control, haga clic en la pestaña **conexiones** y haga clic en **configuración de LAN**. Esto también se puede hacer en Internet Explorer haciendo clic en **Opciones de Internet** en el menú **herramientas** . El servidor de símbolos se ha probado en muchas marcas de servidores proxy mediante los métodos de autenticación básica y desafío-respuesta.

Para definir un servidor proxy específico para que lo use el servidor de símbolos, establezca la \_ \_ \_ variable de entorno de proxy Symbol de NT en el nombre (o dirección IP) del servidor proxy, seguido del número de puerto. Separe los dos valores con un signo de dos puntos. Por ejemplo:

**establecer \_ NT \_ Symbol \_ proxy =**_myservidorproxy_*_: 80_*

Al usar el depurador WinDbg, configure la ruta de acceso de símbolos para que apunte al almacén de símbolos que desea usar. La única diferencia es que el sistema mostrará un cuadro de diálogo en el que es necesario escribir el identificador de usuario y la contraseña para pasarlos al servidor proxy. Si escribe información incorrecta, se volverá a mostrar el cuadro de diálogo. Si hace clic en el botón **Cancelar** , se descarta el cuadro de diálogo y el servidor de símbolos se deshabilitará para su uso a través de Internet.

Al usar las versiones más recientes de cdb.exe o ntsd.exe, esta funcionalidad está desactivada de forma predeterminada. Sin embargo, puede habilitar o deshabilitar esta funcionalidad mediante el comando de extensión! SYM de la siguiente manera:

-   Para activar la solicitud de ID. de usuario y contraseña: **! SYM prompts**.
-   Para desactivar la solicitud de ID. de usuario y contraseña: **! SYM lo solicita**.

Si activa la solicitud, tendrá que volver a cargar los símbolos con el comando. Reload.

La API de DbgHelp se ha ampliado para admitir estos cambios. La función [**SymbolServerSetOptions**](/previous-versions//ms680676(v=vs.85)) admite la \_ opción de proxy SSRVOPT. Si el parámetro de datos es **null**, se usa el proxy predeterminado definido en **Opciones de Internet** . De lo contrario, se pasa una cadena terminada en cero que especifica el nombre y el número de puerto del servidor proxy. El nombre y el puerto se separan con dos puntos, como se indica a continuación: *myservidorproxy*: 80. La función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) admite la \_ opción SYMOPT no \_ prompts. Esto desactiva todas las solicitudes de validación del servidor de símbolos.

 

 
