---
description: Las notificaciones son valores que una función de instalación envía a una rutina de devolución de llamada para especificar un estado o evento. Dos parámetros, Param1 y Param2, se envían con la notificación y contienen información adicional relevante para la notificación.
ms.assetid: 93434558-ae83-4ea2-9324-659e5873a8c3
title: Notificaciones (API de instalación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f602e2062be01e3f521147d7a820d3afc1424f5421667716d3f8d4273f0dd866
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992665"
---
# <a name="notifications-setup-api"></a>Notificaciones (API de instalación)

Las notificaciones son valores que una función de instalación envía a una rutina de devolución de llamada para especificar un estado o evento. Dos parámetros, *Param1* y *Param2,* se envían con la notificación y contienen información adicional relevante para la notificación.

La rutina de devolución de llamada procesa la notificación y devuelve un entero sin signo a la función de configuración. Dependiendo de la función de configuración, puede usar este valor para especificar una operación o selección de usuario, o bien puede omitirla.

Las funciones de instalación envían notificaciones a rutinas de devolución de llamada mediante la sintaxis siguiente.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //notification code
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

El *parámetro Context* es un puntero void a una variable de contexto o estructura que la rutina de devolución de llamada puede usar para almacenar información que debe persistir entre las llamadas posteriores a la rutina de devolución de llamada.

Dado que la rutina de devolución de llamada especifica la implementación del contexto y las funciones de configuración nunca hacen referencia a ella ni la modifican, el contexto no se documenta en el material de referencia para los mensajes de notificación siguientes.

El *parámetro Notification* especifica un valor entero sin signo para un evento o estado que hace que la función de instalación llame a la rutina de devolución de llamada.

*Param1* y *Param2* son parámetros opcionales que pueden contener información adicional relevante para la notificación. Estos parámetros son enteros sin signo. Si *Param1* o *Param2* devuelven información que no es un entero sin signo, se convierte en un entero sin signo y se debe volver a convertir a su tipo de datos original antes de que la rutina de devolución de llamada la pueda usar.

> [!Note]  
> Las siguientes notificaciones representan todas las notificaciones que usan las funciones de configuración. Las funciones individuales usan un subconjunto de estas notificaciones. En otras palabras, no todas las funciones usan todas las notificaciones.

 

Las funciones de instalación usan las siguientes notificaciones.



| Notificación                                                                     | Descripción                                                                                   |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md)                        | Error durante una operación de copia de archivos.                                               |
| [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)                    | Error durante una operación de eliminación de archivos.                                           |
| [**SPFILENOTIFY \_ ENDCOPY**](spfilenotify-endcopy.md)                            | Ha finalizado una operación de copia de archivos.                                                              |
| [**SPFILENOTIFY \_ ENDDELETE**](spfilenotify-enddelete.md)                        | Ha finalizado una operación de eliminación de archivos.                                                          |
| [**SPFILENOTIFY \_ ENDQUEUE**](spfilenotify-endqueue.md)                          | La cola ha terminado de confirmarse.                                                            |
| [**SPFILENOTIFY \_ ENDREGISTRATION**](spfilenotify-endregistration.md)            | El registro o anulación del registro del archivo ha finalizado.                                  |
| [**SPFILENOTIFY \_ ENDRENAME**](spfilenotify-endrename.md)                        | Ha finalizado una operación de cambio de nombre de archivo.                                                            |
| [**SPFILENOTIFY \_ ENDSUBQUEUE**](spfilenotify-endsubqueue.md)                    | Ha finalizado una subcola (copiar, cambiar nombre o eliminar).                                         |
| [**SPFILENOTIFY \_ FILEEXTRACTED**](spfilenotify-fileextracted.md)                | El archivo se ha extraído del archivador.                                                 |
| [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)                | Se encuentra un archivo en el archivador.                                                         |
| [**SPFILENOTIFY \_ FILEOPDELAYED**](spfilenotify-fileopdelayed.md)                | El archivo estaba en uso y la operación actual se ha retrasado hasta que se reinicia el sistema. |
| [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)                  | El idioma de la operación actual no coincide con el idioma del sistema.                     |
| [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md)                        | Se requieren nuevos medios de origen.                                                                 |
| [**SPFILENOTIFY \_ NEEDNEWCABINET**](spfilenotify-neednewcabinet.md)              | El archivo actual continúa en el siguiente archivador.                                            |
| [**SPFILENOTIFY \_ QUEUESCAN**](spfilenotify-queuescan.md)                        | Se ha examinado un nodo de la cola de archivos.                                                    |
| [**SPFILENOTIFY \_ QUEUESCAN \_ EX**](spfilenotify-queuescan-ex.md)                 | Se ha examinado un nodo de la cola de archivos.                                                    |
| [**SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO**](spfilenotify-queuescan-signerinfo.md) | Se ha examinado un nodo de la cola de archivos.                                                    |
| [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md)                    | Error durante una operación de cambio de nombre de archivo.                                             |
| [**SPFILENOTIFY \_ STARTCOPY**](spfilenotify-startcopy.md)                        | Se ha iniciado una operación de copia de archivos.                                                            |
| [**SPFILENOTIFY \_ STARTDELETE**](spfilenotify-startdelete.md)                    | Se ha iniciado una operación de eliminación de archivos.                                                          |
| [**SPFILENOTIFY \_ STARTQUEUE**](spfilenotify-startqueue.md)                      | La cola ha empezado a confirmarse.                                                              |
| [**SPFILENOTIFY \_ STARTREGISTRATION**](spfilenotify-startregistration.md)        | Se ha iniciado el registro o la anulación del registro del archivo.                                   |
| [**SPFILENOTIFY \_ STARTRENAME**](spfilenotify-startrename.md)                    | Se ha iniciado una operación de cambio de nombre de archivo.                                                          |
| [**SPFILENOTIFY \_ STARTSUBQUEUE**](spfilenotify-startsubqueue.md)                | Se ha iniciado una subcola (copiar, cambiar nombre o eliminar).                                       |
| [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)                  | Ya existe una copia del archivo especificado en el destino.                                    |
| [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)                    | Existe una versión más reciente del archivo especificado en el destino.                                   |



 

 

 



