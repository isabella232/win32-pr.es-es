---
description: Aplicación de los niveles de administración parental
ms.assetid: ad996a03-e94e-4743-90a2-aa390984a231
title: Aplicación de los niveles de administración parental
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7548721613c36369aaa34e5b5a62b665100e9495
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169990"
---
# <a name="enforcing-parental-management-levels"></a>Aplicación de los niveles de administración parental

A cualquier título o parte de un título de un disco DVD-Video se le puede asignar un nivel de administración parental genérico (PML) de 1 a 8. Cuando el navegador de DVD está leyendo contenido que tiene una PML, se dice que está en un *bloque parental*. Un bloque parental puede constar de parte de un capítulo, varios capítulos o varios títulos. Una aplicación de DVD destinada a un mercado internacional no debe codificar un sistema de clasificación determinado en su lógica de administración parental.

El propio navegador de DVD no aplica las PML; simplemente informa a la aplicación cuando encuentra información de PML en el disco. De forma predeterminada, omite esta información en el disco y reproduce el contenido de nivel superior. Para aplicar las PML, la aplicación debe implementar algún tipo de lógica de control de contraseñas que asocie a los usuarios con niveles, indicar al navegador de DVD que le envíe notificaciones de eventos PML (llamando al método [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) al iniciarse, con los parámetros DVD \_ NotifyParentalLevelChange y **TRUE)** y responder a esos eventos para permitir o no permitir el acceso según corresponda.

Un título de DVD puede tener una PML general, pero los autores de discos pueden dar a determinadas secciones de ese título valores superiores o más restrictivos. Se denominan comandos de PML temporales; Estos comandos siempre contienen dos instrucciones de bifurcación: una para seguir si la aplicación del reproductor acepta el comando pml temporal y la otra para seguir si se rechaza el comando. La secuencia de eventos es la siguiente. El navegador de DVD está leyendo contenido de vídeo (dominio de título de DVD) cuando encuentra un comando pml temporal en el disco. Comprueba su marca interna para ver si la aplicación ha solicitado que se le notifique de este evento. Si no se establece la marca, el DVD continúa reproduciendo, siguiendo la rama "Cambio de nivel parental rechazado" especificada en el disco. Si se establece la marca, el DVD envía un evento EC DVD PARENTAL LEVEL CHANGE a la aplicación y espera en un estado en pausa hasta que \_ \_ recibe una \_ \_ respuesta. Cuando la aplicación recibe el evento, usa su propia lógica para determinar si se acepta el comando. A continuación, [**llama a IDvdControl2::AcceptParentalLevelChange con**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-acceptparentallevelchange) un argumento de **TRUE** o **FALSE.** Si **es TRUE,** el navegador de DVD reanuda la reproducción, siguiendo la rama "Se aceptó el cambio de nivel parental" especificada en el disco. De lo contrario, reanuda la reproducción y sigue la rama "Cambio de nivel parental rechazado".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



