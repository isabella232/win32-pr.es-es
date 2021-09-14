---
description: En esta sección se describe la sintaxis y el uso del control de excepciones estructurado tal como se implementa en el compilador de optimización de Microsoft C/C++. El compilador interpreta las palabras clave siguientes como parte del mecanismo estructurado de control de excepciones.
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: Sintaxis del controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c50b8d12a74312c8b0a843ea300d23e278e88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164634"
---
# <a name="handler-syntax"></a>Sintaxis del controlador

En esta sección se describe la sintaxis y el uso del control de excepciones estructurado tal como se implementa en el compilador de optimización de Microsoft C/C++. El compilador interpreta las palabras clave siguientes como parte del mecanismo estructurado de control de excepciones.



| Palabra clave         | Descripción                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_\_Tratar**     | Comienza un cuerpo de código guardado. Se usa con la **\_ \_ palabra clave except** para construir un controlador de [excepciones](exception-handler-syntax.md)o con la palabra clave **\_ \_ finally** para construir un [controlador de terminación](termination-handler-syntax.md). |
| **\_\_Excepto**  | Comienza un bloque de código que se ejecuta solo cuando se produce una excepción dentro de su bloque **\_ \_ try** asociado.                                                                                                                                   |
| **\_\_finally** | Comienza un bloque de código que se ejecuta cada vez que el flujo de control deja su bloque **\_ \_ try** asociado.                                                                                                                                    |
| **\_\_Salir**   | Permite la terminación inmediata del bloque **\_ \_ try** sin provocar una terminación anómala y su penalización de rendimiento.                                                                                                                      |



 

El compilador también interpreta las funciones [**GetExceptionCode,**](getexceptioncode.md) [**GetExceptionInformation**](getexceptioninformation.md)y [**AbnormalTermination**](abnormaltermination.md) como palabras clave, y su uso fuera de la sintaxis adecuada de control de excepciones genera un error del compilador. A continuación se descripciones breves de estas funciones.



| Función                                                   | Descripción                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExceptionCode**](getexceptioncode.md)               | Devuelve un código que identifica el tipo de excepción. Solo se puede llamar a esta función desde la expresión de filtro o el bloque de controlador de excepciones.                                                                                                |
| [**GetExceptionInformation**](getexceptioninformation.md) | Devuelve un puntero a una [**estructura EXCEPTION \_ POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) que contiene punteros al registro de contexto y al registro de excepción. Solo se puede llamar a esta función desde la expresión de filtro de un controlador de excepciones. |
| [**AbnormalTermination**](abnormaltermination.md)         | Indica si el flujo de control dejó el bloque **\_ \_ try** asociado secuencialmente después de ejecutar la última instrucción en el bloque . Solo se puede llamar a esta función desde el bloque **\_ \_ finally** de un controlador de terminación.              |



 

 

 



