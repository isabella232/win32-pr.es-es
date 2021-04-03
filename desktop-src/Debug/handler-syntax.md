---
description: En esta sección se describe la sintaxis y el uso del control de excepciones estructurado tal y como se implementa en el compilador de optimización de C/C++ de Microsoft. El compilador interpreta las siguientes palabras clave como parte del mecanismo de control de excepciones estructurado.
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: Sintaxis del controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c50b8d12a74312c8b0a843ea300d23e278e88
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907006"
---
# <a name="handler-syntax"></a>Sintaxis del controlador

En esta sección se describe la sintaxis y el uso del control de excepciones estructurado tal y como se implementa en el compilador de optimización de C/C++ de Microsoft. El compilador interpreta las siguientes palabras clave como parte del mecanismo de control de excepciones estructurado.



| Palabra clave         | Descripción                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_\_try**     | Comienza un cuerpo protegido del código. Se usa con la palabra clave **\_ \_ Except** para construir un [controlador de excepciones](exception-handler-syntax.md)o con la palabra clave **\_ \_ Finally** para construir un [controlador de finalización](termination-handler-syntax.md). |
| **\_\_CEPT**  | Comienza un bloque de código que se ejecuta solo cuando se produce una excepción dentro de su bloque **\_ \_ try** asociado.                                                                                                                                   |
| **\_\_finally** | Comienza un bloque de código que se ejecuta cada vez que el flujo de control abandona su bloque **\_ \_ try** asociado.                                                                                                                                    |
| **\_\_omiti**   | Permite la terminación inmediata del bloque **\_ \_ try** sin causar una terminación anómala y su penalización en el rendimiento.                                                                                                                      |



 

El compilador también interpreta las funciones [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md)y [**AbnormalTermination**](abnormaltermination.md) como palabras clave, y su uso fuera de la sintaxis de control de excepciones adecuada genera un error del compilador. A continuación se muestran breves descripciones de estas funciones.



| Función                                                   | Descripción                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExceptionCode**](getexceptioncode.md)               | Devuelve un código que identifica el tipo de excepción. Solo se puede llamar a esta función desde dentro de la expresión de filtro o el bloque de controlador de excepciones.                                                                                                |
| [**GetExceptionInformation**](getexceptioninformation.md) | Devuelve un puntero a una estructura de [**\_ punteros de excepción**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) que contiene punteros al registro de contexto y al registro de excepción. Solo se puede llamar a esta función desde dentro de la expresión de filtro de un controlador de excepciones. |
| [**AbnormalTermination**](abnormaltermination.md)         | Indica si el flujo de control dejó el bloque **\_ \_ try** asociado secuencialmente después de ejecutar la última instrucción del bloque. Solo se puede llamar a esta función desde dentro del bloque **\_ \_ Finally** de un controlador de finalización.              |



 

 

 



