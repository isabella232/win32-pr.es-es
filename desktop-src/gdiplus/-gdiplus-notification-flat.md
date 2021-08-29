---
description: Funciones de notificación
ms.assetid: 44f69e05-1f08-48da-abb7-7e0a96c0cd26
title: Funciones de notificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6a0a45689bf7dbe4433b018e330278b9c275a567c47fbdd2aa1da82582df0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036493"
---
# <a name="notification-functions"></a>Funciones de notificación



| Función plana                                                                  | Método de contenedor                            | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdiplusNotificationHook(OUT ULONG \_ PTR \* token)<br/> | Los métodos de contenedor no llaman a .<br/> | La [**función GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) devuelve (en su parámetro de salida) un puntero a una [**estructura GdiplusStartupOutput.**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) Uno de los miembros de la estructura es un puntero a una función de enlace de notificación que tiene la misma firma que GdiplusNotificationHook.<br/> Hay dos maneras de llamar a la función de enlace de notificación; Puede usar el puntero devuelto por [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) o puede llamar a GdiplusNotificationHook. De hecho, GdiplusNotificationHook simplemente comprueba que ha suprimido el subproceso en segundo plano y, a continuación, llama a la función de enlace de notificación devuelta por **GdiplusStartup**.<br/> El parámetro de token recibe un identificador que más adelante debe pasar una llamada correspondiente a la función de desenlazón de notificación.<br/>                                                                                                                                         |
| VOID WINGDIPAPI GdiplusNotificationUnhook(token de ULONG \_ PTR)<br/>         | Los métodos de contenedor no llaman a .<br/> | La [**función GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) devuelve (en su parámetro de salida) un puntero a una [**estructura GdiplusStartupOutput.**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) Uno de los miembros de la estructura es un puntero a una función de unhook de notificación que tiene la misma firma que GdiplusNotificationUnhook.<br/> Hay dos maneras de llamar a la función unhook de notificación; Puede usar el puntero devuelto por [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) o puede llamar a GdiplusNotificationUnhook. De hecho, GdiplusNotificationUnhook simplemente comprueba que ha suprimido el subproceso en segundo plano y, a continuación, llama a la función de desenlazamiento de notificación que **devuelve GdiplusStartup.**<br/> Cuando llame a la función de desenlazón de notificación, pase el token que recibió anteriormente de una llamada correspondiente a la función de enlace de notificación. Si no lo hace, habrá pérdidas de recursos que no se limpiarán hasta que se cierre el proceso.<br/> |



 

 

 




