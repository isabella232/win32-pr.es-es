---
title: DLL de cliente de canal virtual
description: El cliente de una aplicación de canales virtuales es un archivo DLL que se carga durante la inicialización del Servicios de Escritorio remoto en el equipo cliente. El archivo DLL debe estar registrado en el equipo cliente.
ms.assetid: fca0505c-c4a9-4230-aeaa-ff3dfa62f581
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd7ffccda8b1da7dfc3920b0a47a12e97840e0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075783"
---
# <a name="virtual-channel-client-dll"></a>DLL de cliente de canal virtual

El cliente de una aplicación de canales virtuales es un archivo DLL que se carga durante la inicialización del Servicios de Escritorio remoto en el equipo cliente. El archivo DLL debe estar registrado en el equipo cliente. Para obtener más información, consulte [registro de cliente de canal virtual](virtual-channel-client-registration.md).

El archivo DLL de cliente debe exportar una función [**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) , que servicios de escritorio remoto llama durante la inicialización. El punto de entrada **VirtualChannelEntry** recibe un puntero a una estructura de [**puntos de \_ entrada \_ de canal**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points) . Esta estructura contiene punteros a las funciones a las que el archivo DLL de cliente llama para tener acceso a los canales virtuales.



| Función                                                      | Descripción                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)<br/>   | Registra los nombres de los canales virtuales que va a utilizar el cliente y proporciona una función de devolución de llamada [**VirtualChannelInitEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) a través de la cual servicios de escritorio remoto notifica al cliente los eventos que afectan a la conexión del cliente.<br/> |
| [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)<br/>   | Abre el cliente final de un canal virtual especificado y proporciona una función de devolución de llamada [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) a través de la cual servicios de escritorio remoto notifica al cliente los eventos que afectan al canal virtual.<br/>                    |
| [**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)<br/> | Escribe datos en un canal virtual. Servicios de Escritorio remoto envía estos datos al final del servidor del canal virtual. El extremo del servidor llama a la función [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) para leer los datos.<br/>                                             |
| [**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)<br/> | Cierra un canal virtual.<br/>                                                                                                                                                                                                                                                  |



 

La función [**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) de la dll debe llamar a la función [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) para inicializar el acceso a los canales virtuales. Al llamar a **VirtualChannelInit**, debe pasar un puntero a la función de devolución de llamada [**VirtualChannelInitEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) . Servicios de Escritorio remoto llama a esta función de devolución de llamada cuando se completa la inicialización y de nuevo cuando se ha establecido una conexión con un servidor de host Escritorio remoto de sesión de escritorio remoto (host de sesión de RD).

Una vez establecida la conexión, puede llamar a la función [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) para abrir los canales virtuales registrados por la llamada a [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) . La llamada a **VirtualChannelOpen** especifica un puntero a la función de devolución de llamada [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) .

Después de que se devuelva la llamada [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) , puede llamar a la función [**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite) para escribir en el canal virtual. La operación de escritura es asincrónica, por lo que no debe liberar ni volver a usar el búfer que se pasa a **VirtualChannelWrite** hasta que servicios de escritorio remoto llama a la función [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) para indicar que se ha completado la operación de escritura. Cuando se llama a **VirtualChannelWrite**, se puede pasar una parte de los datos de usuario que identifica la operación de escritura. Servicios de Escritorio remoto pasa de nuevo estos datos de usuario cuando llama a **VirtualChannelOpenEvent** para notificarle que la operación se ha completado. En el extremo del servidor del canal virtual, el complemento del servidor llama a la función [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) para leer los datos.

Servicios de Escritorio remoto también llama a la función [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) cuando el módulo de servidor escribe los datos en el canal virtual. El módulo de servidor llama a la función [**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite) para escribir datos en el extremo de servidor del canal virtual.

Los módulos de cliente y servidor pueden escribir bloques de datos de cualquier tamaño en el canal virtual. Sin embargo, antes de enviar los datos, Servicios de Escritorio remoto segmenta los datos en fragmentos de \_ bytes de longitud de fragmentos de canal \_ . Servicios de Escritorio remoto llama a la función [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) una vez por cada fragmento de datos, en lugar de volver a generar los datos en un bloque del tamaño original. Cada llamada a **VirtualChannelOpenEvent** indica el tamaño del fragmento, el tamaño total escrito por el servidor y si los datos constituyen el inicio, el medio o el final de un bloque escrito por el servidor.

Puede llamar a la función [**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose) para cerrar un canal. Sin embargo, no es necesario llamarlo porque Servicios de Escritorio remoto cierra todos los canales automáticamente cuando el cliente se desconecta del servidor.

 

 





