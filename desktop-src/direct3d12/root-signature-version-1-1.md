---
title: Versión 1.1 de la firma raíz
description: El propósito de la versión 1.1 de la firma raíz es permitir que las aplicaciones indiquen a los controladores cuándo los descriptores de un montón de descriptores no cambian o los descriptores de datos apuntan a que no cambian.
ms.assetid: 8FE42C1C-7F1D-4E70-A7EE-D5EC67237327
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a7a32576efa4d93a8d26aa57282f06e0d5a02f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343670"
---
# <a name="root-signature-version-11"></a>Versión 1.1 de la firma raíz

El propósito de la versión 1.1 de la firma raíz es permitir que las aplicaciones indiquen a los controladores cuándo los descriptores de un montón de descriptores no cambian o los descriptores de datos apuntan a que no cambian. Esto permite que los controladores realicen optimizaciones que podrían ser posibles sabiendo que un descriptor o la memoria a la que apunta es estático durante un período de tiempo.

-   [Información general](#overview)
-   [Marcas estáticas y volátiles](#static-and-volatile-flags)
    -   [DESCRIPTORES \_ VOLÁTILES](#descriptors_volatile)
    -   [DATOS \_ VOLÁTILES](#data_volatile)
    -   [DATOS \_ ESTÁTICOS \_ MIENTRAS SE ESTABLECE \_ EN \_ \_ EJECUCIÓN](#data_static_while_set_at_execute)
    -   [DATA \_ STATIC](#data_static)
    -   [Combinar marcas](#combining-flags)
    -   [Resumen de marcas](#flag-summary)
-   [Resumen de api de la versión 1.1](#version-11-api-summary)
    -   [Enumeraciones](#enums)
    -   [Estructuras](#helper-structures)
    -   [Funciones](#functions)
    -   [Métodos](#methods)
    -   [Estructuras auxiliares](#helper-structures)
-   [Consecuencias de infringir las marcas de integridad estática](#consequences-of-violating-static-ness-flags)
-   [Administración de versiones](#version-management)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Root Signature versión 1.0 permite que las aplicaciones cambien libremente el contenido de los montones de descriptores y la memoria a la que apuntan cada vez que las listas de comandos o agrupaciones que hacen referencia a ellos estén potencialmente en marcha en la GPU. Sin embargo, a menudo, las aplicaciones no necesitan realmente la flexibilidad para cambiar descriptores o memoria después de que se hayan registrado los comandos que hacen referencia a ellos.

A menudo, las aplicaciones pueden:

-   Configure descriptores (y posiblemente la memoria a la que apuntan) antes de enlazar tablas de descriptores o descriptores raíz en una lista o agrupación de comandos.
-   Asegúrese de que estos descriptores no cambiarán hasta que la lista de comandos /bundles que hace referencia a ellos haya terminado de ejecutarse por última vez.
-   Asegúrese de que los datos a los que apuntan los descriptores no cambian durante la misma duración completa.

Como alternativa, es posible que una aplicación solo pueda respetar que los datos no cambien durante un período de tiempo más corto. En concreto, los datos pueden ser estáticos para la ventana en el tiempo durante la ejecución de la lista de comandos que un enlace de parámetros raíz (tabla descriptor o descriptor raíz) apunta actualmente a los datos. En otras palabras, es posible que una aplicación desee realizar la ejecución en la escala de tiempo de GPU que actualiza algunos datos entre períodos de tiempo en los que se establece a través de un parámetro raíz, sabiendo que cuando se establece será estático.

Si los descriptores o los descriptores de datos apuntan a no cambiarán, los controladores de optimizaciones específicos podrían ser específicos del proveedor de hardware y, lo que es importante, no cambian el comportamiento que no sea posiblemente mejorar el rendimiento. Conservar tantos conocimientos sobre la intención de la aplicación como sea posible no supone una carga para las aplicaciones.

Una optimización es que muchos controladores pueden generar accesos a memoria más eficaces mediante sombreadores si conocen las promesas que una aplicación puede hacer sobre la estática de descriptores y datos. Por ejemplo, los controladores podrían quitar un nivel de direccionamiento indirecto para acceder a un descriptor de un montón si lo convierten en un descriptor raíz si el hardware determinado no es sensible al tamaño del argumento raíz.

La tarea adicional para el desarrollador que usa la versión 1.1 es hacer promesas sobre la inestabilidad y la estática de los datos siempre que sea posible, para que los controladores puedan hacer las optimizaciones que tienen sentido. Los desarrolladores no tienen que hacer ninguna promesa sobre la estática.

La versión 1.0 de la firma raíz sigue funcionando sin cambios, aunque las aplicaciones que vuelvan a compilar firmas raíz tendrán como valor predeterminado la firma raíz 1.1 ahora (con la opción de forzar la versión 1.0 si lo desea).

## <a name="static-and-volatile-flags"></a>Marcas estáticas y volátiles

Las marcas siguientes forman parte de la firma raíz para permitir que los controladores elijan una estrategia para controlar mejor los argumentos raíz individuales cuando se establecen, y también insertan las mismas suposiciones en objetos de estado de canalización (PSO) cuando se compilan originalmente, ya que la firma raíz forma parte de un PSO.

La aplicación establece las marcas siguientes y se aplican a descriptores o datos.

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

### <a name="descriptors_volatile"></a>DESCRIPTORES \_ VOLÁTILES

Con este marcador establecido, la aplicación puede cambiar los descriptores de un montón de descriptores al que apunta una tabla de descriptores raíz en cualquier momento, excepto cuando se han enviado la lista de comandos o agrupaciones que enlazan la tabla de descriptores y no han terminado de ejecutarse. Por ejemplo, es válido registrar una lista de comandos y,  posteriormente, cambiar descriptores en un montón de descriptores al que hace referencia antes de enviar la lista de comandos para su ejecución. Este es el único comportamiento admitido de root signature versión 1.0.

Si no se establece \_ la marca VOLATILE de DESCRIPTORS, los descriptores son estáticos.  No hay ninguna marca para este modo. Los descriptores estáticos significan que los descriptores de un montón de descriptores al que apunta una tabla de descriptores raíz se han inicializado cuando la tabla de descriptores se establece en una lista de comandos o agrupación (durante la grabación), y los descriptores no se pueden cambiar hasta que la lista o agrupación de comandos haya terminado de ejecutarse por última vez. *Para la firma raíz versión 1.1, los descriptores estáticos* son la suposición predeterminada y la aplicación tiene que especificar la marca VOLATILE de DESCRIPTORS \_ cuando sea necesario.

En el caso de las agrupaciones que usan tablas de descriptores con descriptores estáticos, los descriptores deben estar listos a partir del momento en que se registra la agrupación (en lugar de cuando se llama a la agrupación) y no cambiar hasta que la agrupación haya terminado de ejecutarse por última vez. Las tablas de descriptores que apuntan a descriptores estáticos deben establecerse durante la grabación de agrupación y no heredar en la agrupación. Es válido que una lista de comandos use una tabla de descriptores con descriptores estáticos establecidos en una agrupación y devueltos a la lista de comandos.

Cuando los descriptores son estáticos, hay otro cambio de comportamiento que requiere que se establezca la marca \_ VOLATILE de DESCRIPTORS. Los accesos fuera de límites a las vistas de búfer (en lugar de las vistas Texture1D/2D/3D/Cube) no son válidos y generan resultados indefinidos, incluido el posible restablecimiento del dispositivo, en lugar de devolver valores predeterminados para lecturas o colocaciones de escrituras. El propósito de quitar la capacidad de las aplicaciones de depender de la comprobación de acceso de hardware fuera de los límites es permitir que los controladores elijan promover los accesos de descriptor estáticos a los accesos de descriptor raíz si lo consideran más eficaz. Los descriptores raíz no admiten ninguna comprobación fuera de límites.

Si las aplicaciones dependen del comportamiento seguro de acceso a memoria fuera de límites al acceder a descriptores, deben marcar los intervalos de descriptores que tienen acceso a esos descriptores como DESCRIPTORS \_ VOLATILE.

### <a name="data_volatile"></a>DATOS \_ VOLÁTILES

Con esta marca establecida, la CPU puede cambiar los datos a los que apuntan los descriptores en cualquier momento, excepto si se han enviado la lista de comandos o agrupaciones que enlazan la tabla de descriptores y no han terminado de ejecutarse. Este es el único comportamiento admitido de la firma raíz versión 1.0.

La marca está disponible tanto en las marcas de rango de descriptor como en las marcas de descriptor raíz.

### <a name="data_static_while_set_at_execute"></a>DATOS \_ \_ ESTÁTICOS MIENTRAS \_ SE ESTABLECE EN \_ \_ EJECUCIÓN

Con esta marca establecida, los datos a los que apuntan los descriptores no pueden cambiar a partir de cuando el descriptor raíz subyacente o la tabla de descriptores se establecen en una lista de comandos o agrupación durante la ejecución en la escala de tiempo de GPU y finalizan cuando los posteriores draws/dispatches ya no hacen referencia a los datos.

Antes de establecer un descriptor raíz o una  tabla de descriptores en la GPU, estos datos se pueden cambiar incluso con la misma lista o agrupación de comandos. Los datos también se pueden cambiar mientras un descriptor raíz o una tabla de descriptores que apuntan a él todavía se establece en la lista de comandos o agrupación, siempre y cuando se hayan completado draw/dispatches que hacen referencia a él. Sin embargo, para ello es necesario volver a enlazar la tabla de descriptores a la lista de comandos antes de la próxima vez que se desreferencia el descriptor raíz o la tabla de descriptores. Esto permite al controlador saber que los datos a los que apunta un descriptor raíz o una tabla de descriptores han cambiado.

La diferencia esencial entre DATA STATIC WHILE SET AT EXECUTE y DATA VOLATILE es que DATA VOLATILE un controlador no puede saber si las copias de datos de una lista de comandos han cambiado los datos a los que apunta un descriptor, sin realizar un seguimiento de estado \_ \_ \_ \_ \_ \_ \_ adicional. Por ejemplo, si un controlador puede insertar cualquier tipo de comandos de captura previa de datos en su lista de comandos (para que el acceso del sombreador a datos conocidos sea más eficaz, por ejemplo), DATA STATIC WHILE SET AT EXECUTE permite al controlador saber que solo necesita realizar la captura previa de datos en el momento en que se establece a través de \_ \_ \_ \_ \_ [**SetGraphicsRootDescriptorTable,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) [**SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) o uno de los métodos para establecer la vista de búfer constante, la vista de recursos de sombreador o la vista de acceso sin ordenar.

En el caso de los paquetes, la promesa de que los datos son estáticos mientras se establecen en ejecución se aplica de forma única a cada ejecución del paquete.

La marca está disponible tanto en las marcas de rango de descriptor como en las marcas de descriptor raíz.

### <a name="data_static"></a>DATA \_ STATIC

Si se establece esta marca, los datos a los que apuntan los descriptores se han inicializado en el momento en que se ha establecido un descriptor raíz o una tabla de descriptores que hace referencia a la memoria en una lista de comandos o agrupación durante la grabación, y los datos no se pueden cambiar hasta que la lista o agrupación de comandos haya terminado de ejecutarse por última vez.

En el caso de los lotes, la duración estática comienza en la configuración del descriptor raíz o de la tabla de descriptores durante la grabación del paquete, en lugar de la grabación de una lista de comandos de llamada. Además, se debe establecer una tabla de descriptores que apunte a datos estáticos en la agrupación y no heredar. Es válido que una lista de comandos use una tabla de descriptores que apunte a datos estáticos que se han establecido en una agrupación y devueltos a la lista de comandos.

La marca está disponible tanto en las marcas de rango de descriptor como en las marcas de descriptor raíz.

### <a name="combining-flags"></a>Combinar marcas

Como máximo, se puede especificar una de las marcas DATA a la vez, excepto los intervalos de descriptores de sampler que no admiten marcas DATA, ya que los muestreadores no apuntan a los datos.

La ausencia de marcas DE DATOS para los intervalos de descriptores SRV y CBV significa que se supone un comportamiento predeterminado de DATA \_ STATIC WHILE SET AT \_ \_ \_ \_ EXECUTE. La razón por la que se elige este valor predeterminado en lugar de DATA STATIC es que DATA STATIC WHILE SET AT EXECUTE es mucho más probable que sea un valor predeterminado seguro para la mayoría de los casos, a la vez que se produce alguna oportunidad de optimización mejor que el valor predeterminado de \_ \_ DATA \_ \_ \_ \_ \_ VOLATILE.

La ausencia de marcas DE DATOS para los intervalos de descriptores UAV significa que se supone un comportamiento volátil de datos predeterminado, dado que normalmente se escriben \_ UAV en .

DESCRIPTORS \_ VOLATILE no *se* puede combinar con DATA \_ STATIC, pero *se* puede combinar con las otras marcas DE DATOS. La razón por la que DESCRIPTORS VOLATILE se puede combinar con DATA STATIC WHILE SET AT EXECUTE es que los descriptores volátiles todavía requieren que los descriptores estén listos durante la ejecución de la lista de comandos o agrupación, y DATA STATIC WHILE SET AT EXECUTE solo hace promesas sobre la estática en un subconjunto de la ejecución de la lista de comandos o \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ agrupación.

### <a name="flag-summary"></a>Resumen de marcas

En las tablas siguientes se resumen las combinaciones de marcas que se pueden emplear.



| Configuración válida de LAS MARCAS DE RANGO DEL DESCRIPTOR D3D12 \_ \_ \_                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sin marcas establecidas                                                   | Los descriptores son estáticos (el valor predeterminado). Suposiciones predeterminadas para los datos: para SRV/CBV: DATA \_ STATIC WHILE SET AT EXECUTE y para \_ \_ \_ \_ UAV: DATA \_ VOLATILE. Estos valores predeterminados para SRV/CBV se ajustarán de forma segura a los patrones de uso de la mayoría de las firmas raíz.                                                                                              |
| DATA \_ STATIC                                                   | Tanto los descriptores como los datos son estáticos. Esto maximiza el potencial de optimización del controlador.                                                                                                                                                                                                                                                          |
| DATOS \_ VOLÁTILES                                                 | Los descriptores son estáticos y los datos son volátiles.                                                                                                                                                                                                                                                                                                     |
| DATOS \_ ESTÁTICOS \_ MIENTRAS SE ESTABLECE \_ EN \_ \_ EJECUCIÓN                          | Los descriptores son estáticos y los datos son estáticos mientras se establecen en ejecución.                                                                                                                                                                                                                                                                                      |
| DESCRIPTORES \_ VOLÁTILES                                          | Los descriptores son volátiles y se realizan suposiciones predeterminadas sobre los datos: para SRV/CBV: DATA STATIC WHILE SET AT EXECUTE y para \_ \_ \_ \_ \_ UAV: DATA \_ VOLATILE.                                                                                                                                                                                              |
| DESCRIPTORES \_ \| VOLÁTILES DE \_ DATOS VOLÁTILES                        | Tanto los descriptores como los datos son volátiles, equivalentes a root signature 1.0.                                                                                                                                                                                                                                                                            |
| DESCRIPTORES \_ VOLATILE DATA STATIC WHILE SET AT \| \_ \_ \_ \_ \_ EXECUTE | Los descriptores son volátiles, pero tenga en cuenta que todavía no les permite cambiar durante la ejecución de la lista de comandos. Por lo tanto, es válido combinar la declaración adicional de que los datos son estáticos mientras se establecen a través de la tabla de descriptores raíz durante la ejecución: los descriptores subyacentes son estáticos durante más tiempo que los datos que se están con la promesa de ser estáticos. |



 



| Configuración válida de MARCAS DE \_ \_ DESCRIPTOR RAÍZ D3D12 \_                                                  |  Descripción                                                                                                                                                                                                                 |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sin marcas establecidas                                      | Suposiciones predeterminadas para los datos: para SRV/CBV: DATA \_ STATIC WHILE SET AT EXECUTE y para \_ \_ \_ \_ UAV: DATA \_ VOLATILE. Estos valores predeterminados para SRV/CBV se ajustarán de forma segura a los patrones de uso de la mayoría de las firmas raíz. |
| DATA \_ STATIC                                      | Los datos son estáticos, el mejor potencial para la optimización del controlador.                                                                                                                                                       |
| DATOS \_ \_ ESTÁTICOS MIENTRAS \_ SE ESTABLECE EN \_ \_ EJECUCIÓN             | Los datos son estáticos mientras se establecen en ejecución.                                                                                                                                                                              |
| DATOS \_ VOLÁTILES                                    | Equivalente a root signature 1.0.                                                                                                                                                                                 |



 

## <a name="version-11-api-summary"></a>Resumen de api de la versión 1.1

Las siguientes llamadas API habilitan la versión 1.1.

### <a name="enums"></a>Enumeraciones

Estas enumeraciones contienen las marcas de clave para especificar el descriptor y la inestabilidad de los datos.

-   [**D3D \_ ROOT \_ SIGNATURE \_ VERSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version) : identificadores de versión.
-   [**D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) : intervalo de marcas que determina si los descriptores o los datos son volátiles o estáticos.
-   [**D3D12 \_ MARCAS \_ DE DESCRIPTOR \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) RAÍZ: un intervalo similar de marcas a [**D3D12 \_ DESCRIPTOR RANGE \_ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags), salvo que solo las marcas de datos se aplican a los descriptores raíz.

### <a name="structures"></a>Estructuras

Las estructuras actualizadas (de la versión 1.0) contienen referencias a las marcas de inestabilidad o estáticas.

-   [**D3D12 \_ FEATURE \_ DATA \_ ROOT \_ SIGNATURE:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature) pase esta estructura a [**CheckFeatureSupport para**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) comprobar la compatibilidad con la firma raíz versión 1.1.
-   [**D3D12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) puede contener cualquier versión de una descripción de firma raíz y está diseñado para usarse con las funciones de serialización y deserialización que se enumeran a continuación.
-   Estas estructuras son equivalentes a las usadas en la versión 1.0, con la adición de nuevos campos de marcas para rangos de descriptores y descriptores raíz:

    -   [**D3D12 \_ ROOT \_ SIGNATURE \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1)
    -   [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
    -   [**D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
    -   [**DESCRIPTOR RAÍZ D3D121 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
    -   [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

### <a name="functions"></a>Functions

Los métodos enumerados aquí reemplazan a las funciones [**originales D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) y [**D3D12CreateRootSignatureDeserializer,**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) ya que están diseñadas para funcionar en cualquier versión de la firma raíz. El formulario serializado es lo que se pasa a la API [**CreateRootSignature.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) Si se ha creado un sombreador con una firma raíz en él, el sombreador compilado contendrá ya una firma raíz serializada.

-   [**D3D12SerializeVersionedRootSignature:**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) si una aplicación genera por procedimientos la estructura de datos [**D3D12 \_ \_ VERSIONED ROOT \_ SIGNATURE,**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) debe crear el formulario serializado mediante esta función.
-   [**D3D12CreateVersionedRootSignatureDeserializer:**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) genera una interfaz que puede devolver la estructura de datos deserializado a través de [**GetUnconvertedRootSignatureDesc.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc)

### <a name="methods"></a>Métodos

La [**interfaz ID3D12VersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) se crea para deserializar la estructura de datos de firma raíz.

-   [**GetRootSignatureDescAtVersion:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getrootsignaturedescatversion) convierte las estructuras de descripción de firma raíz en una versión solicitada.
-   [**GetUnconvertedRootSignatureDesc:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc) devuelve un puntero a una estructura [**D3D12 \_ \_ VERSIONED ROOT \_ SIGNATURE \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)

### <a name="helper-structures"></a>Estructuras auxiliares

Las estructuras auxiliares se han agregado para ayudar en la inicialización de algunas de las estructuras de la versión 1.1.

-   CD3DX12 \_ DESCRIPTOR \_ RANGE1
-   CD3DX12 \_ ROOT \_ PARAMETER1
-   CD3DX12 \_ STATIC \_ SAMPLER1
-   CD3DX12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC

Consulte Estructuras [y funciones auxiliares para D3D12.](helper-structures-and-functions-for-d3d12.md)

## <a name="consequences-of-violating-static-ness-flags"></a>Consecuencias de infringir las marcas de integridad estática

El descriptor y las marcas de datos descritas anteriormente (así como los valores predeterminados implícitos por la ausencia de marcas concretas) definen una promesa de la aplicación al controlador sobre cómo se comportará. Si una aplicación infringe la promesa, este comportamiento no es válido: los resultados son indefinidos y pueden ser diferentes en distintos controladores y hardware.

La capa de depuración tiene opciones para validar que las aplicaciones respetan sus promesas, incluidas las promesas predeterminadas que incluyen el uso de la firma raíz versión 1.1 sin establecer ninguna marca.

## <a name="version-management"></a>Administración de versiones

Al compilar firmas raíz asociadas a sombreadores, los compiladores HLSL más recientes compilarán de forma predeterminada la firma raíz en la versión 1.1, mientras que los compiladores HLSL antiguos solo admiten la versión 1.0. Tenga en cuenta que las firmas raíz 1.1 no funcionarán en los so que no admiten la firma raíz 1.1.

La versión de firma raíz compilada con un sombreador se puede forzar a una versión determinada mediante `/force_rootsig_ver <version>` . Forzar la versión se realizará correctamente si el compilador puede conservar el comportamiento de la firma raíz que se compila en la versión forzada, por ejemplo, quitando marcas no admitidas en la firma raíz que sirven solo para fines de optimización, pero que no afectan al comportamiento.

De este modo, una aplicación puede, por ejemplo, compilar una firma raíz 1.1 en 1.0 y 1.1 al compilar la aplicación y seleccionar la versión adecuada en tiempo de ejecución en función del nivel de compatibilidad del sistema operativo. Sin embargo, sería más eficaz el espacio para que una aplicación compile firmas raíz individualmente (especialmente si se necesitan varias versiones), independientemente de los sombreadores. Incluso si los sombreadores no se compilan inicialmente con una firma raíz adjunta, la ventaja de la validación del compilador de la compatibilidad de la firma raíz con un sombreador se puede conservar mediante la opción `/verifyrootsignature` del compilador. Más adelante en tiempo de ejecución, los PSO se pueden crear mediante sombreadores que no tienen firmas raíz en ellos mientras se pasa la firma raíz deseada (quizás la versión adecuada compatible con el sistema operativo) como un parámetro independiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de una firma raíz](creating-a-root-signature.md)
</dt> <dt>

[Firmas raíz](root-signatures.md)
</dt> <dt>

[Especificación de firmas de raíz en HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 




