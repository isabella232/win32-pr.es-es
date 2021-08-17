---
title: Apéndice B Compatibilidad con el administrador de diálogos estándar
description: Microsoft Active Accessibility proporciona compatibilidad completa con los controles de cuadro de diálogo del Administrador de diálogos estándar (SDM).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b6500cabf4820fffe12b7ef160f2e494e43db067f6b96409dee02bbfd6119e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326831"
---
# <a name="appendix-b-standard-dialog-manager-support"></a>Apéndice B: Compatibilidad con el Administrador de diálogos estándar

Microsoft Active Accessibility proporciona compatibilidad completa con los controles de cuadro de diálogo del Administrador de diálogos estándar (SDM). SDM es una biblioteca de código interna de Microsoft que proporciona a las aplicaciones de Microsoft un grado de independencia de las diferencias entre macintosh y microsoft Windows sistemas operativos. SDM se usa principalmente para los cuadros de diálogo de Microsoft Excel y Microsoft Word.

SDM presenta problemas de ayuda de accesibilidad porque usa implementaciones no estándar de cuadros de diálogo. Por ejemplo, los botones del cuadro de diálogo SDM no usan identificadores de ventana de la misma manera que los elementos de la interfaz de usuario estándar. No se pueden enviar mensajes a botones y los botones no están incluidos en la lista de ventanas. Una aplicación que usa SDM se comunica con el control a través de una interfaz privada.

En la ilustración siguiente se muestra un cuadro de diálogo de ejemplo de Word. Aunque parece un cuadro de Windows normal que usa el control de ficha, es realmente un cuadro de diálogo SDM.

![captura de pantalla del cuadro de diálogo opciones con la pestaña Vista seleccionada](images/dialog.gif)

 

 




