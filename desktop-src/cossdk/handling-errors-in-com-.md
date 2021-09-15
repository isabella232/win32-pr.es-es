---
description: La parte más problemática de la escritura de componentes es tratar con posibles errores.
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: Control de errores en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1979fc49ff8f14bb83b194be7e1787feaf7d86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568472"
---
# <a name="handling-errors-in-com"></a>Control de errores en COM+

La parte más problemática de la escritura de componentes es tratar con posibles errores. Intentar determinar qué puede salir mal y qué hacer al respecto puede ser complicado en las mejores condiciones. Los errores comunes que el componente podría comprobar y controlar son conexiones de red con errores, errores de seguridad y errores asociados a objetos inaccesibles.

Además, puede desarrollar sus propios códigos de error para notificar errores específicos de la interfaz, como cuando se ha infringido una regla de negocios.

De acuerdo con el modelo de programación com+, un objeto puede (y a menudo lo hace) llamar a métodos de interfaz en otros objetos para realizar el trabajo. Dado que los programadores pueden escribir componentes en distintos lenguajes de programación, COM+ requiere que todos los mecanismos de control de errores sean neutrales en el lenguaje, por ejemplo: colecciones HRESULT y [**ErrorInfo.**](errorinfo.md)

En esta sección se incluyen temas, que se describen en la tabla siguiente, en los que se describen técnicas para controlar errores en aplicaciones COM+, características de COM+ que afectan al comportamiento de errores y sugerencias para diagnosticar errores com+.



| Tema                                                                                           | Descripción                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Estrategias para controlar errores en COM+](strategies-for-handling-errors-in-com-.md)<br/> | Enumera y describe las directrices básicas para controlar errores en COM+, incluido cuándo usar colecciones HRESULT [**y ErrorInfo.**](errorinfo.md)<br/> |
| [Cómo com+ modifica los valores devueltos](how-com--modifies-return-values.md)<br/>               | Identifica la condición única en la que COM+ convierte un HRESULT estándar en un código de error COM+ antes de devolverlo al autor de la llamada.<br/>             |
| [Aislamiento de errores y directiva de error](fault-isolation-and-failfast-policy.md)<br/>       | Muestra cómo el aislamiento de errores y la directiva de conmutación por error afectan al comportamiento de COM+.<br/>                                                                          |
| [Buscar el origen de un error](finding-the-source-of-an-error.md)<br/>                 | Describe cómo diagnosticar el origen y obtener una descripción de los errores de la aplicación. <br/>                                                       |
| [Interpretación de códigos de error](interpreting-error-codes.md)<br/>                             | Identifica el mecanismo predominante de control de errores para Microsoft Visual C++, el lenguaje Java y Microsoft Visual Basic. <br/>                    |
| [Solución de problemas](troubleshooting.md)<br/>                                               | Proporciona ayuda adicional para diagnosticar errores.<br/>                                                                                             |
| [Ponerse en contacto con el soporte técnico](contacting-support.md)<br/>                                         | Identifica información importante para resolver problemas que debe proporcionar al ponerse en contacto con el soporte técnico.<br/>                                                     |



 

Para obtener información detallada sobre cómo controlar los errores asociados a varios servicios COM+, consulte las secciones siguientes:

-   [Acelerar transacciones notificando al objeto raíz](speeding-transactions-by-notifying-the-root-object.md)
-   [Control de errores](handling-errors-in-queued-components.md) (para componentes en cola)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depuración de aplicaciones COM+](debugging-com--applications.md)
</dt> </dl>

 

 




