---
description: Funciones de notificación
ms.assetid: 44f69e05-1f08-48da-abb7-7e0a96c0cd26
title: Funciones de notificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84e5ca0bbcd9f2f184abd312fe15d4923e5cf14b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063431"
---
# <a name="notification-functions"></a>Funciones de notificación



| Función plana                                                                  | Método contenedor                            | Observaciones                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdiplusNotificationHook(token OUT ULONG \_ \* PTR)<br/> | Los métodos contenedor no llaman a .<br/> | La [**función GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) devuelve (en su parámetro de salida) un puntero a una [**estructura GdiplusStartupOutput.**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) Uno de los miembros de la estructura es un puntero a una función de enlace de notificación que tiene la misma firma que GdiplusNotificationHook.<br/> Hay dos maneras de llamar a la función de enlace de notificación; Puede usar el puntero devuelto por [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) o puede llamar a GdiplusNotificationHook. De hecho, GdiplusNotificationHook simplemente comprueba que se ha suprimido el subproceso en segundo plano y, a continuación, llama a la función de enlace de notificación devuelta por **GdiplusStartup**.<br/> El parámetro de token recibe un identificador que se debe pasar más adelante en una llamada correspondiente a la función de desenlaz de notificación.<br/>                                                                                                                                         |
| VOID WINGDIPAPI GdiplusNotificationUnhook(token de ULONG \_ PTR)<br/>         | Los métodos contenedor no llaman a .<br/> | La [**función GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) devuelve (en su parámetro de salida) un puntero a una [**estructura GdiplusStartupOutput.**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) Uno de los miembros de la estructura es un puntero a una función de desenlazamiento de notificación que tiene la misma firma que GdiplusNotificationUnhook.<br/> Hay dos maneras de llamar a la función de desenlaz de notificación; Puede usar el puntero devuelto por [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) o puede llamar a GdiplusNotificationUnhook. De hecho, GdiplusNotificationUnhook simplemente comprueba que ha suprimido el subproceso en segundo plano y, a continuación, llama a la función de desenlazamiento de notificación devuelta por **GdiplusStartup**.<br/> Cuando llame a la función de desenlaz de notificación, pase el token que recibió anteriormente de una llamada correspondiente a la función de enlace de notificación. Si no lo hace, habrá pérdidas de recursos que no se limpiarán hasta que se cierre el proceso.<br/> |



 

 

 




