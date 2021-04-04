---
description: Un controlador de interfaz de usuario (IU) externo puede devolver cualquier número de valores para Windows Installer en función del tipo de botón proporcionado en el parámetro de tipo de mensaje que el instalador pasa al controlador.
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: Devolver valores de un controlador de interfaz de usuario externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b466f6bc3cc034551a01bd2b87caa7292824e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811803"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a>Devolver valores de un controlador de interfaz de usuario externo

Un controlador de interfaz de usuario (IU) externo puede devolver cualquier número de valores para Windows Installer en función del tipo de botón proporcionado en el parámetro de tipo de mensaje que el instalador pasa al controlador.

El controlador de la interfaz de usuario externa puede devolver los valores-1 y 0 en cualquier momento, ya que no están relacionados con los tipos de botón. Un valor devuelto de – 1 indica que se ha producido un error interno en el controlador de la interfaz de usuario externa. Un valor devuelto de 0 indica que el controlador de la interfaz de usuario externa no ha controlado el mensaje del instalador y el instalador debe controlar el mensaje en su lugar.

En el caso de los mensajes que no incluyen un tipo de botón, como INSTALLMESSAGE \_ ACTIONDATA y INSTALLMESSAGE \_ Progress, la devolución de IDCANCEL cancela la instalación. Al devolver IDOK, se notifica al instalador que el controlador de la interfaz de usuario externa controló el mensaje.

Los valores devueltos restantes, como se describe a continuación, se relacionan directamente con los tipos de botón que se incluyen con el tipo de mensaje.



| Valor devuelto de IU externa | Significado                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| IDOK                     | El usuario presionó el botón **Aceptar** . Se entendió la información del mensaje.                     |
| IDCANCEL                 | Se presionó el botón **Cancelar** . Cancele la instalación.                                            |
| IDABORT                  | Se presionó el botón **anular** . Cancele la instalación.                                              |
| IDRETRY                  | Se presionó el botón **Reintentar** . Vuelva a intentar la acción.                                                |
| IDIGNORE                 | Se presionó el botón **omitir** . Omita el error y continúe.                                      |
| IDYES                    | Se presionó el botón **sí** . Respuesta afirmativa, continuar con la secuencia de eventos actual.   |
| IDNO                     | Se presionó el botón **no** . La respuesta negativa, no continuar con la secuencia de eventos actual. |



 

Por ejemplo, si se envía un mensaje al controlador de la interfaz de usuario externa con la \_ marca de estilos de cuadro de mensaje MB ABORTRETRYIGNORE, el controlador de la interfaz de usuario externa puede devolver uno de los siguientes valores:

-   – 1 (error en el controlador de la interfaz de usuario externa)
-   0 (no se realiza ninguna acción en el controlador de la interfaz de usuario externa, se deja Windows Installer controlar)
-   IDABORT (botón de **anulación** presionado)
-   IDRETRY (botón **Reintentar** presionado)
-   IDIGNORE (botón **omitir** presionado)

 

 



