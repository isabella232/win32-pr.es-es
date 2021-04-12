---
title: Errores comunes (ADSI)
description: Todos los errores específicos de ADSI tienen una forma hexadecimal de 80005xxx. Los códigos de error más comunes que se encuentran se describen en la tabla siguiente.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd870871d7a8e2939cda546178e2f31fe92644d
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2019
ms.locfileid: "104358600"
---
# <a name="common-errors-adsi"></a>Errores comunes (ADSI)

Todos los errores específicos de ADSI tienen una forma hexadecimal de 80005xxx. Los códigos de error más comunes que se encuentran se describen en la tabla siguiente.



| Código de error hexadecimal ADSI | Descripción                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 80005000<br/> | Se pasó un nombreruta de ADSI no válido. Este error se produce al pasar un ADsPath con un formato incorrecto a **GetObject** al enlazar a un objeto.<br/> |
| 8000500D<br/> | No se encuentra la propiedad ADSI en la caché de propiedades.<br/>                                                                                 |
| 8000500E<br/> | El objeto ADSI existe. Si intenta crear un objeto ADSI con el mismo nombre que un objeto ADSI existente, se producirá este error.<br/>    |



 

Para obtener una lista completa de los códigos de error ADSI, consulte [códigos de error ADSI genéricos](generic-adsi-error-codes.md).

## <a name="com-errors"></a>Errores COM

Como ADSI se compone de objetos COM, devolverá códigos de error COM estándar. En la tabla siguiente se enumeran los códigos de error COM que se encuentran normalmente en la programación ADSI.



| Código de error hexadecimal COM  | Descripción                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| 80004005<br/> | Error no especificado. La causa del error del objeto COM es indeterminada en ADSI. <br/>                                  |
| 800041E4<br/> | Objeto no encontrado. Este error se produce principalmente debido a la escritura incorrecta de la cadena ADsPath al enlazar con un objeto.<br/> |



 

Consulte [códigos de error com genéricos](generic-com-error-codes.md) para ver algunos ejemplos de errores com que pueden producirse en la programación ADSI.

## <a name="win32-errors"></a>Errores de Win32

Cualquier código de error del formato hexadecimal 8007xxxx es un código de error estándar de Win32. Si convierte los cuatro últimos dígitos de hexadecimal a decimal, puede tener acceso al error desde la línea de comandos de Windows 2000:

**net helpmsg <number>**

En la línea de comandos anterior, " &lt; número &gt; " es el número decimal obtenido al convertir los cuatro últimos dígitos del código de error de hexadecimal. Esta línea de comandos proporcionará una descripción más útil del error de Win32, que puede ser de gran ayuda para depurar el script.

 

 





