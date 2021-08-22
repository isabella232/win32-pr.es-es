---
description: Un controlador de interfaz de usuario (UI) externo puede devolver cualquier número de valores a Windows Installer según el tipo de botón proporcionado en el parámetro de tipo de mensaje que el instalador pasa al controlador.
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: Devolver valores de un controlador de Interfaz de usuario externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b4ba5edcd87b0d4f324762f840c117425b322ea03d1dd15e103c05bcf12352
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626085"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a>Devolver valores de un controlador de Interfaz de usuario externo

Un controlador de interfaz de usuario (UI) externo puede devolver cualquier número de valores a Windows Installer según el tipo de botón proporcionado en el parámetro de tipo de mensaje que el instalador pasa al controlador.

El controlador de interfaz de usuario externo puede devolver los valores –1 y 0 en cualquier momento porque no están relacionados con los tipos de botón. Un valor devuelto de –1 indica que se produjo un error interno en el controlador de interfaz de usuario externo. Un valor devuelto de 0 indica que el controlador de interfaz de usuario externo no ha manipulado el mensaje del instalador y, en su lugar, el instalador debe controlar el mensaje.

Para los mensajes que no incluyen un tipo de botón, como INSTALLMESSAGE ACTIONDATA e \_ INSTALLMESSAGE PROGRESS, devolver \_ IDCANCEL cancela la instalación. Al devolver IDOK, se notifica al instalador que el controlador de interfaz de usuario externo controló el mensaje.

Los valores devueltos restantes, como se describe a continuación, están directamente relacionados con los tipos de botón que se incluyen con el tipo de mensaje.



| Valor devuelto de la interfaz de usuario externa | Significado                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| IDOK                     | El **usuario** presionó el botón Aceptar. Se ha comprendido la información del mensaje.                     |
| IDCANCEL                 | Se **presionó** el botón CANCELAR. Cancele la instalación.                                            |
| IDABORT                  | Se presionó el botón **ABORT.** Anule la instalación.                                              |
| IDRETRY                  | Se presionó el botón **RETRY.** Vuelva a intentar la acción.                                                |
| IDIGNORE                 | Se **presionó** el botón IGNORE. Ignore el error y continúe.                                      |
| IDYES                    | Se **presionó** el botón SÍ. La respuesta afirmativa, continúe con la secuencia actual de eventos.   |
| IDNO                     | Se **presionó** el botón NO. La respuesta negativa, no continúe con la secuencia actual de eventos. |



 

Por ejemplo, si el controlador de interfaz de usuario externo se envía un mensaje con la marca de estilos de cuadro de mensaje ABORTRETRYIGNORE de MB, el controlador de interfaz de usuario externo puede devolver uno de \_ los valores siguientes:

-   –1 (error en el controlador de interfaz de usuario externo)
-   0 (no se ha realizado ninguna acción en el controlador de interfaz de usuario externo, deje que Windows installer lo controle)
-   IDABORT **(botón ABORT** presionado)
-   IDRETRY **(botón REINTENTAR** presionado)
-   IDIGNORE **(botón IGNORE** presionado)

 

 



