---
description: Las aplicaciones que usan las funciones de API Unicode y juego de caracteres suelen usar la misma clase de ventana. El sistema operativo traduce de forma transparente los mensajes entre ventanas de diferentes clases.
ms.assetid: 68e9839b-39f8-411a-8ae4-4a627c667cae
title: Traducción automática de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b02a5c5a4951189333608aa448f09ba9c6866d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274855"
---
# <a name="automatic-message-translation"></a>Traducción automática de mensajes

Las aplicaciones que usan las funciones de API Unicode y juego de caracteres suelen usar la misma clase de ventana. El sistema operativo traduce de forma transparente los mensajes entre ventanas de diferentes clases.

Se implementa una función de ventana para recibir mensajes en formato Unicode Windows página de códigos. La función de ventana puede enviar mensajes o llamar a funciones de cualquier tipo.

Los mensajes siguientes tienen argumentos de texto y están sujetos a la traducción automática de texto. Para obtener información sobre la traducción automática, vea [Subclases y Traducción automática de mensajes.](subclassing-and-automatic-message-translation.md)

<dl>

[CB \_ ADDSTRING](../controls/cb-addstring.md)  
[CB \_ DIR](../controls/cb-dir.md)  
[CB \_ FINDSTRING](../controls/cb-findstring.md)  
[CB \_ GETLBTEXT](../controls/cb-getlbtext.md)  
[CB \_ INSERTSTRING](../controls/cb-insertstring.md)  
[CB \_ SELECTSTRING](../controls/cb-selectstring.md)  
[EM \_ GETLINE](../controls/em-getline.md)  
[EM \_ REPLACESEL](../controls/em-replacesel.md)  
[EM \_ SETPASSWORDCHAR](../controls/em-setpasswordchar.md)  
[LB \_ ADDFILE](../controls/lb-addfile.md)  
[LB \_ ADDSTRING](../controls/lb-addstring.md)  
[LB \_ DIR](../controls/lb-dir.md)  
[LB \_ FINDSTRING](../controls/lb-findstring.md)  
[LB \_ GETTEXT](../controls/lb-gettext.md)  
[LB \_ INSERTSTRING](../controls/lb-insertstring.md)  
[LB \_ SELECTSTRING](../controls/lb-selectstring.md)  
[WM \_ ASKCBFORMATNAME](../dataxchg/wm-askcbformatname.md)  
[WM \_ CHAR](../inputdev/wm-char.md)  
[WM \_ CHARTOITEM](../controls/wm-chartoitem.md)  
[WM \_ CREATE](../winmsg/wm-create.md)  
[WM \_ DEADCHAR](../inputdev/wm-deadchar.md)  
[WM \_ DEVMODECHANGE](../gdi/wm-devmodechange.md)  
[WM \_ GETTEXT](../winmsg/wm-gettext.md)  
[WM \_ MDICREATE](../winmsg/wm-mdicreate.md)  
[WM \_ MENUCHAR](../menurc/wm-menuchar.md)  
[WM \_ NCCREATE](../winmsg/wm-nccreate.md)  
[WM \_ SETTEXT](../winmsg/wm-settext.md)  
[WM \_ SYSCHAR](../menurc/wm-syschar.md)  
[WM \_ SYSDEADCHAR](../inputdev/wm-sysdeadchar.md)  
[WM \_ WININICHANGE](../winmsg/wm-wininichange.md)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Unicode en la API de Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
