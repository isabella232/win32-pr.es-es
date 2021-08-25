---
title: Acerca de la sincronización de listas de reproducción
description: Acerca de la sincronización de listas de reproducción
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Reproductor de Windows Media,sincronización de lista de reproducción
- Reproductor de Windows Media de objetos, sincronización de lista de reproducción
- modelo de objetos, sincronización de lista de reproducción
- Reproductor de Windows Media ActiveX, sincronización de lista de reproducción
- ActiveX control,sincronización de lista de reproducción
- Reproductor de Windows Media Control de ActiveX móvil,sincronización de lista de reproducción
- Reproductor de Windows Media Móvil, sincronización de lista de reproducción
- sincronizar dispositivos, listas de reproducción
- sincronización de dispositivos, listas de reproducción
- listas de reproducción, sincronización
- Windows Listas de reproducción de metarchivo multimedia, sincronización
- listas de reproducción de metarchivo, sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe54bef188fea2baee64da962dabf4eb8f700b72407772d591d73f52be2d4289
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956875"
---
# <a name="about-playlist-synchronization"></a>Acerca de la sincronización de listas de reproducción

Reproductor de Windows Media 10 o posterior está diseñado para sincronizar contenido multimedia digital con dispositivos mediante un modelo de sincronización de listas de reproducción. Esto significa que el contenido diseñado para copiarse en un dispositivo debe formar parte de una lista de reproducción. Cuando el usuario elige transferir contenido multimedia digital individual desde su equipo a un dispositivo, Reproductor de Windows Media agrega el contenido a una lista de reproducción predeterminada para la copia.

Las REPRODUCTOR DE WINDOWS MEDIA de sincronización de dispositivos están diseñadas para funcionar de esta forma. Al Reproductor de Windows Media, el programa puede presentar al usuario una lista de listas de reproducción que haya definido. A continuación, puede permitir que el usuario elija qué listas de reproducción se sincronizarán con un dispositivo determinado y para establecer el orden de prioridad para el proceso de sincronización.

Dado que los dispositivos portátiles tienen una capacidad de almacenamiento limitada, es posible que el usuario elija sincronizar más contenido multimedia digital del que el dispositivo puede almacenar. Reproductor de Windows Media el contenido en orden de prioridad. El usuario puede definir el orden de prioridad mediante un cuadro de diálogo al que se puede acceder desde la **característica Dispositivos.** En respuesta a la entrada del usuario en el programa, puede cambiar el orden de prioridad mediante programación cambiando los valores de determinados atributos de lista de reproducción. Colectivamente, estos atributos se denominan *atributos de* sincronización.

Cada lista de reproducción de una biblioteca tiene 16 atributos de sincronización: **Sync01** a **Sync16**. Cada atributo representa el dispositivo que tiene el índice de asociación correspondiente. El valor de cada atributo indica dos cosas:

-   Si la lista de reproducción debe sincronizarse con el dispositivo.
-   Valor de prioridad de la lista de reproducción.

Un valor de cero indica que Reproductor de Windows Media no debe intentar sincronizar la lista de reproducción con el dispositivo. Cualquier otro valor es un número de prioridad. Los valores más bajos reciben una prioridad mayor en el momento de la sincronización.

Las listas de reproducción también **tienen un atributo SyncOnly** que indica si la lista de reproducción solo está disponible para la sincronización.

Los elementos individuales del contenido multimedia digital también contienen metadatos sobre la sincronización. Al recuperar un objeto **Media** de la biblioteca, puede inspeccionar el valor del **atributo SyncState.** Este atributo proporciona información ampliada sobre si el contenido se ha copiado correctamente en el dispositivo o si se ha producido un error al copiar el contenido porque no encajaría.

> [!Note]  
> Debe evitar proporcionar elementos de interfaz de usuario que permitan al usuario crear listas de reproducción a partir de todo el contenido de la biblioteca para la sincronización.

 

Para optimizar el rendimiento, Reproductor de Windows Media un conjunto de reglas para crear listas de reproducción de sincronización. El programa solo debe crear listas de reproducción de sincronización para el contenido proporcionado. Permita Reproductor de Windows Media listas de reproducción de sincronización para el contenido que el usuario agregó a la biblioteca desde otros orígenes.

Como alternativa a la creación de su propia interfaz de usuario de lista de reproducción, puede presentar a los usuarios un cuadro de diálogo predeterminado para elegir listas de reproducción y administrar la asociación para un dispositivo. Para ello, llame a [IWMPSyncDevice::showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings). Al invocar este método, Reproductor de Windows Media muestra su configuración de sincronización. Cuando el usuario cierra el cuadro de diálogo, Reproductor de Windows Media automáticamente a su estado de acoplamiento anterior y pasa el control de nuevo al programa remoto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de la sincronización de dispositivos**](about-device-synchronization.md)
</dt> <dt>

[**Administración de listas de reproducción de sincronización**](managing-synchronization-playlists.md)
</dt> <dt>

[**Atributos de lista de reproducción**](playlist-attributes.md)
</dt> </dl>

 

 




