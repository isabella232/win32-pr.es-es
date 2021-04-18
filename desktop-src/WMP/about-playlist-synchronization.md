---
title: Acerca de la sincronización de listas de reproducción
description: Acerca de la sincronización de listas de reproducción
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Windows Media Player, sincronización de listas de reproducción
- Modelo de objetos de Windows Media Player, sincronización de listas de reproducción
- modelo de objetos, sincronización de listas de reproducción
- Control ActiveX de Windows Media Player, sincronización de listas de reproducción
- Control ActiveX, sincronización de listas de reproducción
- Control ActiveX móvil de Windows Media Player, sincronización de listas de reproducción
- Windows Media Player Mobile, sincronización de listas de reproducción
- sincronizar dispositivos, listas de reproducción
- sincronización de dispositivos, listas de reproducción
- listas de reproducción, sincronización
- Listas de reproducción de metarchivos de Windows Media, sincronización
- listas de reproducción de metarchivos, sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc019b31518fda1a49c8d3ae86f2d03c4ecefc8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358676"
---
# <a name="about-playlist-synchronization"></a>Acerca de la sincronización de listas de reproducción

Windows Media Player 10 o posterior está diseñado para sincronizar el contenido multimedia digital con los dispositivos mediante un modelo de sincronización de listas de reproducción. Esto significa que el contenido destinado a copiarse en un dispositivo debe formar parte de una lista de reproducción. Cuando el usuario elige transferir contenido multimedia digital individual desde su equipo a un dispositivo, Windows Media Player agrega el contenido a una lista de reproducción predeterminada para copiarlo.

Las API de sincronización de dispositivos de Windows Media Player están diseñadas para funcionar como esto también. Al igual que Windows Media Player, el programa puede presentar al usuario una lista de listas de reproducción que ha definido. Después, puede permitir que el usuario elija qué listas de reproducción se van a sincronizar con un dispositivo determinado y establecer el orden de prioridad para el proceso de sincronización.

Dado que los dispositivos portátiles tienen una capacidad de almacenamiento limitada, es posible que el usuario elija sincronizar más contenido multimedia digital que el dispositivo que puede almacenar. Windows Media Player sincroniza el contenido en orden de prioridad. El usuario puede definir el orden de prioridad mediante el uso de un cuadro de diálogo al que se puede tener acceso desde la característica **dispositivos** . En respuesta a la entrada del usuario en el programa, puede cambiar el orden de prioridad mediante programación cambiando los valores de determinados atributos de la lista de reproducción. Colectivamente, estos atributos se denominan atributos de *sincronización* .

Cada lista de reproducción de una biblioteca tiene 16 atributos de sincronización: **Sync01** a **Sync16**. Cada atributo representa el dispositivo que tiene el índice de asociación correspondiente. El valor de cada atributo le indica dos cosas:

-   Si la lista de reproducción se debe sincronizar con el dispositivo.
-   Valor de prioridad para la lista de reproducción.

Un valor de cero indica que Windows Media Player no debe intentar sincronizar la lista de reproducción con el dispositivo. Cualquier otro valor es un número de prioridad. Los valores inferiores reciben mayor prioridad en el momento de la sincronización.

Las listas de reproducción también tienen un atributo **SyncOnly** que indica si la lista de reproducción solo está disponible para la sincronización.

Los elementos individuales de contenido multimedia digital contienen metadatos sobre la sincronización también. Al recuperar un objeto **multimedia** de la biblioteca, puede inspeccionar el valor del atributo **SyncState** . Este atributo proporciona información ampliada sobre si el contenido se ha copiado correctamente en el dispositivo o si se ha producido un error en la copia del contenido porque no cabe.

> [!Note]  
> Debe evitar proporcionar elementos de la interfaz de usuario que permitan al usuario crear listas de reproducción a partir de todo el contenido de la biblioteca para la sincronización.

 

Para optimizar el rendimiento, Windows Media Player aplica un conjunto de reglas para crear listas de reproducción de sincronización. El programa solo debe crear listas de reproducción de sincronización para el contenido proporcionado. Esta opción permite a Windows Media Player crear listas de reproducción de sincronización para el contenido que el usuario agregó a la biblioteca desde otros orígenes.

Como alternativa a la creación de su propia interfaz de usuario de lista de reproducción, puede presentar a los usuarios un cuadro de diálogo predeterminado para elegir listas de reproducción y administrar la Asociación de un dispositivo. Para ello, llame a [IWMPSyncDevice:: showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings). Al invocar este método, Windows Media Player muestra el cuadro de diálogo Configuración de sincronización. Cuando el usuario cierra el cuadro de diálogo, Windows Media Player vuelve automáticamente a su estado de acoplamiento anterior y vuelve a pasar el control al programa remoto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de la sincronización de dispositivos**](about-device-synchronization.md)
</dt> <dt>

[**Administrar listas de reproducción de sincronización**](managing-synchronization-playlists.md)
</dt> <dt>

[**Atributos de lista de reproducción**](playlist-attributes.md)
</dt> </dl>

 

 




