---
description: Una función del instalador puede mostrar un cuadro de diálogo de mensaje de error que devuelve cualquiera de los errores siguientes. Solo se muestra un cuadro de error si el nivel de interfaz de usuario está en el nivel completo, reducido o básico. Para obtener más información, vea Interfaz de usuario niveles.
ms.assetid: 0153a21f-9b26-4088-b12b-96c9e6918cc3
title: Mensajes de error mostrados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4e339a67f054134b4e2462593682cbdeac8d6eb7be63fefd93fd32d504f5e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745385"
---
# <a name="displayed-error-messages"></a>Mensajes de error mostrados

Una [función del instalador](installer-function-reference.md) puede mostrar un cuadro de diálogo de mensaje de error que devuelve cualquiera de los errores siguientes. Solo se muestra un cuadro de error si el nivel de interfaz de usuario está en el nivel completo, reducido o básico. Para obtener más información, [vea Interfaz de usuario Levels](user-interface-levels.md).

Las funciones del instalador solo muestran mensajes de error que se encuentran en la tabla siguiente. En el caso de los errores que no están en esta lista, el autor de la llamada de la función es responsable de controlar la presentación de mensajes de error.



| Código de error               | Error                        |
|--------------------------|------------------------------|
| ERROR \_ INSTALL \_ SUSPEND  | La instalación se suspendió.   |
| ERROR \_ AL \_ INSTALAR USEREXIT | El usuario ha salido de la instalación. |
| ERROR \_ DE INSTALACIÓN \_  | Error de instalación.              |



 

 

 



