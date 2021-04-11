---
description: En este tema se explica cómo crear y registrar controladores de propiedades para trabajar con el sistema de propiedades de Windows.
ms.assetid: E6E81E04-9CC1-4df5-9A87-DE0CBD177356
title: Registrar y distribuir controladores de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1de6af17df8e15912870626935995c67c25f518
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276203"
---
# <a name="registering-and-distributing-property-handlers"></a>Registrar y distribuir controladores de propiedades

En este tema se explica cómo crear y registrar controladores de propiedades para trabajar con el sistema de propiedades de Windows.

Este tema se organiza de la siguiente manera:

-   [Registrar y distribuir controladores de propiedades](#registering-and-distributing-property-handlers)
-   [Consideraciones de rendimiento y confiabilidad para los controladores de propiedades](#performance-and-reliability-considerations-for-property-handlers)
    -   [Directrices para el rendimiento y la confiabilidad](#guidelines-for-performance-and-reliability)
-   [Temas relacionados](#related-topics)

## <a name="registering-and-distributing-property-handlers"></a>Registrar y distribuir controladores de propiedades

Una vez implementado el controlador de propiedades, se debe registrar y su extensión de nombre de archivo debe estar asociada al controlador. En el ejemplo siguiente, con la extensión. Recipe se muestran las entradas del registro necesarias para hacerlo.

```
HKEY_CLASSES_ROOT
   CLSID
      {50d9450f-2a80-4f08-93b9-2eb526477d1a}
         (Default) = Recipe Property Handler
         ManualSafeSave [REG_DWORD] = 00000001
         InProcServer32
            (Default) = C:\\SDK\\PropertyHandlerSample\\bin\\RecipeHandlers.dll
            ThreadingModel = Apartment
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     .recipe
                        (Default) = {50d9450f-2a80-4f08-93b9-2eb526477d1a}
```

Los controladores de propiedades de un tipo de archivo determinado se distribuyen normalmente con las aplicaciones que crean o manipulan archivos de ese tipo. Sin embargo, también debe considerar la posibilidad de hacer que los controladores de propiedades estén disponibles independientemente de estas aplicaciones para admitir la indización del tipo de archivo en escenarios de servidor en los que el indizador usa los controladores de propiedades, pero no se requieren las aplicaciones que lo acompañan. Si crea un paquete de instalación independiente para el controlador de propiedades, asegúrese de que incluye lo siguiente:

-   Los detalles de registro del controlador de propiedades especificados en el tema [registrar y distribuir controladores de propiedades]().
-   Registro para el tipo de archivo y los archivos de esquema que se deben instalar, para permitir que los clientes tengan acceso a todas las características del controlador de propiedades.

## <a name="performance-and-reliability-considerations-for-property-handlers"></a>Consideraciones de rendimiento y confiabilidad para los controladores de propiedades

Los controladores de propiedades se invocan para cada archivo en un equipo determinado. Normalmente se les llama en las siguientes circunstancias:

-   Durante la indización del archivo. Esto se hace fuera de proceso, en un proceso aislado con derechos restringidos.
-   Cuando se tiene acceso a los archivos en el explorador de Windows con el fin de leer y escribir valores de propiedad. Esto se hace en proceso.

### <a name="guidelines-for-performance-and-reliability"></a>Directrices para el rendimiento y la confiabilidad

En cualquier momento, un usuario podría tener decenas de miles de archivos de cualquier tipo específico (incluido el suyo) en sus equipos, y podría tener acceso a todos estos archivos o modificarlos en cualquier momento. Dado que los controladores de propiedades se invocan con frecuencia para admitir estas operaciones de acceso y modificación, las características de rendimiento y confiabilidad del controlador de propiedades en entornos que están ocupados y muy simultáneos son de importancia crítica.

Tenga en cuenta las siguientes directrices al desarrollar y probar el controlador de propiedad.

-   **Enumeración de propiedades**

    Los controladores de propiedades deben tener un tiempo de respuesta muy rápido en la enumeración de sus propiedades. Los cálculos que consumen mucha memoria de los valores de propiedad, las búsquedas en la red o la búsqueda de recursos distintos del propio archivo deben evitarse para garantizar tiempos de respuesta rápidos.

-   **Escritura de propiedades en contexto**

    Si es posible, cuando se trabaja con archivos de tamaño medio o grande (varios cientos de KB o más), el formato de archivo se debe organizar de modo que la lectura o escritura de valores de propiedad no requiera leer todo el archivo del disco. Incluso si es necesario buscar el archivo, no se debe leer en memoria en su totalidad, ya que aumenta el espacio de trabajo del explorador de Windows o del indizador de Windows Search cuando intentan obtener acceso a estos archivos o indizarlos. Para obtener más información, vea [inicializar controladores de propiedades](./building-property-handlers-property-handlers.md).

    Una técnica útil para lograrlo es rellenar el encabezado del archivo con espacio adicional para que la próxima vez que se deba escribir un valor de propiedad, el valor se pueda escribir en su lugar sin necesidad de volver a escribir todo el archivo. Esto requiere la funcionalidad ManualSafeSave. Este enfoque implica un riesgo adicional de que la operación de escritura de archivo se interrumpa mientras la escritura está en curso (debido a un bloqueo del sistema o a una pérdida de energía), pero como los tamaños de las propiedades son generalmente pequeños, la probabilidad de una interrupción de este tipo es igualmente pequeña y las ganancias de rendimiento que se pueden realizar mediante la escritura de propiedades en contexto se consideran lo suficientemente significativas Aun así, debe tener cuidado de probar la implementación exhaustivamente para asegurarse de que los archivos no estén dañados en caso de que se produzca un error en el transcurso de una operación de escritura.

    Por último, al implementar la escritura de propiedades en contexto con ManualSafeSave, a veces la operación no se puede realizar en contexto y se debe volver a escribir toda la secuencia. Para facilitar la reescritura, la secuencia proporcionada durante la inicialización del controlador es compatible con la interfaz [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory) . La interfaz **IDestinationStreamFactory** permite a las implementaciones del controlador obtener un flujo temporal para escribir en él. Cuando se completan todas las operaciones de escritura y se llama al método [**IDestinationStreamFactory:: GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream) , esta secuencia se usa para reemplazar completamente el flujo de archivos original. Cuando se usa el flujo de destino, el flujo de archivos original debe tratarse como de solo lectura, ya que será reemplazado por el flujo de destino después de que se haya llamado al método **IDestinationStreamFactory:: GetDestinationStream** .

-   **Elección del modelo de subprocesos COM**

    Para maximizar la eficacia del controlador de propiedades, debe especificar que use el modelo de subprocesos COM `Both` . Esto permite el acceso directo desde apartamentos de STA (explorador de Windows, por ejemplo) y apartamentos del agente de transferencia de mensajes (MTA) (el proceso SearchProtocolHost en Windows Search, por ejemplo), evitando la sobrecarga de serialización en esos entornos. Para lograr todas las ventajas del `Both` modelo de subprocesos, los servicios de los que depende el controlador también se deben designar como `Both` para evitar la serialización en las llamadas a esos componentes. Consulte la documentación de estos servicios concretos para comprobar si usan este modelo de subprocesos.

-   **Simultaneidad del controlador de propiedades**

    Los controladores de propiedades y la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) están diseñados para el acceso en serie en lugar de los simultáneos. El explorador de Windows, el indizador de Windows Search y todas las demás invocaciones del controlador de propiedades de la base de código de Windows garantizan este uso. No debe haber ningún motivo para que terceras personas utilicen un controlador de propiedades simultáneamente, pero no se puede garantizar este comportamiento. Además, aunque se espera que el patrón de llamada sea en serie, las llamadas pueden presentarse en diferentes subprocesos (por ejemplo, cuando se llama al objeto de forma remota a través de COM RPC, como ocurre en el indizador). Por lo tanto, las implementaciones del controlador de propiedades deben admitir que se llamen en diferentes subprocesos y, idealmente, no deberían sufrir efectos indebidos cuando se llama a la vez. Dado que el patrón de llamada previsto es en serie, una implementación trivial que usa una sección crítica debe ser suficiente para cumplir estos requisitos en la mayoría de los casos. Es aceptable evitar el bloqueo de llamadas simultáneas mediante la función [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) para detectar y producir errores en las llamadas simultáneas.

-   **Simultaneidad de archivos**

    Los controladores de propiedades se usan a menudo en escenarios donde varias aplicaciones tienen acceso a un archivo simultáneamente. Por lo tanto, el controlador y las aplicaciones necesitan administrar la simultaneidad mediante la especificación de los modos de uso compartido adecuados al abrir el archivo. También deben tener en cuenta el acceso que las demás aplicaciones especifican y administrar los casos en los que no se permite el acceso. Es mejor si todos los consumidores especifican modos de uso compartido liberales para permitir que otros usuarios tengan acceso al archivo al mismo tiempo, pero al hacerlo, es necesario administrar los problemas de coherencia. Las decisiones sobre los modos de uso compartido más adecuados que se deben usar deben realizarse en el contexto de la comunidad de aplicaciones que tienen acceso al archivo.

    Los sistemas de archivos permiten a las aplicaciones abrir archivos de una forma que les permita controlar si otras aplicaciones pueden abrir el archivo y cómo hacerlo. Los modos de uso compartido habilitan el acceso de lectura, escritura y eliminación. El sistema de propiedades admite un subconjunto de estos modos de uso compartido, que se describen en la tabla siguiente.

    

    | Modo de acceso                     | Modo de uso compartido                             |
    |---------------------------------|------------------------------------------|
    | Escritura                           | Denegar a otros lectores y escritores           |
    | Escritura (EnableShareDenyWrite)    | Habilitar otros lectores, denegar otros escritores |
    | Solo lectura (valor predeterminado)             | Habilitar otros lectores, denegar otros escritores |
    | Solo lectura (EnableShareDenyNone) | Habilitar otros lectores y escritores         |

    

     

    Los controladores de propiedad abiertos para escritura (el **valor** de GPS \_ ReadWrite) denegarán a otros lectores y escritores. Los controladores pueden optar por el comportamiento que permite a los lectores especificar la `EnableShareDenyWrite` marca (que implica habilitar lectura) en su registro.

    Los controladores de propiedades abiertos para **lectura** ( \_ valor predeterminado de GPS), habilitan de forma predeterminada a otros lectores pero deniegan a otros escritores. Los controladores pueden optar por habilitar otros escritores especificando la `EnableShareDenyNone` marca en su registro. Esto significa que un controlador puede controlar correctamente una situación en la que el contenido de un archivo cambia mientras el controlador lee el archivo.

    Para ver las definiciones de marca, vea [**GETPROPERTYSTOREFLAGS**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de los controladores de propiedades](./building-property-handlers-properties.md)
</dt> <dt>

[Usar nombres de tipo](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Usar listas de propiedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicializar controladores de propiedades](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Prácticas recomendadas y preguntas más frecuentes sobre controladores de propiedades](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
