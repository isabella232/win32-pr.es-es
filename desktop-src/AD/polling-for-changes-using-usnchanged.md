---
title: Sondeo de cambios mediante USNChanged
description: Los cambios Active Directory también se pueden obtener consultando el atributo uSNChanged, lo que evita las limitaciones del control DirSync.
ms.assetid: 83bda359-09e5-4abf-8f60-9c63bccfcdd1
ms.tgt_platform: multiple
keywords:
- Sondeo de cambios mediante USNChanged AD
- USNChanged AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c665d536eb3dcb0e3265a2e3abb87808ddf630510e5d0600f6185007c72bc28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025533"
---
# <a name="polling-for-changes-using-usnchanged"></a>Sondeo de cambios mediante USNChanged

El control DirSync es eficaz y eficaz, pero tiene dos limitaciones importantes:

-   Solo para aplicaciones con privilegios elevados: para usar el control DirSync, una aplicación debe ejecutarse con una cuenta que tenga el privilegio SE **\_ NOMBRE DEL AGENTE \_ \_ DE** SINCRONIZACIÓN en el controlador de dominio. Pocas cuentas tienen tantos privilegios, por lo que los usuarios normales no pueden ejecutar una aplicación que use el control DirSync.
-   Sin ámbito de subárbol: el control DirSync devuelve todos los cambios que se producen dentro de un contexto de nomenclatura. Una aplicación interesada solo en los cambios que se producen en un subárbol pequeño de un contexto de nomenclatura debe atravesar muchos cambios irrelevantes, lo que es ineficaz tanto para la aplicación como para el controlador de dominio.

Los cambios Active Directory también se pueden obtener consultando el atributo [**uSNChanged,**](/windows/desktop/ADSchema/a-usnchanged) lo que evita las limitaciones del control DirSync. Esta alternativa no es mejor que el control DirSync en todos los aspectos porque implica transmitir todos los atributos cuando cambia cualquier atributo y requiere más trabajo del desarrollador de la aplicación para controlar ciertos escenarios de error correctamente. Actualmente, es la mejor manera de escribir determinadas aplicaciones de seguimiento de cambios.

Cuando un controlador de dominio modifica un objeto, establece el atributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) de ese objeto en un valor mayor que el valor anterior del atributo **uSNChanged** para ese objeto y mayor que el valor actual del atributo **uSNChanged** para todos los demás objetos contenidos en ese controlador de dominio. Como consecuencia, una aplicación puede encontrar el objeto modificado más recientemente en un controlador de dominio mediante la búsqueda del objeto con el valor **uSNChanged más** grande. El segundo objeto cambiado más recientemente en un controlador de dominio tendrá el segundo valor **de uSNChanged** más grande, y así sucesivamente.

El [**atributo uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) no se replica, por lo que la lectura del atributo **uSNChanged** de un objeto en dos controladores de dominio diferentes normalmente dará valores diferentes.

Por ejemplo, el [**atributo uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) se puede usar para realizar un seguimiento de los cambios en un subárbol S. En primer lugar, realice una "sincronización completa" del subárbol S. Supongamos que el valor **de uSNChanged** más grande para cualquier objeto de S es U. Consultar periódicamente todos los objetos del subárbol S cuyo valor **uSNChanged** es mayor que U. La consulta devolverá todos los objetos que han cambiado desde la sincronización completa. Establezca el valor de **uSNChanged más** grande entre estos objetos modificados y esté listo para sondear de nuevo.

Las sutilidades de la implementación de una [**aplicación de sincronización uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) incluyen:

-   Use el **atributo highestCommittedUSN** de rootDSE para enlazar los [**filtros uSNChanged.**](/windows/desktop/ADSchema/a-usnchanged) Es decir, antes de iniciar una sincronización completa, lea **el valor de highestCommittedUSN** del controlador de dominio asociado. A continuación, realice una consulta de sincronización completa (mediante resultados paginados) para inicializar la base de datos. Cuando haya finalizado, almacene el valor **highestCommittedUSN** leído antes de la consulta de sincronización completa. para usar como límites inferiores del **atributo uSNChanged** para la siguiente sincronización. Más adelante, para realizar una sincronización incremental, vuelva a leer el **atributo rootDSE highestCommittedUSN.** A continuación, consulte los objetos pertinentes mediante los resultados paginados, cuyo **uSNChanged** es mayor que los límites inferiores del valor del atributo **uSNChanged** guardado de la sincronización anterior. Actualice la base de datos con esta información. Cuando haya terminado, actualice los límites inferiores del atributo **uSNChanged** desde el valor **highestCommittedUSN** leído antes de la consulta de sincronización incremental. Almacene siempre los límites inferiores del valor del atributo **uSNChanged** en el mismo almacenamiento que la aplicación está sincronizando con el contenido del controlador de dominio.

    Siguiendo este procedimiento, en lugar de basarse en valores [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) en objetos recuperados, evita que el servidor vuelva a examinar los objetos actualizados que se encuentran fuera del conjunto aplicable a la aplicación.

-   Dado [**que uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) es un atributo no replicado, la aplicación debe enlazarse al mismo controlador de dominio cada vez que se ejecuta. Si no puede enlazar a ese controlador de dominio, debe esperar hasta que pueda hacerlo, o estar asociado a algún nuevo controlador de dominio y realizar una sincronización completa con ese controlador de dominio. Cuando las filiales de aplicación con un controlador de dominio registra el nombre DNS de ese controlador de dominio en almacenamiento estable, que es el mismo almacenamiento que mantiene coherente con el contenido del controlador de dominio. A continuación, usa el nombre DNS almacenado para enlazar con el mismo controlador de dominio para las sincronizaciones posteriores.
-   La aplicación debe detectar cuándo se restauró de la copia de seguridad el controlador de dominio al que está actualmente asociado, ya que esto puede provocar incoherencias. Cuando las filiales de aplicación con un controlador de dominio almacena en caché el "identificador de invocación" de ese controlador de dominio en un almacenamiento estable, es decir, el mismo almacenamiento que mantiene coherente con el contenido del controlador de dominio. El "identificador de invocación" de un controlador de dominio es un GUID almacenado en el atributo **invocationID** del objeto de servicio del controlador de dominio. Para obtener el nombre distintivo del objeto de servicio de un controlador de dominio, lea el atributo **dsServiceName** del rootDSE.

    Tenga en cuenta que cuando se restaura el almacenamiento estable de la aplicación desde la copia de seguridad, no hay ningún problema de coherencia porque el nombre del controlador de dominio, el identificador de invocación y los límites inferiores del valor del atributo [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) se almacenan con los datos sincronizados con el contenido del controlador de dominio.

-   Use la paginación al consultar el servidor, tanto las sincronizaciones completa como las incrementales, para evitar la posibilidad de recuperar conjuntos de resultados grandes simultáneamente. Para obtener más información, vea [Especificar otras opciones de búsqueda.](specifying-other-search-options.md)
-   Realice consultas basadas en índices para evitar forzar al servidor a almacenar resultados intermedios grandes al usar resultados paginados. Para obtener más información, vea [Atributos indizados.](indexed-attributes.md)
-   En general, no use la ordenación del lado servidor de los resultados de búsqueda, lo que puede obligar al servidor a almacenar y ordenar resultados intermedios grandes. Esto se aplica a las sincronizaciones completa e incremental. Para obtener más información, vea [Especificar otras opciones de búsqueda.](specifying-other-search-options.md)
-   No controle las condiciones primarias correctamente. La aplicación puede reconocer un objeto antes de que haya reconocido su elemento primario. Dependiendo de la aplicación, esto puede ser o no un problema. La aplicación siempre puede leer el estado actual del elemento primario desde el directorio .
-   Para controlar los objetos movidos o eliminados, almacene el [**atributo objectGUID**](/windows/desktop/ADSchema/a-objectguid) de cada objeto de seguimiento. El atributo **objectGUID de** un objeto permanece sin cambios, independientemente de dónde se mueve a través del bosque.
-   Para controlar los objetos movidos, realice sincronizaciones periódicas o aumente el ámbito de búsqueda y filtre los cambios que no le interesen en el extremo del cliente.
-   Para controlar los objetos eliminados, realice sincronizaciones periódicas y completa o realice una búsqueda independiente de los objetos eliminados al realizar una sincronización incremental. Al consultar los objetos eliminados, recupere el [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) de los objetos eliminados para determinar los objetos que se eliminarán de la base de datos. Para obtener más información, [vea Recuperar objetos eliminados.](retrieving-deleted-objects.md)
-   Tenga en cuenta que los resultados de la búsqueda incluyen solo los objetos y atributos que el autor de la llamada tiene permiso para leer (en función de los descriptores de seguridad y las DACL en los distintos objetos). Para obtener más información, [vea Efectos de la seguridad en las consultas](effects-of-security-on-queries.md).

Para obtener más información y un ejemplo de código que muestra los conceptos básicos de una aplicación de sincronización USNChanged, vea Código de ejemplo para recuperar cambios [mediante USNChanged.](example-code-to-retrieve-changes-using-usnchanged.md)

 

 