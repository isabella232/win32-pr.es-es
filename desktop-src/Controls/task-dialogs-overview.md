---
title: Acerca de los cuadros de diálogo de tareas
description: Un cuadro de diálogo de tareas es el que se puede usar para mostrar información y recibir entradas sencillas del usuario.
ms.assetid: vs|controls|~\controls\toolbar\taskdialogsoverview.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eb5cafa452a4ed653c404d053e888c6de644236
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166925"
---
# <a name="about-task-dialogs"></a>Acerca de los cuadros de diálogo de tareas

Un cuadro de diálogo de tareas es el que se puede usar para mostrar información y recibir entradas sencillas del usuario. Al igual que un cuadro de mensaje, el sistema operativo le formatee según los parámetros establecidos. Sin embargo, un cuadro de diálogo de tarea tiene muchas más características que un cuadro de mensaje.

> [!Note]  
> Los diálogos de tareas requieren el modelo de apartamento de un solo subproceso (STA).

 

## <a name="parts-of-a-task-dialog"></a>Partes de un cuadro de diálogo de tarea

Un cuadro de diálogo de tarea consta de varios elementos, la mayoría de los cuales son opcionales. En la ilustración siguiente se muestran las distintas partes de un cuadro de diálogo de tarea.

![captura de pantalla de una ventana que muestra varios botones, incluido uno junto al texto de control contraído](images/taskdialog.jpg)

En la siguiente ilustración, el usuario ha hecho clic en el botón situado junto al texto del control contraído, lo que hace que el texto alternativo se muestre allí y en el pie de página.

![captura de pantalla de la ventana anterior, pero con dos líneas de texto de control expandido](images/taskdialogexpand.jpg)

En las ilustraciones se muestran las siguientes partes:



| Parte                   | Descripción                                                                                                                                                                                                                                                                                                                                                                          | Miembro TASKDIALOGCONFIG                                    |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Título de la ventana           | Título de la ventana.                                                                                                                                                                                                                                                                                                                                                               | **pszWindowTitle**                                         |
| Icono principal              | Icono grande que indica el propósito del cuadro de diálogo de tarea.                                                                                                                                                                                                                                                                                                                          | **hMainIcon** o **pszMainIcon**                           |
| Instrucción principal       | Texto principal.                                                                                                                                                                                                                                                                                                                                                                      | **pszMainInstruction**                                     |
| Contenido                | Texto adicional.                                                                                                                                                                                                                                                                                                                                                                          | **pszContent**                                             |
| Barra de progreso           | Una barra animada que muestra el progreso de alguna tarea.                                                                                                                                                                                                                                                                                                                                | **dwFlags**                                                |
| Botones de radio          | Opciones definidas por la aplicación para el usuario.                                                                                                                                                                                                                                                                                                                                            | **pRadioButtons**                                          |
| Botón Personalizado          | Botón que no es uno de los botones comunes. Puede ser un botón normal o, como se muestra en la ilustración, un vínculo de comando con hasta dos líneas de texto.                                                                                                                                                                                                                    | **pButtons**                                               |
| Botón Expandir o contraer | Botón que se puede usar para alternar entre el texto del control contraído definido por la aplicación (por ejemplo, "Ver más detalles") y el texto del control expandido, que puede estar en dos o más líneas. Cuando se expande el texto del control, también se muestra el texto adicional de **pszExpandedInformation,** ya sea después del texto del contenido o (como se muestra en la segunda ilustración) en el pie de página. | **pszCollapsedControlText** **y pszExpandedControlText** |
| Casilla de verificación | Casilla, acompañada de texto definido por la aplicación, para opciones sencillas como "No volver a mostrar este cuadro de diálogo".                                                                                                                                                                                                                                                                     | **pszVerificationText**                                    |
| Icono de pie de página            | Un pequeño icono que indica el propósito del texto del pie de página.                                                                                                                                                                                                                                                                                                                          | **hFooterIcon** o **pszFooterIcon**                       |
| Texto del pie de página            | Texto adicional. En las ilustraciones, el texto contiene un hipervínculo.                                                                                                                                                                                                                                                                                                                | **pszFooter**                                              |
| Botón Común          | Botón estándar; en las ilustraciones, el botón Aceptar.                                                                                                                                                                                                                                                                                                                              | **dwCommonButtons**                                        |



 

 

 




