---
description: En este artículo se explica cómo registrar y distribuir controladores de propiedades para trabajar con el Windows de propiedades.
ms.assetid: E6E81E04-9CC1-4df5-9A87-DE0CBD177356
title: Registro y distribución de controladores de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6a21ba1ae45848fd319d68bfee0624cf5686d3324cc4a3dff039dc94691cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867407"
---
# <a name="registering-and-distributing-property-handlers"></a>Registro y distribución de controladores de propiedades

En este tema se explica cómo crear y registrar controladores de propiedades para trabajar con el Windows de propiedades.

Este tema se organiza de la siguiente manera:

-   [Registro y distribución de controladores de propiedades](#registering-and-distributing-property-handlers)
-   [Consideraciones de rendimiento y confiabilidad para los controladores de propiedades](#performance-and-reliability-considerations-for-property-handlers)
    -   [Directrices para el rendimiento y la confiabilidad](#guidelines-for-performance-and-reliability)
-   [Temas relacionados](#related-topics)

## <a name="registering-and-distributing-property-handlers"></a>Registro y distribución de controladores de propiedades

Una vez implementado el controlador de propiedades, se debe registrar y su extensión de nombre de archivo debe estar asociada al controlador. En el ejemplo siguiente, en el que se usa la extensión .recipe se muestran las entradas del Registro necesarias para hacerlo.

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

Los controladores de propiedades para un tipo de archivo determinado se distribuyen normalmente con las aplicaciones que crean o manipulan archivos de ese tipo. Sin embargo, también debe considerar la posibilidad de que los controladores de propiedades estén disponibles independientemente de estas aplicaciones para admitir la indexación del tipo de archivo en escenarios de servidor en los que el indexador usa controladores de propiedades, pero no son necesarias sus aplicaciones que lo acompañan. Si crea un paquete de instalación independiente para el controlador de propiedades, asegúrese de que incluye lo siguiente:

-   Detalles del registro del controlador de propiedades especificados en el tema [Registering and Distributing Property Handlers]().
-   Registro para el tipo de archivo y los archivos de esquema que se deben instalar, para permitir que los clientes accedan a todas las características del controlador de propiedades.

## <a name="performance-and-reliability-considerations-for-property-handlers"></a>Consideraciones de rendimiento y confiabilidad para los controladores de propiedades

Los controladores de propiedades se invocan para cada archivo de un equipo determinado. Normalmente se les llama en las siguientes circunstancias:

-   Durante la indexación del archivo. Esto se hace fuera de proceso, en un proceso aislado con derechos restringidos.
-   Cuando se accede a los archivos en Windows Explorer con el fin de leer y escribir valores de propiedad. Esto se realiza en proceso.

### <a name="guidelines-for-performance-and-reliability"></a>Directrices para el rendimiento y la confiabilidad

En cualquier momento, un usuario podría tener decenas de miles de archivos de cualquier tipo específico (incluido el suyo) en sus equipos y podría acceder a cualquiera o modificar todos estos archivos en cualquier momento. Dado que los controladores de propiedades se invocan con frecuencia para admitir estas operaciones de acceso y modificación, las características de rendimiento y confiabilidad del controlador de propiedades en entornos ocupados y altamente simultáneos son de importancia crítica.

Tenga en cuenta las siguientes directrices mientras desarrolla y prueba el controlador de propiedades.

-   **Enumeración de propiedades**

    Los controladores de propiedades deben tener un tiempo de respuesta muy rápido para enumerar sus propiedades. Se deben evitar los cálculos de uso intensivo de memoria de valores de propiedad, búsquedas de red o la búsqueda de recursos distintos del propio archivo para garantizar tiempos de respuesta rápidos.

-   **Escritura de propiedades en el lugar**

    Si es posible, cuando se trabaja con archivos de tamaño mediano o grande (varios cientos de KB o más), el formato de archivo debe organizarse para que la lectura o escritura de valores de propiedad no requiera leer todo el archivo desde el disco. Incluso si es necesario buscar el archivo, no debe leerse en la memoria en su totalidad porque eso abate el espacio de trabajo del Explorador de Windows o el indexador de Windows Search cuando intentan acceder a estos archivos o indexar estos archivos. Para obtener más información, vea [Inicializar controladores de propiedades](./building-property-handlers-property-handlers.md).

    Una técnica útil para lograr esto es agregar espacio adicional al encabezado del archivo para que la próxima vez que sea necesario escribir un valor de propiedad, el valor se pueda escribir en su lugar sin necesidad de volver a escribir todo el archivo. Esto requiere la funcionalidad ManualSafeSave. Este enfoque implica un riesgo adicional de que la operación de escritura de archivos se pueda interrumpir mientras la escritura está en curso (debido a un bloqueo del sistema o a una pérdida de energía), pero dado que los tamaños de propiedad suelen ser pequeños, la probabilidad de dicha interrupción es similarmente pequeña y las mejoras de rendimiento que se pueden realizar a través de la escritura de propiedades en el lugar se consideran lo suficientemente importantes como para justificar este riesgo adicional. Aun así, debe tener cuidado de probar la implementación exhaustivamente para asegurarse de que los archivos no estén dañados en caso de que surja un error en el transcurso de una operación de escritura.

    Por último, al implementar la escritura de propiedades en el lugar con ManualSafeSave, a veces la operación no se puede realizar en su lugar y toda la secuencia se debe reescribir de todos modos. Para facilitar la reescritura, la secuencia proporcionada durante la inicialización del controlador admite la [**interfaz IDestinationStreamFactory.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory) La **interfaz IDestinationStreamFactory permite** que las implementaciones de controlador obtengan una secuencia temporal para escribir; Cuando se completan todas las escrituras y se llama al método [**IDestinationStreamFactory::GetDestinationStream,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream) esta secuencia se usa para reemplazar completamente la secuencia de archivos original. Cuando se usa la secuencia de destino, la secuencia de archivo original debe tratarse como de solo lectura, ya que se reemplazará por la secuencia de destino después de llamar al método **IDestinationStreamFactory::GetDestinationStream.**

-   **Elección del modelo de subprocesamiento COM**

    Para maximizar la eficacia del controlador de propiedades, debe especificar que usa el modelo de subprocesos COM `Both` . Esto permite el acceso directo desde los departamentos STA (explorador de Windows, por ejemplo) y los departamentos del agente de transferencia de mensajes (MTA) (el proceso SearchProtocolHost en Windows Search, por ejemplo), evitando la sobrecarga de serialización en esos entornos. Para lograr toda la ventaja del modelo de subprocesos, los servicios de los que depende el controlador también se deben designar como para evitar cualquier serialización en las llamadas a `Both` `Both` esos componentes. Compruebe la documentación de estos servicios concretos para comprobar si usan este modelo de subprocesamiento.

-   **Simultaneidad del controlador de propiedades**

    Los controladores de propiedades y la [**interfaz IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) están diseñados para el acceso en serie en lugar de simultáneo. Windows Explorer, el Windows Search y todas las demás invocaciones de controlador de propiedades del Windows código base garantizan este uso. No debe haber ninguna razón para que terceros usen un controlador de propiedades simultáneamente, pero no se puede garantizar este comportamiento. Además, aunque se espera que el patrón de llamada sea en serie, las llamadas pueden producirse en subprocesos diferentes (por ejemplo, cuando se llama al objeto de forma remota a través de RPC COM, como sucede en el indexador). Por lo tanto, las implementaciones del controlador de propiedades deben admitir la llamada a en subprocesos diferentes y lo ideal es que no sufran ningún efecto negativo cuando se llama simultáneamente. Dado que el patrón de llamada previsto es serie, una implementación trivial que use una sección crítica debe ser suficiente para cumplir estos requisitos en la mayoría de los casos. Es aceptable evitar el bloqueo en llamadas simultáneas mediante la función [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) para detectar y producir errores en las llamadas simultáneas.

-   **Simultaneidad de archivos**

    Los controladores de propiedades se suelen usar en escenarios en los que varias aplicaciones acceden a un archivo simultáneamente. Por lo tanto, el controlador y las aplicaciones deben administrar la simultaneidad especificando los modos de uso compartido adecuados al abrir el archivo. También deben tener en cuenta el acceso que especifican las otras aplicaciones y administrar los casos en los que no se permite el acceso. Es mejor que todos los consumidores especifiquen modos de uso compartido para permitir que otros usuarios accedan al archivo simultáneamente, pero al hacerlo, es necesario administrar los problemas de coherencia. Es necesario tomar decisiones sobre los modos de uso compartido más adecuados en el contexto de la comunidad de aplicaciones que acceden al archivo.

    Los sistemas de archivos permiten a las aplicaciones abrir archivos de forma que les dé control sobre si otras aplicaciones pueden abrir el archivo y cómo. Los modos de uso compartido permiten el acceso de lectura, escritura y eliminación. El sistema de propiedades admite un subconjunto de estos modos de uso compartido, que se describen en la tabla siguiente.

    

    | Modo de acceso                     | Modo de uso compartido                             |
    |---------------------------------|------------------------------------------|
    | Escritura                           | Denegar a otros lectores y escritores           |
    | Escritura (EnableShareDenyWrite)    | Habilitar otros lectores, denegar otros escritores |
    | Solo lectura (valor predeterminado)             | Habilitar otros lectores, denegar otros escritores |
    | Solo lectura (EnableShareDenyNone) | Habilitar otros lectores y escritores         |

    

     

    Los controladores de propiedades abiertos **para escritura** (GPS \_ READWRITE) denegarán a otros lectores y escritores. Los controladores pueden optar por un comportamiento que permita a los lectores especificar la `EnableShareDenyWrite` marca (lo que implica habilitar Lectura) en su registro.

    Los controladores de propiedades se abren **para lectura** (GPS DEFAULT), de forma predeterminada \_ habilitan otros lectores, pero deniegan a otros escritores. Los controladores pueden optar por habilitar otros escritores especificando la `EnableShareDenyNone` marca en su registro. Esto significa que un controlador puede controlar correctamente una situación en la que cambia el contenido de un archivo mientras el controlador lee el archivo.

    Para las definiciones de marca, [**vea GETPROPERTYSTOREFLAGS.**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de los controladores de propiedades](./building-property-handlers-properties.md)
</dt> <dt>

[Usar nombres de tipo](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Usar listas de propiedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicialización de controladores de propiedades](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Procedimientos recomendados y preguntas más frecuentes sobre el controlador de propiedades](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
