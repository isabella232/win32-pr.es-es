---
title: Errores comunes (ADSI)
description: Todos los errores específicos de ADSI tienen una forma hexadecimal de 80005xxx. Los códigos de error más comunes encontrados se describen en la tabla siguiente.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efcbbbce67d9928c9ecda3840f34a1cbf6faae79ca4d9fe72830a5b57881177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692199"
---
# <a name="common-errors-adsi"></a>Errores comunes (ADSI)

Todos los errores específicos de ADSI tienen una forma hexadecimal de 80005xxx. Los códigos de error más comunes encontrados se describen en la tabla siguiente.



| Código de error hexadecimal adsi | Descripción                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 80005000<br/> | Se pasó un nombre de ruta de acceso ADSI no válido. Este error se produce al pasar un ADsPath con un formato deficiente a **GetObject** al enlazar a un objeto .<br/> |
| 8000500D<br/> | La propiedad ADSI no se encuentra en la caché de propiedades.<br/>                                                                                 |
| 8000500E<br/> | El objeto ADSI existe. Si intenta crear un objeto ADSI con el mismo nombre que un objeto ADSI existente, se producirá este error.<br/>    |



 

Para obtener una lista completa de los códigos de error ADSI, vea [Generic ADSI Error Codes](generic-adsi-error-codes.md).

## <a name="com-errors"></a>Errores COM

Puesto que ADSI se compone de objetos COM, devolverá códigos de error COM estándar. En la tabla siguiente se enumeran los códigos de error COM más comunes en la programación ADSI.



| Código de error hexadecimal COM  | Descripción                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| 80004005<br/> | Error no especificado. ADSI no determina la causa del error del objeto COM. <br/>                                  |
| 800041E4<br/> | Objeto no encontrado. Este error se produce principalmente debido a un error ortográfico de la cadena ADsPath al enlazar a un objeto .<br/> |



 

Consulte [Códigos de error COM genéricos](generic-com-error-codes.md) para ver algunos ejemplos más de errores COM que pueden producirse en la programación ADSI.

## <a name="win32-errors"></a>Errores de Win32

Cualquier código de error con formato hexadecimal 8007xxxx es un código de error estándar de Win32. Si convierte los cuatro últimos dígitos de hexadecimal a decimal, puede acceder al error desde la línea de comandos Windows 2000:

**net helpmsg <number>**

En la línea de comandos anterior, " number " es el número decimal obtenido al convertir los cuatro últimos dígitos &lt; del código de error a partir de &gt; hexadecimal. Esta línea de comandos proporcionará una descripción más útil del error de Win32, que puede ser de gran ayuda para depurar el script.

 

 





