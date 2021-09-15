---
title: Recuperar información de estado
description: Recuperar información de estado
ms.assetid: 61561520-705a-4d06-a72c-c1cc6315f54e
keywords:
- Reproductor de Windows Media en línea,Download Manager
- online stores,Download Manager
- tipo 2 tiendas en línea, Administrador de descarga
- Reproductor de Windows Media en línea, recuperar el estado
- tiendas en línea, recuperar el estado
- tiendas en línea de tipo 2, recuperando el estado
- Reproductor de Windows Media,Download Manager
- Reproductor de Windows Media Administrador de descarga
- Administrador de descarga
- recuperación del estado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 155d1c9d949306ae5cda3ffff6a7a55fd3bae23c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476189"
---
# <a name="retrieving-status-information"></a>Recuperar información de estado

La información de estado se actualiza mediante el temporizador creado en la **función Init.** Todo el estado se actualiza con el mismo temporizador. El nombre de la función para el evento de temporizador es **OnTimer.**

**OnTimer** determina la información que se va a mostrar en función de la selección del usuario, que se almacena en la variable global denominada g \_ oCurrentDLItem. La función comprueba primero si los valores de tamaño o progreso son válidos y crea una cadena para cada caso.


```C++
var Size = g_oCurrentDLItem.size <=0 ? "Waiting..." : g_oCurrentDLItem.size + " bytes";
var Progress = g_oCurrentDLItem.progress <=0 ? "Waiting..." : g_oCurrentDLItem.progress + " bytes";

```



Si un valor es válido, la cadena representa el recuento de bytes. Si el valor no es válido, como -1, la cadena proporciona un mensaje para informar al usuario de que la información aún no está disponible.

A continuación, **un** bloque modificador determina si la descarga del elemento seleccionado se ha completado o cancelado. Si alguno de los casos es true, el valor de las variables Size o Progress se actualiza en consecuencia.


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

[**Uso del Administrador de descargas**](using-the-download-manager.md)
</dt> </dl>

 

 




