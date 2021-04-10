---
description: La parte más problemática de la escritura de componentes consiste en tratar con posibles errores.
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: Control de errores en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1979fc49ff8f14bb83b194be7e1787feaf7d86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153584"
---
# <a name="handling-errors-in-com"></a>Control de errores en COM+

La parte más problemática de la escritura de componentes consiste en tratar con posibles errores. Intentar determinar lo que puede ir mal y lo que debe hacer sobre él puede ser complicado en las mejores condiciones. Los errores comunes que el componente puede buscar y controlar son las conexiones de red con errores, los errores de seguridad y los errores asociados a los objetos inalcanzables.

Además, puede desarrollar sus propios códigos de error para informar sobre errores específicos de la interfaz, como cuando se ha infringido una regla de negocios.

En consonancia con el modelo de programación COM+, un objeto puede (y con frecuencia) llamar a métodos de interfaz en otros objetos para realizar el trabajo. Dado que los programadores pueden escribir componentes en diferentes lenguajes de programación, COM+ requiere que todos los mecanismos de control de errores sean independientes del idioma, por ejemplo: HRESULTs y colecciones [**errorInfo**](errorinfo.md) .

En esta sección se incluyen temas, que se describen en la tabla siguiente, en los que se explican técnicas para controlar errores en aplicaciones COM+, características de COM+ que afectan al comportamiento de errores y sugerencias para diagnosticar errores de COM+.



| Tema                                                                                           | Descripción                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Estrategias para controlar errores en COM+](strategies-for-handling-errors-in-com-.md)<br/> | Enumera y describe las directrices básicas para controlar los errores en COM+, incluido Cuándo usar valores HRESULT y colecciones de [**errorInfo**](errorinfo.md) .<br/> |
| [Cómo modifica COM+ los valores devueltos](how-com--modifies-return-values.md)<br/>               | Identifica la única condición en la que COM+ convierte un valor HRESULT estándar en un código de error de COM+ antes de devolverlo al autor de la llamada.<br/>             |
| [Aislamiento de errores y Directiva FailFast](fault-isolation-and-failfast-policy.md)<br/>       | Muestra cómo el aislamiento de errores y la Directiva FailFast afectan al comportamiento de COM+.<br/>                                                                          |
| [Buscar el origen de un error](finding-the-source-of-an-error.md)<br/>                 | Describe cómo diagnosticar el origen y obtener una descripción de los errores de la aplicación. <br/>                                                       |
| [Interpretar códigos de error](interpreting-error-codes.md)<br/>                             | Identifica el mecanismo de control de errores predominante para Microsoft Visual C++, el lenguaje Java y Visual Basic de Microsoft. <br/>                    |
| [Solución de problemas](troubleshooting.md)<br/>                                               | Proporciona ayuda adicional para diagnosticar errores.<br/>                                                                                             |
| [Ponerse en contacto con soporte técnico](contacting-support.md)<br/>                                         | Identifica información importante sobre la solución de problemas que debe proporcionar al ponerse en contacto con el servicio de soporte técnico.<br/>                                                     |



 

Para obtener información detallada sobre el control de errores asociados a varios servicios COM+, vea las siguientes secciones:

-   [Acelerar las transacciones mediante la notificación del objeto raíz](speeding-transactions-by-notifying-the-root-object.md)
-   [Control de errores](handling-errors-in-queued-components.md) (para componentes en cola)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depurar aplicaciones COM+](debugging-com--applications.md)
</dt> </dl>

 

 




