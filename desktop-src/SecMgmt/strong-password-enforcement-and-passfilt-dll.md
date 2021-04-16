---
description: Enumera los requisitos exigidos por las herramientas de administración del sistema de contraseñas seguras.
ms.assetid: a84f83b2-181b-4f65-82bd-bc7f0689aad3
title: Aplicación segura de contraseñas y Passfilt.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b7be524511d52048e06ae83ab110384c3bf5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540966"
---
# <a name="strong-password-enforcement-and-passfiltdll"></a>Aplicación segura de contraseñas y Passfilt.dll

La aplicación segura de contraseñas se puede habilitar con las herramientas de administración del sistema. Si la Directiva de administración del sistema está habilitada, las contraseñas deben cumplir los siguientes requisitos mínimos cuando se crean o se cambian:

-   Las contraseñas no pueden contener el valor samAccountName (Nombre de cuenta) del usuario o el valor displayName completo (valor Nombre completo). Ambas comprobaciones no distinguen mayúsculas de minúsculas.
-   SamAccountName se comprueba en su totalidad únicamente para determinar si forma parte de la contraseña. Si samAccountName tiene menos de tres caracteres, se omitirá esta comprobación.
-   La propiedad displayName se analiza para delimitadores: comas, puntos, guiones, caracteres de subrayado, espacios, signo de número y tabulaciones. Si se encuentran alguno de estos delimitadores, se divide displayName y se confirma que no se incluirán en la contraseña todas las secciones analizadas (tokens). Se ignoran los tokens de menos de tres caracteres y no se comprueban subcadenas de los tokens. Por ejemplo, el nombre "Beatriz M. Melgar" se divide en tres símbolos: "Beatriz", "M" y "Melgar". Dado que el segundo símbolo solo tiene un carácter, este se omite. Por lo tanto, este usuario no podría tener una contraseña que incluya "beatriz" o "melgar" como subcadena en cualquier parte de la contraseña.
-   Las contraseñas deben contener caracteres de tres de las cinco categorías siguientes.



| Categorías de caracteres                                                                                                                                                      | Ejemplos                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Mayúsculas de los idiomas europeos (de A a la Z con marcas diacríticas, griego y caracteres cirílicos)<br/>                                                     | A, B, C, Z<br/>                |
| Minúsculas de los idiomas europeos (de a a la a, s nítidass, marcas diacríticas, griego y caracteres cirílico)<br/>                                            | a, b, c, z<br/>                |
| Dígitos en base 10 (del 0 al 9)<br/>                                                                                                                                   | 0, 1, 2, 9<br/>                |
| Caracteres no alfanuméricos (caracteres especiales)<br/>                                                                                                               | $,!,%, ^, () {} \[ \] ;: <>?<br/> |
| Cualquier carácter Unicode que se clasifica como carácter alfabético, pero que no está en mayúsculas o minúsculas. Esto incluye caracteres Unicode de idiomas de Asia.<br/> |                                        |



 

**Para habilitar la aplicación segura de contraseñas**

1.  En la consola de administración de, busque **Directiva de seguridad local**.
2.  Seleccione **Directiva de cuenta** y, a continuación, seleccione **Directiva de contraseñas**.
3.  Habilite la configuración las **contraseñas deben cumplir los requisitos de complejidad** .

> [!Note]  
> Un carácter determinado solo puede satisfacer una categoría. La función [GetStringTypeW](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypew) se usa para comprobar si cada uno de los caracteres de la contraseña está en mayúsculas, minúsculas o alfanuméricos.

 

 

