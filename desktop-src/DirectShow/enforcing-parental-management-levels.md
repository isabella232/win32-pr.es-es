---
description: Aplicar niveles de administración parental
ms.assetid: ad996a03-e94e-4743-90a2-aa390984a231
title: Aplicar niveles de administración parental
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7548721613c36369aaa34e5b5a62b665100e9495
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495515"
---
# <a name="enforcing-parental-management-levels"></a>Aplicar niveles de administración parental

A cualquier título o parte de un título de un disco DVD-Video se le puede asignar un nivel de administración parental (PML) genérico de 1 a 8. Cuando el navegador de DVD Lee contenido que tiene un PML, se dice que está en un *bloque parental*. Un bloque parental puede constar de una parte de un capítulo, varios capítulos o varios títulos. Una aplicación de DVD diseñada para un mercado internacional no debe codificar de forma rígida un sistema de clasificación determinado en su lógica de administración parental.

El navegador de DVD no aplica el PMLs; simplemente informa a la aplicación cuando encuentra información de PML en el disco. De forma predeterminada, omite esta información en el disco y reproduce el contenido de nivel más alto. Para aplicar el PMLs, la aplicación debe implementar alguna forma de lógica de control de contraseña que asocia los usuarios con los niveles. Indique al navegador de DVD que le envíe notificaciones de eventos de PML (llamando al método [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) en el inicio, con los parámetros DVD \_ NotifyParentalLevelChange y **true**) y responda a esos eventos para permitir o denegar el acceso según corresponda.

Un título de DVD puede tener un PML general, pero los autores de discos pueden dar a determinadas secciones de ese título una PMLs superior o más restrictiva. Se denominan comandos temporales de PML; Estos comandos siempre contienen dos instrucciones de bifurcación: una que se va a seguir si el comando PML temporal es aceptado por la aplicación de reproducción y el otro para seguir si se rechaza el comando. La secuencia de eventos es la siguiente. El navegador de DVD está leyendo el contenido de vídeo (dominio de título de DVD) cuando encuentra un comando PML temporal en el disco. Comprueba su marca interna para ver si la aplicación ha solicitado recibir notificaciones de este evento. Si no se establece la marca, el DVD continúa jugando, siguiendo la rama "el cambio de nivel de parental rechazado" especificado en el disco. Si se establece la marca, el DVD envía un \_ evento de \_ cambio de nivel parental de DVD \_ \_ a la aplicación y espera en un estado de pausa hasta que obtiene una respuesta. Cuando la aplicación recibe el evento, utiliza su propia lógica para determinar si se debe aceptar el comando. A continuación, llama a [**IDvdControl2:: AcceptParentalLevelChange**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-acceptparentallevelchange) con un argumento de **true** o **false**. Si **es true**, el explorador de DVD se reanudará la reproducción, siguiendo la rama "el cambio de nivel parental aceptado" especificado en el disco. En caso contrario, se reanuda la reproducción y se sigue la rama "el cambio de nivel paterno rechazado".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



