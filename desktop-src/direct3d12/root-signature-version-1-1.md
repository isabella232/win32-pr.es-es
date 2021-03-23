---
title: Versión de firma raíz 1,1
description: El propósito de la versión 1,1 de la firma raíz es permitir que las aplicaciones indiquen los controladores cuando los descriptores de un montón de descriptores no cambian o los descriptores de datos que apuntan a no cambian.
ms.assetid: 8FE42C1C-7F1D-4E70-A7EE-D5EC67237327
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d0a107b4186f164e60a6225f55c5ba3f4f06b2
ms.sourcegitcommit: f5a319899176e2df564bdb4d9eaffc32140452a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/14/2020
ms.locfileid: "104549140"
---
# <a name="root-signature-version-11"></a>Versión de firma raíz 1,1

El propósito de la versión 1,1 de la firma raíz es permitir que las aplicaciones indiquen los controladores cuando los descriptores de un montón de descriptores no cambian o los descriptores de datos que apuntan a no cambian. Esto permite que los controladores realicen optimizaciones que podrían ser posibles sabiendo que un descriptor o la memoria a la que apunta es estático durante un período de tiempo.

-   [Información general](#overview)
-   [Marcas estáticas y volátiles](#static-and-volatile-flags)
    -   [descriptores \_ volátiles](#descriptors_volatile)
    -   [DATOS \_ volátiles](#data_volatile)
    -   [DATOS \_ estáticos \_ mientras se \_ establecen \_ en \_ Execute](#data_static_while_set_at_execute)
    -   [DATOS \_ estáticos](#data_static)
    -   [Combinar marcas](#combining-flags)
    -   [Resumen de la marca](#flag-summary)
-   [Resumen de la API de la versión 1,1](#version-11-api-summary)
    -   [Enumeraciones](#enums)
    -   [Estructuras](#helper-structures)
    -   [Funciones](#functions)
    -   [Métodos](#methods)
    -   [Estructuras auxiliares](#helper-structures)
-   [Consecuencias de infringir las marcas estáticas](#consequences-of-violating-static-ness-flags)
-   [Administración de versiones](#version-management)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

La versión 1,0 de la firma raíz permite que las aplicaciones cambien libremente el contenido de los montones de descriptor y la memoria en la que señalan cada vez que las listas de comandos o agrupaciones que hacen referencia a ellos son potencialmente en vuelo en la GPU. Sin embargo, con mucha frecuencia, las aplicaciones no necesitan realmente la flexibilidad de cambiar los descriptores o la memoria después de que se hayan registrado los comandos que hacen referencia a ellos.

Las aplicaciones a menudo pueden:

-   Configure los descriptores (y la posible memoria a la que señalan) antes de enlazar las tablas de descriptores o los descriptores raíz en una lista de comandos o agrupación.
-   Asegúrese de que estos descriptores no cambien hasta que la lista de comandos/bundles que hace referencia a ellos haya terminado de ejecutarse por última vez.
-   Asegúrese de que los datos a los que apuntan los descriptores no cambian durante la misma duración completa.

Como alternativa, una aplicación solo puede tener en cuenta que los datos no cambian durante una duración más corta en el tiempo. En concreto, los datos pueden ser estáticos para la ventana en el tiempo durante la ejecución de la lista de comandos, ya que un enlace de parámetros raíz (tabla del descriptor o descriptor raíz) apunta actualmente a los datos. Dicho de otro modo, es posible que una aplicación desee realizar la ejecución en la escala de tiempo de GPU que actualiza algunos datos entre períodos de tiempo en los que se establece a través de un parámetro raíz, sabiendo que, cuando se establece, será estático.

Si los descriptores, o los descriptores de datos que apuntan a, no cambiarán, los controladores de optimizaciones específicos podrían ser específicos del proveedor de hardware y, lo que es importante, no cambian el comportamiento distinto al de mejorar el rendimiento. Conservar todo el conocimiento sobre la intención de la aplicación como sea posible no supone una carga en las aplicaciones.

Una optimización es que muchos controladores pueden producir accesos más eficaces a la memoria por parte de los sombreadores si saben las promesas que una aplicación puede hacer sobre la inestabilidad de los descriptores y los datos. Por ejemplo, los controladores podrían quitar un nivel de direccionamiento indirecto para tener acceso a un descriptor de un montón convirtiéndolo en un descriptor raíz si el hardware determinado no es sensible al tamaño del argumento raíz.

La tarea adicional para desarrolladores que usan la versión 1,1 es hacer promesas sobre la volatilidad y la unestática de los datos siempre que sea posible, para que los controladores puedan realizar las optimizaciones que tengan sentido. Los desarrolladores no tienen que hacer ninguna promesa sobre el estático.

La versión 1,0 de la firma raíz sigue funcionando sin cambios, aunque las aplicaciones que vuelvan a compilar las firmas raíz tendrán como valor predeterminado la firma raíz 1,1 ahora (con una opción para forzar la versión 1,0 si lo desea).

## <a name="static-and-volatile-flags"></a>Marcas estáticas y volátiles

Las marcas siguientes forman parte de la firma raíz para permitir que los controladores elijan una estrategia para administrar mejor los argumentos raíz individuales cuando se establecen, e incrustar también las mismas suposiciones en objetos de estado de canalización (PSO) cuando se compilan originalmente, ya que la firma raíz forma parte de un PSO.

La aplicación establece las marcas siguientes y se aplican a los descriptores o los datos.

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_FLAGS
{
    D3D12_DESCRIPTOR_RANGE_FLAG_NONE    = 0,
    D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE    = 0x1,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_VOLATILE   = 0x2,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE    = 0x4,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC = 0x8
} D3D12_DESCRIPTOR_RANGE_FLAGS;

typedef enum D3D12_ROOT_DESCRIPTOR_FLAGS
{
    D3D12_ROOT_DESCRIPTOR_FLAG_NONE = 0,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_VOLATILE    = 0x2,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE = 0x4,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC  = 0x8
} D3D12_ROOT_DESCRIPTOR_FLAGS;
```

### <a name="descriptors_volatile"></a>descriptores \_ volátiles

Con este marcador establecido, la aplicación puede cambiar los descriptores de un montón de descriptor al que apunta una tabla de descriptores raíz, excepto mientras la lista de comandos o agrupaciones que enlazan la tabla del descriptor se hayan enviado y no hayan terminado de ejecutarse. Por ejemplo, la grabación de una lista de comandos y la modificación posterior de descriptores en un montón de descriptores al que hace referencia *antes* de enviar la lista de comandos para su ejecución es válida. Este es el único comportamiento admitido de la versión 1,0 de la firma raíz.

Si \_ *no* se establece la marca volatile de descriptores, los descriptores son estáticos. No hay ninguna marca para este modo. Los descriptores estáticos suponen que los descriptores de un montón de descriptores a los que apunta una tabla de descriptores raíz se han inicializado en el momento en que se establece la tabla de descriptores en una lista de comandos o un lote (durante la grabación), y los descriptores no se pueden cambiar hasta que la lista de comandos o el *En la versión 1,1 de la firma raíz, los descriptores estáticos son la hipótesis predeterminada* y la aplicación tiene que especificar la marca volatile de descriptores \_ cuando sea necesario.

En el caso de las agrupaciones que utilizan tablas de descriptores con descriptores estáticos, los descriptores deben estar listos a partir del momento en que se registra la agrupación (en lugar de cuando se llama a la agrupación), y no cambian hasta que el paquete ha terminado de ejecutarse por última vez. Las tablas de descriptores que apuntan a descriptores estáticos se deben establecer durante la grabación de la agrupación y no se heredan en la agrupación. Es válido que una lista de comandos use una tabla de descriptores con descriptores estáticos que se haya establecido en una agrupación y devueltos de nuevo a la lista de comandos.

Cuando los descriptores son estáticos, hay otro cambio en el comportamiento que requiere que \_ se establezca la marca volatile de DEscriptores. Los accesos fuera de los límites a las vistas de búfer (en lugar de Texture1D/2D/3D/vistas de cubo) no son válidos y generan resultados indefinidos, incluido el posible restablecimiento de dispositivos, en lugar de devolver valores predeterminados para lecturas o eliminaciones de escrituras. El propósito de quitar la capacidad de las aplicaciones de depender del hardware fuera de los límites de la comprobación de acceso es permitir que los controladores decidan promover los accesos de los descriptores estáticos a los accesos del descriptor raíz si consideran que son más eficaces. Los descriptores raíz no admiten la comprobación de límites.

Si las aplicaciones dependen de un comportamiento seguro de acceso a memoria fuera de los límites al obtener acceso a los descriptores, deben marcar los intervalos de descriptor que tienen acceso a esos descriptores como descriptores \_ volatile.

### <a name="data_volatile"></a>DATOS \_ volátiles

Con este marcador establecido, la CPU puede cambiar los datos a los que apuntan los descriptores en cualquier momento, excepto mientras se hayan enviado la lista de comandos o agrupaciones que enlazan la tabla de descriptores y no se han terminado de ejecutar. Este es el único comportamiento admitido de la versión 1,0 de la firma raíz.

La marca está disponible en las marcas de intervalo de descriptor y en las marcas de descriptor raíz.

### <a name="data_static_while_set_at_execute"></a>DATOS \_ estáticos \_ mientras se \_ establecen \_ en \_ Execute

Con este marcador establecido, los datos a los que apuntan los descriptores no pueden cambiar a partir de cuando el descriptor raíz subyacente o la tabla de descriptor se establece en una lista de comandos o un lote durante la ejecución en la escala de tiempo de la GPU y finaliza cuando las operaciones de envío o distribución posteriores ya no hagan referencia a los datos.

Antes de que se haya establecido un descriptor de raíz o una tabla de descriptor en la GPU, estos datos se *pueden* cambiar incluso con la misma lista de comandos o lote. Los datos también se pueden cambiar mientras que un descriptor raíz o una tabla de descriptores que apuntan a él todavía están establecidos en el paquete o lista de comandos, siempre y cuando se hayan completado Draw/distribuciones que hacen referencia a él. Sin embargo, para ello es necesario volver a enlazar la tabla de descriptores a la lista de comandos antes de la próxima vez que se desreferencia el descriptor raíz o la tabla de descriptores. Esto permite que el controlador sepa que han cambiado los datos señalados por un descriptor raíz o una tabla de descriptores.

La diferencia fundamental entre los datos \_ estáticos \_ mientras \_ \_ se establecen en \_ la ejecución y los datos \_ volátiles es con los datos \_ volátiles un controlador no puede saber si las copias de datos en una lista de comandos han cambiado los datos a los que apunta un descriptor, sin realizar un seguimiento de estado adicional. Por lo tanto, si, por ejemplo, un controlador puede insertar cualquier tipo de comando de captura previa de datos en su lista de comandos (para que el acceso del sombreador a los datos conocidos sea más eficaz, por ejemplo, \_ los datos estáticos \_ mientras \_ \_ se establecen en \_ Execute permiten que el controlador sepa que solo necesita realizar la captura previa de los datos en el momento en que se establece a través de [**SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable), [**SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) o uno de los métodos para establecer la vista de búfer de constantes, la vista de recursos del sombreador o la vista de acceso desordenado.

En el caso de los paquetes, la promesa de que los datos son estáticos mientras se establece en Execute se aplica de forma única a cada ejecución de la agrupación.

La marca está disponible en las marcas de intervalo de descriptor y en las marcas de descriptor raíz.

### <a name="data_static"></a>DATOS \_ estáticos

Si se establece esta marca, los datos a los que apuntan los descriptores se han inicializado en el momento en que se ha establecido una tabla de descriptor o descriptor raíz que hace referencia a la memoria en una lista de comandos o un lote durante la grabación, y los datos no se pueden cambiar hasta que el lote o la lista de comandos termine de ejecutarse.

En el caso de los paquetes, la duración estática comienza en el descriptor de raíz o la configuración de la tabla de descriptor durante la grabación de la agrupación, en lugar de grabar la lista de comandos que realiza la llamada. Además, una tabla de descriptores que apunta a datos estáticos se debe establecer en la agrupación y no se puede heredar. Es válido para que una lista de comandos use una tabla de descriptores que apunte a los datos estáticos que se han establecido en una agrupación y devueltos a la lista de comandos.

La marca está disponible en las marcas de intervalo de descriptor y en las marcas de descriptor raíz.

### <a name="combining-flags"></a>Combinar marcas

Como máximo, se puede especificar una de las marcas de datos a la vez, excepto los intervalos de descriptores de muestra que no admiten marcas de datos en absoluto, ya que los ejemplos no apuntan a los datos.

La ausencia de marcadores de datos para los intervalos de descriptores SRV y CBV significa que se supone un valor predeterminado de datos \_ estáticos \_ mientras \_ \_ se establece en el \_ comportamiento de ejecución. La razón por la que se elige este valor predeterminado en lugar de datos \_ estáticos es que los datos \_ estáticos \_ mientras se \_ establecen \_ en la \_ ejecución es mucho más probable que sea un valor predeterminado seguro para la mayoría de los casos, al mismo tiempo que se sigue produciendo una oportunidad de optimización mejor que la predeterminada para los datos \_ volátiles.

La ausencia de marcadores de datos para los intervalos de descriptores de UAV significa \_ que se supone un comportamiento predeterminado de datos volatile, dado que normalmente UAVs se escribe en.

Los descriptores \_ volatile *no se* pueden combinar con datos \_ estáticos, pero se *pueden* combinar con las demás marcas de datos. La razón por la que los descriptores \_ volatile se pueden combinar con datos \_ estáticos \_ mientras \_ \_ se establece en \_ Execute es que los descriptores volátiles aún requieren que los descriptores estén listos durante la ejecución del lote o la lista de comandos, mientras que los datos \_ estáticos \_ mientras \_ \_ se establecen en \_ Execute solo hacen promesas sobre el estático en un subconjunto de la ejecución de la lista

### <a name="flag-summary"></a>Resumen de la marca

En las tablas siguientes se resumen las combinaciones de marcas que se pueden emplear.



|                                                                |                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Configuración válida \_ de \_ marcas de intervalo de descriptor D3D12 \_**             | **Descripción**                                                                                                                                                                                                                                                                                                                                      |
| No se ha establecido ninguna marca                                                   | Los descriptores son estáticos (valor predeterminado). Suposiciones predeterminadas para los datos: para SRV/CBV: DATA \_ static \_ mientras se \_ establece \_ en \_ Execute, y para UAV: Data \_ volatile. Estos valores predeterminados para SRV/CBV se ajustarán de forma segura a los patrones de uso de la mayoría de las firmas raíz.                                                                                              |
| DATOS \_ estáticos                                                   | Los descriptores y los datos son estáticos. Esto maximiza el potencial de optimización del controlador.                                                                                                                                                                                                                                                          |
| DATOS \_ volátiles                                                 | Los descriptores son estáticos y los datos son volátiles.                                                                                                                                                                                                                                                                                                     |
| DATOS \_ estáticos \_ mientras se \_ establecen \_ en \_ Execute                          | Los descriptores son estáticos y los datos son estáticos mientras se establecen en Execute.                                                                                                                                                                                                                                                                                      |
| descriptores \_ volátiles                                          | Los descriptores son volátiles y se realizan suposiciones predeterminadas sobre los datos: para SRV/CBV: DATA \_ static \_ mientras se \_ establece \_ en \_ Execute, y para UAV: Data \_ volatile.                                                                                                                                                                                              |
| descriptores \_ volatile \| Data \_ volatile                        | Los descriptores y los datos son volátiles, equivalentes a la firma raíz 1,0.                                                                                                                                                                                                                                                                            |
| descriptores \_ \| de datos volátiles \_ estáticos \_ mientras se \_ establecen \_ en \_ Execute | Los descriptores son volátiles, pero tenga en cuenta que todavía no les permite cambiar durante la ejecución de la lista de comandos. Por lo tanto, es válido combinar la declaración adicional de que los datos son estáticos mientras se establecen a través de la tabla del descriptor raíz durante la ejecución: los descriptores subyacentes son realmente estáticos durante más tiempo del que se promete que los datos son estáticos. |



 



|                                                   |                                                                                                                                                                                                                   |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Configuración válida \_ de \_ marcas de descriptor raíz de D3D12 \_** | **Descripción**                                                                                                                                                                                                   |
| No se ha establecido ninguna marca                                      | Suposiciones predeterminadas para los datos: para SRV/CBV: DATA \_ static \_ mientras se \_ establece \_ en \_ Execute, y para UAV: Data \_ volatile. Estos valores predeterminados para SRV/CBV se ajustarán de forma segura a los patrones de uso de la mayoría de las firmas raíz. |
| DATOS \_ estáticos                                      | Los datos son estáticos, el mejor potencial para la optimización del controlador.                                                                                                                                                       |
| DATOS \_ estáticos \_ mientras se \_ establecen \_ en \_ Execute             | Los datos son estáticos mientras se establecen en Execute.                                                                                                                                                                              |
| DATOS \_ volátiles                                    | Equivalente a la firma raíz 1,0.                                                                                                                                                                                 |



 

## <a name="version-11-api-summary"></a>Resumen de la API de la versión 1,1

Las siguientes llamadas de API habilitan la versión 1,1.

### <a name="enums"></a>Enumeraciones

Estas enumeraciones contienen las marcas de clave para especificar la volatilidad de los datos y el descriptor.

-   [**D3D \_ \_ \_ Versión de la firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version) : ID. de versión.
-   [**D3D12 \_ \_ \_ Marcas de intervalo de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) : un intervalo de marcas que determinan si los descriptores o los datos son volátiles o estáticos.
-   [**D3D12 \_ \_ \_ Marcas de descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) : un intervalo similar de marcas para las [**marcas de \_ \_ intervalo \_ de descriptores de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags), excepto que solo las marcas de datos se aplican a los descriptores raíz.

### <a name="structures"></a>Estructuras

Las estructuras actualizadas (de la versión 1,0) contienen referencias a las marcas Volatility/static.

-   [**D3D12 \_ \_ \_ \_ Firma raíz de datos de características**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature) : pase esta estructura a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) para comprobar la compatibilidad con la firma raíz 1,1.
-   [**D3D12 \_ La \_ firma raíz con versión \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) : puede contener cualquier versión de una descripción de la firma raíz y está diseñada para usarse con las funciones de serialización y deserialización que se enumeran a continuación.
-   Estas estructuras son equivalentes a las que se usan en la versión 1,0, con la adición de nuevos campos de marcas para los intervalos de descriptores y los descriptores raíz:

    -   [**D3D12 \_ raíz \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1)
    -   [**\_Descriptor D3D12 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
    -   [**D3D12 \_ el \_ descriptor raíz \_ TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
    -   [**\_DESCRIPTOR1 raíz \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
    -   [**D3D12 \_ raíz \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

### <a name="functions"></a>Functions

Los métodos enumerados aquí sustituyen las funciones [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) y [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) originales, ya que están diseñadas para funcionar en cualquier versión de la firma raíz. El formulario serializado es lo que se pasa a la API de [**CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) . Si se ha creado un sombreador con una firma raíz en él, el sombreador compilado contendrá ya una firma raíz serializada.

-   [**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) : Si una aplicación genera un procedimiento con la estructura de datos de la [**\_ \_ \_ firma raíz con versión D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) , debe crear el formulario serializado mediante esta función.
-   [**D3D12CreateVersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) : genera una interfaz que puede devolver la estructura de datos deserializada, a través de [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc).

### <a name="methods"></a>Métodos

La interfaz [**ID3D12VersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) se crea para deserializar la estructura de datos de la firma raíz.

-   [**GetRootSignatureDescAtVersion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getrootsignaturedescatversion) : convierte las estructuras de descripción de firma raíz en una versión solicitada.
-   [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc) : devuelve un puntero a una estructura de DESC de la [**\_ \_ \_ \_ firma raíz con versiones de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

### <a name="helper-structures"></a>Estructuras auxiliares

Las estructuras auxiliares se han agregado a ayuda para la inicialización de algunas de las estructuras de la versión 1,1.

-   \_Descriptor CD3DX12 \_ RANGE1
-   CD3DX12 \_ raíz \_ parámetro1
-   CD3DX12 \_ static \_ SAMPLER1
-   \_Descripción de la \_ \_ firma raíz \_ de CD3DX12 con versiones

Consulte [estructuras y funciones auxiliares para D3D12](helper-structures-and-functions-for-d3d12.md).

## <a name="consequences-of-violating-static-ness-flags"></a>Consecuencias de infringir las marcas estáticas

El descriptor y las marcas de datos descritos anteriormente (así como los valores predeterminados que la ausencia de marcas concretas) definen una promesa por parte de la aplicación para que el controlador se comporte. Si una aplicación infringe la promesa, este comportamiento no es válido: los resultados son indefinidos y pueden ser diferentes en distintos controladores y hardware.

El nivel de depuración tiene opciones para validar que las aplicaciones respetan sus promesas, incluidas las promesas predeterminadas que se usan con la firma raíz versión 1,1 sin establecer ninguna marca.

## <a name="version-management"></a>Administración de versiones

Al compilar las signaturas raíz asociadas a los sombreadores, los compiladores HLSL más recientes volverán a compilar la firma raíz en la versión 1,1, mientras que los compiladores HLSL anteriores solo admiten 1,0. Tenga en cuenta que las signaturas raíz 1,1 no funcionarán en el sistema operativo que no admiten la firma raíz 1,1.

La versión de la firma raíz compilada con un sombreador se puede forzar a una versión concreta mediante `/force_rootsig_ver <version>` . Forzar la versión se realizará correctamente si el compilador puede conservar el comportamiento de la firma raíz que se está compilando en la versión forzada, por ejemplo, quitando las marcas no admitidas en la firma raíz que solo sirven para fines de optimización pero que no afectan al comportamiento.

De este modo, una aplicación puede, por ejemplo, compilar una firma raíz 1,1 a 1,0 y 1,1 al compilar la aplicación y seleccionar la versión adecuada en tiempo de ejecución según el nivel de compatibilidad del sistema operativo. Sin embargo, sería más eficaz para una aplicación compilar firmas raíz individualmente (especialmente si se necesitan varias versiones), independientemente de los sombreadores. Incluso si los sombreadores no se compilan inicialmente con una firma raíz adjunta, la ventaja de la validación del compilador de la compatibilidad con la firma raíz con un sombreador se puede conservar mediante la `/verifyrootsignature` opción del compilador. Más adelante, en tiempo de ejecución, PSO se puede crear con sombreadores que no tienen firmas raíz en ellos al pasar la firma raíz deseada (quizás la versión adecuada admitida por el sistema operativo) como parámetro independiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una firma raíz](creating-a-root-signature.md)
</dt> <dt>

[Firmas raíz](root-signatures.md)
</dt> <dt>

[Especificación de firmas de raíz en HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 




