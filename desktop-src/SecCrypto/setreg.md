---
description: La herramienta SetReg establece el valor de las claves del Registro que controlan el comportamiento del proceso de comprobación del certificado Authenticode.
ms.assetid: 6c456a59-ee6c-420d-b075-7de8bd2fd8ff
title: SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05da29d3eddf7e04ba5bd735e1032f388d9d204a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160743"
---
# <a name="setreg"></a>SetReg

La herramienta SetReg establece el valor de las claves del Registro que controlan el comportamiento del proceso de comprobación del certificado Authenticode. Estas claves se denominan claves de estado de publicación de software. Después de completar la acción solicitada, la herramienta muestra el estado actual de las claves de estado de publicación de software.

**SetReg** \[ *Opciones* \] \[ *Opción \#* {**TRUE** \| **FALSE**}\]

La herramienta Establecer registro solo se incluye con las versiones 1.0 y 1.1 del SDK de .NET Framework, que puede descargar desde el Centro [de descarga de Microsoft.](https://www.microsoft.com/download/details.aspx?id=16217)

## <a name="options"></a>Opciones

Las opciones pueden ser uno de los siguientes valores. Las opciones de la tabla siguiente solo se pueden usar con Internet Explorer 4.0 o posterior.



| Opción | Descripción                                                                                                                                            |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-q** | Suprime la presentación de los valores de Clave de estado de publicación de software después de que SetReg haya completado la acción solicitada. Los valores se muestran de forma predeterminada. |
| **-?** | Enumerar la sintaxis y las opciones de los comandos.                                                                                                                       |



 

## <a name="choice-"></a>Elección \#

*Elección \#* debe ser uno de los siguientes valores.



| Opción | Descripción                                                                                                                       | Resultado                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------|-----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1**  | Confiar en la raíz de prueba                                                                                                               | Este valor se omite. **Windows XP/2000:** Si **es TRUE,** confía en una raíz de prueba. Esto equivale a ejecutar "regedit wvtvtvt.reg" en Internet Explorer 3. *x*.<br/> El valor predeterminado es **FALSE.** Cualquier archivo firmado con una raíz de prueba no se comprobará a menos que esta marca esté establecida en **TRUE.** Tenga en cuenta que este comportamiento ha cambiado con Windows XP con Service Pack 1 (SP1) porque Windows XP con SP1 omite este valor.<br/> <br/> |
| **2**  | Uso de la fecha de expiración en los certificados                                                                                               | Si **es TRUE,** comprueba la fecha de expiración del certificado. Para omitir las fechas de expiración, establezca esta marca en **FALSE.** El valor predeterminado es **TRUE.**                                                                                                                                                                                                                                                                                                       |
| **3**  | Comprobación de la [ *lista de revocación*](../secgloss/c-gly.md) | Si **es TRUE,** realiza la comprobación de revocación. Para omitir la comprobación de revocación, establezca esta marca en **FALSE.** El valor predeterminado es **TRUE.** **Internet Explorer 3. *x*: el** valor predeterminado es **FALSE.**<br/>                                                                                                                                                                                                                                               |
| **4**  | Servidor de revocación sin conexión correcto (individual)<br/>                                                                              | Si **es TRUE,** permite la aprobación sin conexión para certificados individuales. El valor predeterminado es **FALSE.**                                                                                                                                                                                                                                                                                                                                                 |
| **5**  | Servidor de revocación sin conexión correcto (comercial)<br/>                                                                              | Si **es TRUE,** permite la aprobación sin conexión para los certificados comerciales. El valor predeterminado es **TRUE.**                                                                                                                                                                                                                                                                                                                                                  |
| **6**  | Java offline Revocation server OK (Individual) (Correcto del servidor de revocación sin conexión de Java [individual])<br/>                                                                         | Si **es TRUE,** permite la aprobación sin conexión para certificados individuales y no muestra la interfaz de usuario para los certificados no válidos. El valor predeterminado es **FALSE.**                                                                                                                                                                                                                                                                                    |
| **7**  | Java offline Revocation server OK (Commercial) (Correcto del servidor de revocación sin conexión de Java [comercial])<br/>                                                                         | Si **es TRUE,** permite la aprobación sin conexión para los certificados comerciales y no muestra la interfaz de usuario para los certificados no válidos. El valor predeterminado es **TRUE.**                                                                                                                                                                                                                                                                                     |
| **8**  | Hacer que los objetos firmados de la versión 1 ya no son válidos                                                                                     | Si **es TRUE,** hace que los objetos firmados de la versión 1 ya no son válidos. El valor predeterminado es **FALSE.**                                                                                                                                                                                                                                                                                                                                                      |
| **9**  | Comprobación de la lista de revocación del servidor de marca de tiempo                                                                                | Si **es TRUE,** realiza la comprobación de revocación en el certificado del servidor de marca de tiempo. El valor predeterminado es **FALSE.** **Internet Explorer 3. *x*:** este valor no se admite.<br/>                                                                                                                                                                                                                                                            |
| **10** | Solo los elementos de confianza encontrados en la base de datos de confianza                                                                                      | Si **es TRUE,** permite descargas de publicadores contenidos en la base de datos de confianza personal. El valor predeterminado es **FALSE.** **Internet Explorer 3. *x*:** este valor no se admite.<br/>                                                                                                                                                                                                                                             |



 

 

 
