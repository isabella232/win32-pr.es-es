---
description: En este tema se identifican las marcas de opciones que puede utilizar para controlar el procesamiento del subproceso de acción personalizada.
ms.assetid: a09b3a0e-564e-41aa-af0d-2e46776f291b
title: Opciones de procesamiento de devolución de acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f8664ff489280993a7fc52117f3d19bccb023b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913498"
---
# <a name="custom-action-return-processing-options"></a>Opciones de procesamiento de devolución de acción personalizada

En este tema se identifican las marcas de opciones que puede utilizar para controlar el procesamiento del subproceso de acción personalizada. Las marcas se usan para especificar que los subprocesos de acción principales y personalizados se ejecuten sincrónicamente (Windows Installer espera a que el subproceso de acción personalizada se complete antes de reanudar el subproceso de instalación principal) o de forma asincrónica (Windows Installer ejecuta la acción personalizada simultáneamente mientras continúa la instalación principal).

Para habilitar las marcas de opción, agregue el valor que se identifica en la tabla siguiente al valor del campo Type de la [tabla CustomAction](customaction-table.md).



| Constante                                                           | Hexadecimal             | Decimal | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|-------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (ninguno)                                                             | 0x00000000              | +0      | Ejecución sincrónica que produce un error si el código de salida no es 0 (cero). <br/> Si no se establece la marca msidbCustomActionTypeContinue, la acción personalizada debe devolver uno de los valores devueltos que se describe en [valores devueltos de acción personalizada](custom-action-return-values.md).<br/>                                                                                                                                                                                                                             |
| **msidbCustomActionTypeContinue**                                  | 0x00000040              | + 64     | Ejecución sincrónica que omite el código de salida y continúa.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **msidbCustomActionTypeAsync**                                     | 0x00000080              | + 128    | Ejecución asincrónica que espera el código de salida al final de la secuencia.<br/> Esta opción no se puede usar con [instalaciones simultáneas](concurrent-installations.md), [revertir acciones personalizadas](rollback-custom-actions.md)o [acciones personalizadas de script](scripts.md).<br/>                                                                                                                                                                                                                                |
| **msidbCustomActionTypeAsync**  +  **msidbCustomActionTypeContinue** | 0x00000040 + 0x00000080 | +192    | Ejecución asincrónica que no espera a que finalice.<br/> La ejecución continúa una vez finalizada la Windows Installer.<br/> Esta opción solo se puede usar con las acciones personalizadas de tipo EXE que son [archivos ejecutables](executable-files.md). <br/> El resto de tipos de acciones personalizadas solo puede ser asincrónico dentro de la sesión de instalación y debe finalizar para que finalice la instalación.<br/> Esta opción no se puede usar con [instalaciones simultáneas](concurrent-installations.md).<br/> |



 

 

 




