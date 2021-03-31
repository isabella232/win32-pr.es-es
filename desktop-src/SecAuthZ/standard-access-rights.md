---
description: Cada tipo de objeto protegible tiene un conjunto de derechos de acceso que corresponden a las operaciones específicas de ese tipo de objeto.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Derechos de acceso estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28fb1ac86a60df373a9f747510b4df624a17eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908167"
---
# <a name="standard-access-rights"></a>Derechos de acceso estándar

Cada tipo de objeto protegible tiene un conjunto de derechos de acceso que corresponden a las operaciones específicas de ese tipo de objeto. Además de estos derechos de acceso específicos del objeto, existe un conjunto de derechos de acceso estándar que se corresponden con operaciones comunes a la mayoría de los tipos de objetos protegibles.

El [formato de máscara de acceso](access-mask-format.md) incluye un conjunto de bits para los derechos de acceso estándar. Las siguientes constantes de Windows para los derechos de acceso estándar se definen en Winnt. h.



| Constante      | Significado                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Delete        | Derecho a eliminar el objeto.                                                                                                                                                                                                                                                                                                              |
| CONTROL de lectura \_ | Derecho para leer la información del [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)del objeto, sin incluir la información de la [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL). |
| SYNCHRONIZE   | Derecho a utilizar el objeto para la sincronización. Esto permite a un subproceso esperar hasta que el objeto se encuentra en el estado señalado. Algunos tipos de objetos no admiten este derecho de acceso.                                                                                                                                                                |
| ESCRIBIR \_ DAC    | Derecho a modificar la [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) en el descriptor de seguridad del objeto.                                                                                                                    |
| propietario de escritura \_  | Derecho a cambiar el propietario que figura en el descriptor de seguridad del objeto.                                                                                                                                                                                                                                                                           |



 

Winnt. h también define las siguientes combinaciones de las constantes de derechos de acceso estándar.



| Constante                   | Significado                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| \_ \_ todos los derechos estándar      | Combina la eliminación, el \_ control de lectura, la \_ DAC de escritura, el propietario de escritura \_ y el acceso de sincronización. |
| se \_ ejecutan los derechos estándar \_  | Definido actualmente para igualar el control de lectura \_ .                                         |
| \_lectura de derechos estándar \_     | Definido actualmente para igualar el control de lectura \_ .                                         |
| \_derechos estándar \_ requeridos | Combina la eliminación, el \_ control de lectura, la \_ DAC de escritura y el acceso de propietario de escritura \_ .              |
| \_escritura de derechos estándar \_    | Definido actualmente para igualar el control de lectura \_ .                                         |



 

 

 
