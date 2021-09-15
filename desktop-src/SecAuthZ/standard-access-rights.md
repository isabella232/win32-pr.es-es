---
description: Cada tipo de objeto protegible tiene un conjunto de derechos de acceso que corresponden a operaciones específicas de ese tipo de objeto.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Derechos de acceso estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28fb1ac86a60df373a9f747510b4df624a17eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473469"
---
# <a name="standard-access-rights"></a>Derechos de acceso estándar

Cada tipo de objeto protegible tiene un conjunto de derechos de acceso que corresponden a operaciones específicas de ese tipo de objeto. Además de estos derechos de acceso específicos del objeto, hay un conjunto de derechos de acceso estándar que corresponden a las operaciones comunes a la mayoría de los tipos de objetos protegibles.

El [formato de máscara de](access-mask-format.md) acceso incluye un conjunto de bits para los derechos de acceso estándar. Las siguientes Windows constantes de acceso estándar se definen en Winnt.h.



| Constante      | Significado                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DELETE        | Derecho a eliminar el objeto.                                                                                                                                                                                                                                                                                                              |
| CONTROL DE \_ LECTURA | Derecho a leer la información en el descriptor de seguridad del [*objeto*](/windows/desktop/SecGloss/s-gly), sin incluir la información en la lista de [*control*](/windows/desktop/SecGloss/s-gly) de acceso del sistema (SACL). |
| SYNCHRONIZE   | Derecho a utilizar el objeto para la sincronización. Esto permite que un subproceso espere hasta que el objeto esté en el estado señalado. Algunos tipos de objeto no admiten este derecho de acceso.                                                                                                                                                                |
| ESCRIBIR \_ DAC    | Derecho a modificar la lista [*de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) en el descriptor de seguridad del objeto.                                                                                                                    |
| PROPIETARIO DE \_ ESCRITURA  | Derecho a cambiar el propietario que figura en el descriptor de seguridad del objeto.                                                                                                                                                                                                                                                                           |



 

Winnt.h también define las siguientes combinaciones de las constantes de derechos de acceso estándar.



| Constante                   | Significado                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| DERECHOS \_ ESTÁNDAR \_ TODOS      | Combina el acceso DELETE, READ \_ CONTROL, WRITE \_ DAC, WRITE \_ OWNER y SYNCHRONIZE. |
| STANDARD \_ RIGHTS \_ EXECUTE  | Actualmente se define para que sea igual a \_ READ CONTROL.                                         |
| DERECHOS \_ ESTÁNDAR \_ LEÍDOS     | Actualmente se define para que sea igual a \_ READ CONTROL.                                         |
| DERECHOS \_ ESTÁNDAR \_ REQUERIDOS | Combina el acceso DELETE, READ \_ CONTROL, WRITE \_ DAC y WRITE \_ OWNER.              |
| ESCRITURA \_ DE DERECHOS \_ ESTÁNDAR    | Actualmente se define para que sea igual a \_ READ CONTROL.                                         |



 

 

 
