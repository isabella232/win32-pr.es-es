---
description: 'Windows Las funciones y los métodos de adquisición de imágenes (WIA) pueden devolver códigos de error de la lista siguiente: Error CodeMeaningCodeWIA ERROR BUSYEl dispositivo \_ \_ está ocupado.'
ms.assetid: 3abbe92b-32b7-4820-b208-45c847243078
title: Códigos de error (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6025616d46a5973692bb3cafbcf88e18836ad0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251841"
---
# <a name="error-codes-wia"></a>Códigos de error (WIA)

Windows Las funciones y los métodos de adquisición de imágenes (WIA) pueden devolver códigos de error de la lista siguiente: 

| Código de error                                      | Significado                                                                                                                                                                                                                             | Código       |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| ERROR DE WIA \_ \_ OCUPADO                                | El dispositivo está ocupado. Cierre las aplicaciones que usan este dispositivo o espere a que finalice y vuelva a intentarlo.                                                                                                                          | 0x80210006 |
| WIA \_ ERROR \_ COVER \_ OPEN                         | Una o varias de las portadas del dispositivo están abiertas.                                                                                                                                                                                          | 0x80210016 |
| COMUNICACIÓN DEL \_ DISPOSITIVO CON ERRORES \_ DE WIA \_               | Error de comunicación con el dispositivo WIA. Asegúrese de que el dispositivo está encendido y conectado al equipo. Si el problema persiste, desconecte y vuelva a conectar el dispositivo.                                                            | 0x8021000A |
| DISPOSITIVO DE ERROR DE WIA \_ \_ \_ BLOQUEADO                      | El dispositivo está bloqueado. Cierre las aplicaciones que usan este dispositivo o espere a que finalice y vuelva a intentarlo.                                                                                                                        | 0x8021000D |
| EXCEPCIÓN DE ERROR DE WIA \_ \_ EN EL \_ \_ CONTROLADOR               | El controlador del dispositivo produjo una excepción.                                                                                                                                                                                               | 0x8021000E |
| ERROR \_ GENERAL DE WIA \_ \_                      | Se ha producido un error desconocido con el dispositivo WIA.                                                                                                                                                                                  | 0x80210001 |
| ERROR DE WIA \_ \_ CONFIGURACIÓN DE HARDWARE \_ \_ INCORRECTA        | Hay una configuración incorrecta en el dispositivo WIA.                                                                                                                                                                                    | 0x8021000C |
| COMANDO NO \_ VÁLIDO DE ERROR \_ DE WIA \_                    | El dispositivo no admite este comando.                                                                                                                                                                                            | 0x8021000B |
| ERROR DE WIA \_ RESPUESTA DEL CONTROLADOR NO \_ \_ \_ VÁLIDA           | La respuesta del controlador no es válida.                                                                                                                                                                                            | 0x8021000F |
| ELEMENTO DE ERROR DE WIA \_ \_ \_ ELIMINADO                       | Se eliminó el dispositivo WIA. Ya no está disponible.                                                                                                                                                                               | 0x80210009 |
| WIA \_ ERROR \_ LAMP \_ OFF                           | La luz del analizador está apagada.                                                                                                                                                                                                          | 0x80210017 |
| CONTADOR DE APROBADOR DE IMPRESORA MÁXIMO DE \_ \_ ERRORES \_ \_ DE \_ WIA | Se interrumpió un trabajo de examen porque un elemento Imprinter/Endorser alcanzó el valor máximo válido para WIA IPS PRINTER ENDORSER COUNTER y se restablecieron \_ \_ a \_ \_ 0. Esta característica está disponible con Windows 8 versiones posteriores de Windows. | 0x80210021 |
| FUENTE MÚLTIPLE \_ DE ERRORES \_ DE WIA \_                         | Se produjo un error de examen debido a una condición de fuente de varias páginas. Esta característica está disponible con Windows 8 versiones posteriores de Windows.                                                                                            | 0x80210020 |
| ERROR DE WIA \_ SIN \_ CONEXIÓN                             | El dispositivo está sin conexión. Asegúrese de que el dispositivo está encendido y conectado al equipo.                                                                                                                                                  | 0x80210005 |
| DOCUMENTO DE ERROR DE WIA \_ \_ \_ VACÍO                        | No hay ningún documento en el feeder de documentos.                                                                                                                                                                                      | 0x80210003 |
| WIA \_ ERROR \_ PAPER \_ JAM                          | El papel se afila en el feeder de documentos del analizador.                                                                                                                                                                                   | 0x80210002 |
| PROBLEMA DE PAPEL \_ DE ERROR \_ DE WIA \_                      | Se produjo un problema no especificado con el feeder de documentos del analizador.                                                                                                                                                                 | 0x80210004 |
| ERROR DE \_ WIA \_ WARMING \_ UP                         | El dispositivo se está entrenando.                                                                                                                                                                                                           | 0x80210007 |
| ERROR DE WIA \_ \_ INTERVENCIÓN DEL \_ USUARIO                  | Hay un problema con el dispositivo WIA. Asegúrese de que el dispositivo está encendido, en línea y de que los cables están conectados correctamente.                                                                                                      | 0x80210008 |
| WIA \_ S NO HAY DISPOSITIVO \_ \_ \_ DISPONIBLE                   | No se encontró ningún dispositivo de escáner. Asegúrese de que el dispositivo está en línea, conectado al equipo y que tiene instalado el controlador correcto en el equipo.                                                                                                   | 0x80210015 |



 

 

 



