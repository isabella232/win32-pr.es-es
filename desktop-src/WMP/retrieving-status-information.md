---
title: Recuperando información de estado
description: Recuperando información de estado
ms.assetid: 61561520-705a-4d06-a72c-c1cc6315f54e
keywords:
- Windows Media Player tiendas en línea, administrador de descargas
- tiendas en línea, administrador de descargas
- tipo 2 tiendas en línea, administrador de descargas
- Windows Media Player tiendas en línea, recuperar el estado
- tiendas en línea, recuperar estado
- tipo 2 tiendas en línea, recuperando estado
- Windows Media Player, administrador de descargas
- Administrador de descargas de Windows Media Player
- Administrador de descargas
- recuperando estado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 155d1c9d949306ae5cda3ffff6a7a55fd3bae23c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778258"
---
# <a name="retrieving-status-information"></a>Recuperando información de estado

La información de estado se actualiza mediante el temporizador creado en la función **init** . Todo el estado se actualiza con el mismo temporizador. El nombre de la función para el evento del temporizador es **Altimer**.

**Altimer** determina la información que se va a mostrar en función de la selección del usuario, que se almacena en la variable global denominada g \_ oCurrentDLItem. La función comprueba primero si los valores de tamaño o progreso son válidos y crea una cadena para cada caso.


```C++
var Size = g_oCurrentDLItem.size <=0 ? "Waiting..." : g_oCurrentDLItem.size + " bytes";
var Progress = g_oCurrentDLItem.progress <=0 ? "Waiting..." : g_oCurrentDLItem.progress + " bytes";

```



Si un valor es válido, la cadena representa el recuento de bytes. Si el valor no es válido, como-1, la cadena proporciona un mensaje para informar al usuario de que la información aún no está disponible.

Después, un bloque **Switch** determina si la descarga del elemento seleccionado se ha completado o cancelado. Si alguna de las mayúsculas y minúsculas es true, el valor de las variables size o Progress se actualiza en consecuencia.


```C++
switch(g_oCurrentDLItem.downloadState)
{
    case 3:            
        Size = "Completed";
        Progress = "Completed";
        break;
        
    case 4:
        Size = "Canceled";
        Progress = "Canceled";
        break;
        
    default:
        break;                
}

```



Por último, la información de estado se muestra en el elemento DIV denominado dlstate.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del administrador de descargas**](using-the-download-manager.md)
</dt> </dl>

 

 




