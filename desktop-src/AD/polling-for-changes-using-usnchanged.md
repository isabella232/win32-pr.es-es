---
title: Sondeo de cambios mediante USNChanged
description: Los cambios de Active Directory también se pueden obtener consultando el atributo uSNChanged, lo que evita las limitaciones del control DirSync.
ms.assetid: 83bda359-09e5-4abf-8f60-9c63bccfcdd1
ms.tgt_platform: multiple
keywords:
- Sondeo de cambios con USNChanged AD
- De USNChanged AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e062c84fae575f837f45d78be7c92e5e284c1e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904482"
---
# <a name="polling-for-changes-using-usnchanged"></a>Sondeo de cambios mediante USNChanged

El control DirSync es eficaz y eficaz, pero tiene dos limitaciones importantes:

-   Solo para aplicaciones con privilegios elevados: para usar el control DirSync, una aplicación se debe ejecutar en una cuenta que tenga el privilegio de **\_ nombre del \_ agente \_ de sincronización se** en el controlador de dominio. Hay pocas cuentas con privilegios elevados, por lo que los usuarios normales no pueden ejecutar una aplicación que use el control DirSync.
-   Sin ámbito de subárbol: el control DirSync devuelve todos los cambios que se producen en un contexto de nomenclatura. Una aplicación interesada solo en los cambios que se producen en un pequeño subárbol de un contexto de nomenclatura debe examinar muchos cambios irrelevantes, lo que es ineficaz tanto para la aplicación como para el controlador de dominio.

Los cambios de Active Directory también se pueden obtener consultando el atributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) , lo que evita las limitaciones del control DirSync. Esta alternativa no es mejor que el control DirSync en todos los aspectos porque implica la transmisión de todos los atributos cuando cambia cualquier atributo y requiere más trabajo del desarrollador de la aplicación para administrar correctamente determinados escenarios de error. Actualmente, es la mejor manera de escribir ciertas aplicaciones de seguimiento de cambios.

Cuando un controlador de dominio modifica un objeto, establece el atributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) del objeto en un valor mayor que el valor anterior del atributo **uSNChanged** para ese objeto, y mayor que el valor actual del atributo **uSNChanged** para todos los demás objetos contenidos en ese controlador de dominio. Como consecuencia, una aplicación puede encontrar el objeto modificado más recientemente en un controlador de dominio buscando el objeto con el valor de **uSNChanged** más grande. El segundo objeto modificado más recientemente en un controlador de dominio tendrá el segundo valor de **uSNChanged** más grande, y así sucesivamente.

El atributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) no se replica, por lo que al leer el atributo **uSNChanged** de un objeto en dos controladores de dominio diferentes, normalmente se proporcionan valores distintos.

Por ejemplo, el atributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) se puede usar para realizar el seguimiento de los cambios en un subárbol S. En primer lugar, realice una sincronización completa de los subárboles S. Supongamos que el valor de **uSNChanged** más grande para cualquier objeto en S es U. consulte periódicamente todos los objetos de subárbol s cuyo valor de **uSNChanged** sea mayor que U. La consulta devolverá todos los objetos que han cambiado desde la sincronización completa. Establézcalo en el valor de **uSNChanged** más grande entre estos objetos modificados y esté listo para volver a sondear.

Los matices de la implementación de una aplicación de sincronización de [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) incluyen:

-   Use el atributo **highestCommittedUSN,** de RootDSE para enlazar los filtros de [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) . Es decir, antes de iniciar una sincronización completa, lea el **highestCommittedUSN,** del controlador de dominio asociado. A continuación, realice una consulta de sincronización completa (con los resultados paginados) para inicializar la base de datos. Cuando haya finalizado, almacene el valor **highestCommittedUSN,** leído antes de la consulta de sincronización completa. para utilizar como límite inferior del atributo **uSNChanged** para la siguiente sincronización. Más adelante, para realizar una sincronización incremental, relea el atributo RootDSE de **highestCommittedUSN,** . A continuación, consulte los objetos pertinentes, con los resultados paginados, cuyo **uSNChanged** es mayor que los límites inferiores del valor del atributo **uSNChanged** guardado de la sincronización anterior. Actualice la base de datos con esta información. Cuando termine, actualice los límites inferiores del atributo **uSNChanged** desde el valor **highestCommittedUSN,** leído antes de la consulta de sincronización incremental. Almacene siempre los límites inferiores del valor del atributo **uSNChanged** en el mismo almacenamiento que la aplicación está sincronizando con el contenido del controlador de dominio.

    Al seguir este procedimiento, en lugar de basarse en valores de [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) en objetos recuperados, se evita que el servidor Revise los objetos actualizados que se encuentran fuera del conjunto que es aplicable a la aplicación.

-   Dado que [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) es un atributo no replicado, la aplicación debe enlazarse al mismo controlador de dominio cada vez que se ejecuta. Si no se puede enlazar a ese controlador de dominio, debe esperar hasta que pueda hacerlo, o afiliar con algún nuevo controlador de dominio y realizar una sincronización completa con ese controlador de dominio. Cuando la aplicación se afilia con un controlador de dominio, registra el nombre DNS de ese controlador de dominio en un almacenamiento estable, que es el mismo almacenamiento que mantiene coherente con el contenido del controlador de dominio. A continuación, usa el nombre DNS almacenado para enlazar al mismo controlador de dominio para las sincronizaciones posteriores.
-   La aplicación debe detectar cuándo se ha restaurado la copia de seguridad del controlador de dominio al que está afiliada actualmente, ya que esto puede provocar incoherencias. Cuando la aplicación se asocia con un controlador de dominio, almacena en caché el "ID. de invocación" de ese controlador de dominio en almacenamiento estable, es decir, el mismo almacenamiento que mantiene coherente con el contenido del controlador de dominio. El "identificador de invocación" de un controlador de dominio es un GUID almacenado en **el atributo de invocación del** objeto de servicio del controlador de dominio. Para obtener el nombre distintivo del objeto de servicio de un controlador de dominio, lea el atributo **dsServiceName** de RootDSE.

    Tenga en cuenta que cuando el almacenamiento estable de la aplicación se restaura desde una copia de seguridad, no hay ningún problema de coherencia porque el nombre del controlador de dominio, el ID. de invocación y los límites inferiores del valor del atributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) se almacenan con los datos sincronizados con el contenido del controlador de dominio.

-   Use la paginación al consultar el servidor, tanto las sincronizaciones completas como incrementales, para evitar la posibilidad de recuperar grandes conjuntos de resultados simultáneamente. Para obtener más información, vea [especificar otras opciones de búsqueda](specifying-other-search-options.md).
-   Realice consultas basadas en índices para evitar obligar al servidor a almacenar resultados intermedios grandes al usar resultados paginados. Para obtener más información, vea [atributos indexados](indexed-attributes.md).
-   En general, no use la ordenación del lado servidor de los resultados de la búsqueda, lo que puede obligar al servidor a almacenar y ordenar resultados intermedios grandes. Esto se aplica a las sincronizaciones completas e incrementales. Para obtener más información, vea [especificar otras opciones de búsqueda](specifying-other-search-options.md).
-   No controlar correctamente las condiciones de los elementos primarios. La aplicación puede reconocer un objeto antes de que haya reconocido su elemento primario. En función de la aplicación, esto puede ser o no un problema. La aplicación siempre puede leer el estado actual del elemento primario desde el directorio.
-   Para controlar los objetos que se han descargado o eliminado, almacene el atributo [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) de cada objeto sometido a seguimiento. El atributo **objectGUID** de un objeto permanece sin modificar, independientemente de dónde se mueva en todo el bosque.
-   Para controlar los objetos que se han descargado, realice sincronizaciones completas periódicas o aumente el ámbito de búsqueda y filtre los cambios que no interesen en el cliente.
-   Para controlar los objetos eliminados, realice sincronizaciones completas periódicas o realice una búsqueda independiente de los objetos eliminados cuando realice una sincronización incremental. Al consultar los objetos eliminados, recupere el [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) de los objetos eliminados para determinar los objetos que se van a eliminar de la base de datos. Para obtener más información, vea [recuperar objetos eliminados](retrieving-deleted-objects.md).
-   Tenga en cuenta que los resultados de la búsqueda incluyen solo los objetos y atributos que el autor de la llamada tiene permiso para leer (en función de los descriptores de seguridad y las DACL en los distintos objetos). Para obtener más información, vea [efectos de la seguridad en las consultas](effects-of-security-on-queries.md).

Para obtener más información y un ejemplo de código que muestra los conceptos básicos de una aplicación de sincronización de USNChanged, vea el [código de ejemplo para recuperar los cambios mediante USNChanged](example-code-to-retrieve-changes-using-usnchanged.md).

 

 