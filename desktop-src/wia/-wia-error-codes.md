---
description: 'Las funciones y los métodos de adquisición de imágenes de Windows (WIA) pueden devolver códigos de error de la lista siguiente: error CodeMeaningCodeWIA \_ error \_ BUSYThe el dispositivo está ocupado.'
ms.assetid: 3abbe92b-32b7-4820-b208-45c847243078
title: Códigos de error (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6025616d46a5973692bb3cafbcf88e18836ad0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908198"
---
# <a name="error-codes-wia"></a>Códigos de error (WIA)

Las funciones y los métodos de adquisición de imágenes de Windows (WIA) pueden devolver códigos de error de la lista siguiente: 

| Código de error                                      | Significado                                                                                                                                                                                                                             | Código       |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| ERROR de WIA \_ \_ ocupado                                | El dispositivo está ocupado. Cierre todas las aplicaciones que usen este dispositivo o espere a que finalice y vuelva a intentarlo.                                                                                                                          | 0x80210006 |
| ERROR de detección de WIA \_ \_ \_ abierto                         | Una o varias de las cubiertas del dispositivo están abiertas.                                                                                                                                                                                          | 0x80210016 |
| ERROR de WIA en la \_ \_ comunicación del dispositivo \_               | Error en la comunicación con el dispositivo WIA. Asegúrese de que el dispositivo esté encendido y conectado al equipo. Si el problema persiste, desconecte y vuelva a conectar el dispositivo.                                                            | 0x8021000A |
| \_dispositivo de error WIA \_ \_ bloqueado                      | El dispositivo está bloqueado. Cierre todas las aplicaciones que usen este dispositivo o espere a que finalice y vuelva a intentarlo.                                                                                                                        | 0x8021000D |
| \_ \_ excepción de error \_ de WIA en el \_ controlador               | El controlador de dispositivo produjo una excepción.                                                                                                                                                                                               | 0x8021000E |
| error de WIA error \_ \_ General \_                      | Se ha producido un error desconocido con el dispositivo WIA.                                                                                                                                                                                  | 0x80210001 |
| ERROR de WIA de \_ \_ \_ configuración de hardware incorrecta \_        | Hay una configuración incorrecta en el dispositivo WIA.                                                                                                                                                                                    | 0x8021000C |
| ERROR de WIA \_ \_ comando no válido \_                    | El dispositivo no admite este comando.                                                                                                                                                                                            | 0x8021000B |
| ERROR de WIA \_ : \_ respuesta de controlador no válida \_ \_           | La respuesta del controlador no es válida.                                                                                                                                                                                            | 0x8021000F |
| elemento de error de WIA \_ \_ \_ eliminado                       | Se eliminó el dispositivo WIA. Ya no está disponible.                                                                                                                                                                               | 0x80210009 |
| luz de error de WIA \_ \_ \_ desactivada                           | La lámpara del escáner está desactivada.                                                                                                                                                                                                          | 0x80210017 |
| ERROR de WIA \_ : \_ \_ \_ contador de aprobador de impresora máximo \_ | Se interrumpió un trabajo de digitalización debido a que un elemento de endosador o endosador alcanzó el valor máximo válido para el \_ contador de aprobador de impresoras IPS de WIA \_ \_ \_ y se restableció en 0. Esta característica está disponible con Windows 8 y versiones posteriores de Windows. | 0x80210021 |
| \_ \_ fuente múltiple de errores de WIA \_                         | Se produjo un error de examen debido a una condición de fuente de varias páginas. Esta característica está disponible con Windows 8 y versiones posteriores de Windows.                                                                                            | 0x80210020 |
| ERROR de WIA \_ \_ sin conexión                             | El dispositivo está sin conexión. Asegúrese de que el dispositivo esté encendido y conectado al equipo.                                                                                                                                                  | 0x80210005 |
| \_documento de error WIA \_ \_ vacío                        | No hay ningún documento en el alimentador de documentos.                                                                                                                                                                                      | 0x80210003 |
| \_atasco de \_ papel de error WIA \_                          | El papel está atascado en el alimentador de documentos del escáner.                                                                                                                                                                                   | 0x80210002 |
| problema con el papel de error de WIA \_ \_ \_                      | Se produjo un problema no especificado con el alimentador de documentos del escáner.                                                                                                                                                                 | 0x80210004 |
| \_error de WIA al \_ preparar \_                         | El dispositivo se está preparando.                                                                                                                                                                                                           | 0x80210007 |
| \_intervención del \_ usuario con errores de WIA \_                  | Hay un problema con el dispositivo WIA. Asegúrese de que el dispositivo está encendido, en línea y de que los cables están conectados correctamente.                                                                                                      | 0x80210008 |
| WIA \_ S \_ no hay ningún \_ dispositivo \_ disponible                   | No se encontró ningún dispositivo de escáner. Asegúrese de que el dispositivo está en línea, conectado al equipo y que tiene instalado el controlador correcto en el equipo.                                                                                                   | 0x80210015 |



 

 

 



