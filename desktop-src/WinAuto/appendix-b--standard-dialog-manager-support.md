---
title: Apéndice B compatibilidad del administrador de cuadros de diálogo estándar
description: Microsoft Active Accessibility proporciona compatibilidad completa para los controles de cuadro de diálogo del administrador de cuadros de diálogo estándar (SDM).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a710b7f35a242badbff6295d1af0d08cada13fa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776404"
---
# <a name="appendix-b-standard-dialog-manager-support"></a>Apéndice B: compatibilidad con el administrador de cuadros de diálogo estándar

Microsoft Active Accessibility proporciona compatibilidad completa para los controles de cuadro de diálogo del administrador de cuadros de diálogo estándar (SDM). SDM es una biblioteca de código de Microsoft interna que proporciona a las aplicaciones de Microsoft un grado de independencia de las diferencias entre los sistemas operativos Macintosh y Microsoft Windows. SDM se usa principalmente para cuadros de diálogo de Microsoft Excel y Microsoft Word.

SDM presenta problemas para las ayudas de accesibilidad porque utiliza implementaciones no estándar de cuadros de diálogo. Por ejemplo, los botones del cuadro de diálogo SDM no utilizan los identificadores de ventana del mismo modo que los elementos de la interfaz de usuario estándar. No se pueden enviar mensajes a botones y botones no se incluyen en la lista de ventanas. Una aplicación que usa SDM se comunica con el control a través de una interfaz privada.

En la ilustración siguiente se muestra un cuadro de diálogo de ejemplo de Word. Aunque parece un cuadro de diálogo normal de Windows que usa el control de pestañas, en realidad es un cuadro de diálogo de SDM.

![captura de pantalla del cuadro de diálogo Opciones con la pestaña vista seleccionada](images/dialog.gif)

 

 




