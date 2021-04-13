---
title: SYSMON valores devueltos
description: A continuación se muestra una lista de los valores devueltos del monitor de sistema que se definen en Smonmsg. h.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ce5678c20a1ab8df825a5e3bc5f725d255e459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421129"
---
# <a name="sysmon-return-values"></a>SYSMON valores devueltos

A continuación se muestra una lista de los valores devueltos del monitor de sistema que se definen en Smonmsg. h.



| Valor devuelto                                       | Descripción                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SMON \_ estado \_ DUPL \_ ruta de acceso de contador \_ (0xC0001388)     | La colección de contadores ya contiene el contador especificado.                                                                                                                                                                               |
| Estado de SMON \_ \_ no \_ \_ objeto SYSMON (0xC0001389)      | La configuración no contiene ningún objeto HTML de monitor de sistema completo.                                                                                                                                                                        |
| SMON \_ status \_ Too \_ pocas \_ Samples (0xC000138A)       | El archivo de registro especificado contiene menos de dos muestras de datos.                                                                                                                                                                                 |
| \_Límite de \_ tamaño del archivo de registro de estado de SMON \_ \_ \_ (0xC000138B)  | El archivo de registro especificado supera los límites de tamaño del control de monitor del sistema. Si hay un archivo de registro seleccionado, seleccione actividad actual como origen de datos para descargar el archivo de registro actual y, a continuación, vuelva a seleccionar el archivo de registro especificado. |
| \_Origen de \_ datos del archivo de registro de estado de SMON \_ \_ \_ (0xC000138C) | Para agregar un nuevo archivo de registro al origen de datos, el tipo de origen de datos debe cambiarse a un tipo distinto de sysmonLogFiles.                                                                                                                          |
| SMON \_ status \_ DUPL \_ \_ ruta de acceso del archivo de registro \_ (0xC000138D)   | La colección de archivos de registro ya contiene el archivo de registro especificado.                                                                                                                                                                             |



 

Para obtener una descripción de los valores devueltos adicionales devueltos por el monitor de sistema, vea códigos de [error del sistema](/windows/desktop/Debug/system-error-codes) y códigos de error de la [aplicación auxiliar de datos de rendimiento](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).

 

 