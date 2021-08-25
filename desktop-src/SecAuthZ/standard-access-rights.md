---
description: Cada tipo de objeto protegible tiene un conjunto de derechos de acceso que corresponden a operaciones específicas de ese tipo de objeto.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Derechos de acceso estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56067a4ed31f9506aee0b326e82a9bd5b4b49b02d12e6d401cc04f8262b19da0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907115"
---
# <a name="standard-access-rights"></a>Derechos de acceso estándar

Cada tipo de objeto protegible tiene un conjunto de derechos de acceso que corresponden a operaciones específicas de ese tipo de objeto. Además de estos derechos de acceso específicos del objeto, hay un conjunto de derechos de acceso estándar que corresponden a operaciones comunes a la mayoría de los tipos de objetos protegibles.

El [formato de máscara de](access-mask-format.md) acceso incluye un conjunto de bits para los derechos de acceso estándar. Las siguientes Windows constantes de acceso estándar se definen en Winnt.h.



| Constante      | Significado                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Delete        | Derecho a eliminar el objeto.                                                                                                                                                                                                                                                                                                              |
| CONTROL DE \_ LECTURA | Derecho a leer la información en el descriptor de seguridad del [*objeto*](/windows/desktop/SecGloss/s-gly), sin incluir la información en la lista de [*control*](/windows/desktop/SecGloss/s-gly) de acceso del sistema (SACL). |
| SYNCHRONIZE   | Derecho a utilizar el objeto para la sincronización. Esto permite que un subproceso espere hasta que el objeto esté en estado señalado. Algunos tipos de objeto no admiten este derecho de acceso.                                                                                                                                                                |
| ESCRIBIR \_ DAC    | Derecho a modificar la lista [*de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) en el descriptor de seguridad del objeto.                                                                                                                    |
| PROPIETARIO DE \_ ESCRITURA  | Derecho a cambiar el propietario que figura en el descriptor de seguridad del objeto.                                                                                                                                                                                                                                                                           |



 

Winnt.h también define las siguientes combinaciones de constantes de derechos de acceso estándar.



| Constante                   | Significado                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| TODOS \_ LOS DERECHOS \_ ESTÁNDAR      | Combina el acceso DELETE, READ \_ CONTROL, WRITE \_ DAC, WRITE \_ OWNER y SYNCHRONIZE. |
| EJECUCIÓN \_ DE DERECHOS \_ ESTÁNDAR  | Actualmente se define para que sea igual a \_ READ CONTROL.                                         |
| LECTURA \_ DE DERECHOS \_ ESTÁNDAR     | Actualmente se define para que sea igual a \_ READ CONTROL.                                         |
| DERECHOS \_ ESTÁNDAR \_ REQUERIDOS | Combina los accesos DELETE, READ \_ CONTROL, WRITE \_ DAC y WRITE \_ OWNER.              |
| ESCRITURA \_ DE DERECHOS \_ ESTÁNDAR    | Actualmente se define para que sea igual a \_ READ CONTROL.                                         |



 

 

 
