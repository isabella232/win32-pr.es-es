---
description: La herramienta SetReg establece el valor de las claves del registro que controlan el comportamiento del proceso de comprobación de certificados Authenticode.
ms.assetid: 6c456a59-ee6c-420d-b075-7de8bd2fd8ff
title: SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05da29d3eddf7e04ba5bd735e1032f388d9d204a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808324"
---
# <a name="setreg"></a>SetReg

La herramienta SetReg establece el valor de las claves del registro que controlan el comportamiento del proceso de comprobación de certificados Authenticode. Estas claves se denominan claves de estado de publicación de software. Después de completar la acción solicitada, la herramienta muestra el estado actual de las claves de estado de publicación de software.

**SetReg** \[ *Opciones* \] de \[ *Choice \#* {**true** \| **false**}\]

La herramienta establecer registro solo se incluye con la versión 1,0 y 1,1 del SDK de .NET Framework, que puede descargar desde el [centro de descarga de Microsoft](https://www.microsoft.com/download/details.aspx?id=16217).

## <a name="options"></a>Opciones

Las opciones pueden ser de uno de los valores siguientes. Las opciones que se indican en la tabla siguiente solo se pueden usar con Internet Explorer 4,0 o posterior.



| Opción | Descripción                                                                                                                                            |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-q** | Suprima la presentación de los valores de clave de estado de publicación de software después de que SetReg haya completado la acción solicitada. Los valores se muestran de forma predeterminada. |
| **-?** | Enumerar las opciones y la sintaxis de los comandos.                                                                                                                       |



 

## <a name="choice-"></a>Alternativa \#

*Elección \#* debe ser uno de los valores siguientes.



| Opción | Descripción                                                                                                                       | Resultado                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------|-----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1**  | Confiar en la raíz de prueba                                                                                                               | Este valor se omite. **Windows XP/2000:** Si **es true**, confía en una raíz de prueba. Esto equivale a ejecutar "regedit wvtston. reg" en Internet Explorer 3. *x*.<br/> El valor predeterminado es **false**. Los archivos firmados con una raíz de prueba no comprobarán a menos que esta marca esté establecida en **true**. Tenga en cuenta que este comportamiento ha cambiado con Windows XP con Service Pack 1 (SP1) porque Windows XP con SP1 omite este valor.<br/> <br/> |
| **2**  | Usar fecha de expiración en certificados                                                                                               | Si **es true**, comprueba la fecha de expiración del certificado. Para omitir las fechas de expiración, establezca esta marca en **false**. El valor predeterminado es **true**.                                                                                                                                                                                                                                                                                                       |
| **3**  | Comprobar la [ *lista de revocación*](../secgloss/c-gly.md) | Si **es true**, realiza la comprobación de revocación. Para omitir la comprobación de revocación, establezca esta marca en **false**. El valor predeterminado es **true**. **Internet Explorer 3. *x*:** el valor predeterminado es **false**.<br/>                                                                                                                                                                                                                                               |
| **4**  | Servidor de revocación sin conexión correcto (individual)<br/>                                                                              | Si **es true**, permite la aprobación sin conexión para certificados individuales. El valor predeterminado es **false**.                                                                                                                                                                                                                                                                                                                                                 |
| **5**  | Servidor de revocación sin conexión correcto (comercial)<br/>                                                                              | Si **es true**, permite la aprobación sin conexión para los certificados comerciales. El valor predeterminado es **true**.                                                                                                                                                                                                                                                                                                                                                  |
| **6**  | Servidor de revocación sin conexión de Java correcto (individual)<br/>                                                                         | Si **es true**, permite la aprobación sin conexión para certificados individuales y no muestra la interfaz de usuario para los certificados incorrectos. El valor predeterminado es **false**.                                                                                                                                                                                                                                                                                    |
| **7**  | Servidor de revocación sin conexión de Java correcto (comercial)<br/>                                                                         | Si **es true**, permite la aprobación sin conexión para los certificados comerciales y no muestra la interfaz de usuario para los certificados incorrectos. El valor predeterminado es **true**.                                                                                                                                                                                                                                                                                     |
| **8**  | Hacer que los objetos firmados de la versión 1 dejen de ser válidos                                                                                     | Si **es true**, hace que los objetos firmados de la versión 1 dejen de ser válidos. El valor predeterminado es **false**.                                                                                                                                                                                                                                                                                                                                                      |
| **9**  | Comprobar la lista de revocación del servidor de marca de tiempo                                                                                | Si **es true**, realiza la comprobación de revocación en el certificado del servidor de marca de tiempo. El valor predeterminado es **false**. **Internet Explorer 3. *x*:** este valor no se admite.<br/>                                                                                                                                                                                                                                                            |
| **10** | Solo los elementos de confianza encontrados en la base de datos de confianza                                                                                      | Si **es true**, permite descargas de publicadores contenidos en la base de datos de confianza personal. El valor predeterminado es **false**. **Internet Explorer 3. *x*:** este valor no se admite.<br/>                                                                                                                                                                                                                                             |



 

 

 
