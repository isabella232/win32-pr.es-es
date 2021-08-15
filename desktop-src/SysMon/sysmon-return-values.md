---
title: Valores devueltos de SYSMON
description: A continuación se muestra una lista de los valores devueltos del Monitor de sistema que se definen en Smonmsg.h.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ce526a64132cef51338a83b387aa8e9bfd58ce0ef0b99a1fb7db0dce4c15ef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956451"
---
# <a name="sysmon-return-values"></a>Valores devueltos de SYSMON

A continuación se muestra una lista de los valores devueltos del Monitor de sistema que se definen en Smonmsg.h.



| Valor devuelto                                       | Descripción                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RUTA DE ACCESO DEL CONTADOR DUPL DE ESTADO DE SMON \_ \_ \_ \_ (0xC0001388)     | La colección de contadores ya contiene el contador especificado.                                                                                                                                                                               |
| SMON \_ STATUS \_ NO \_ SYSMON OBJECT \_ (0XC0001389)      | La configuración no contiene ningún objeto HTML completo del Monitor de sistema.                                                                                                                                                                        |
| ESTADO DE SMON \_ \_ MUY POCOS EJEMPLOS \_ \_ (0xC000138A)       | El archivo de registro especificado contiene menos de dos ejemplos de datos.                                                                                                                                                                                 |
| LÍMITE DE TAMAÑO DEL ARCHIVO DE REGISTRO DE ESTADO DE SMON \_ \_ \_ \_ \_ (0xC000138B)  | El archivo de registro especificado supera los límites de tamaño del control Monitor de sistema. Si un archivo de registro está seleccionado actualmente, seleccione la actividad actual como origen de datos para descargar el archivo de registro actual y, a continuación, vuelva a seleccionar el archivo de registro especificado. |
| ORIGEN DE DATOS DEL ARCHIVO DE REGISTRO DE ESTADO DE SMON \_ \_ \_ \_ \_ (0xC000138C) | Para agregar un nuevo archivo de registro al origen de datos, el tipo de origen de datos debe cambiarse a un tipo distinto de sysmonLogFiles.                                                                                                                          |
| RUTA DE ACCESO DEL ARCHIVO DE REGISTRO DUPL DE ESTADO DE SMON \_ \_ \_ \_ \_ (0xC000138D)   | La colección de archivos de registro ya contiene el archivo de registro especificado.                                                                                                                                                                             |



 

Para obtener una descripción de los valores devueltos adicionales devueltos por el Monitor de sistema, vea Códigos de [error](/windows/desktop/Debug/system-error-codes) del sistema y Códigos de error del asistente [de datos de rendimiento](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).

 

 