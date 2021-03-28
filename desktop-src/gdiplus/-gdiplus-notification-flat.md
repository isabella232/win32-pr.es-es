---
description: Funciones de notificación
ms.assetid: 44f69e05-1f08-48da-abb7-7e0a96c0cd26
title: Funciones de notificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84e5ca0bbcd9f2f184abd312fe15d4923e5cf14b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156180"
---
# <a name="notification-functions"></a>Funciones de notificación



| Función plana                                                                  | Wrapper (método)                            | Observaciones                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdiplusNotificationHook (OUT ULONG \_ ptr \* token)<br/> | No lo llaman los métodos contenedores.<br/> | La función [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) devuelve (en su parámetro de salida) un puntero a una estructura [**GdiplusStartupOutput**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) . Uno de los miembros de la estructura es un puntero a una función de enlace de notificación que tiene la misma firma que GdiplusNotificationHook.<br/> Hay dos maneras de llamar a la función de enlace de notificación: puede usar el puntero devuelto por [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) o puede llamar a GdiplusNotificationHook. De hecho, GdiplusNotificationHook simplemente comprueba que ha suprimido el subproceso en segundo plano y, a continuación, llama a la función de enlace de notificación que devuelve **GdiplusStartup**.<br/> El parámetro token recibe un identificador que posteriormente debe pasar en una llamada correspondiente a la función de desenlace de notificación.<br/>                                                                                                                                         |
| VOID WINGDIPAPI GdiplusNotificationUnhook (ULONG \_ ptr token)<br/>         | No lo llaman los métodos contenedores.<br/> | La función [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) devuelve (en su parámetro de salida) un puntero a una estructura [**GdiplusStartupOutput**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) . Uno de los miembros de la estructura es un puntero a una función de desenlace de notificación que tiene la misma firma que GdiplusNotificationUnhook.<br/> Hay dos maneras de llamar a la función de desenlace de notificación; puede usar el puntero devuelto por [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) o puede llamar a GdiplusNotificationUnhook. De hecho, GdiplusNotificationUnhook simplemente comprueba que se ha suprimido el subproceso en segundo plano y, a continuación, llama a la función de desenlace de notificación que devuelve **GdiplusStartup**.<br/> Cuando llame a la función de desenlace de notificación, pase el token que recibió anteriormente desde una llamada correspondiente a la función de enlace de notificación. Si no lo hace, habrá fugas de recursos que no se limpiarán hasta que se cierre el proceso.<br/> |



 

 

 




