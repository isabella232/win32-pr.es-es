---
description: Confiabilidad y seguridad
ms.assetid: 1cbfabce-3d56-4e23-b9a7-02369c67e392
title: Confiabilidad y seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0f0e4a244de2c1463cdadb76162c18b041812b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688128"
---
# <a name="reliability-and-security"></a>Confiabilidad y seguridad

Dado que los códecs de componentes de imágenes de Windows (WIC) se invocarán desde el shell de Windows y la Galería fotográfica de, los creadores de códec deben hacer todo lo posible para garantizar un alto nivel de confiabilidad y seguridad en sus códecs WIC.

La escritura de código confiable depende en gran medida de buenas prácticas de codificación, revisiones de código eficaces y pruebas unitarias y pruebas de escenarios exhaustivas. Además, las siguientes instrucciones le ayudarán a asegurarse de que el códec cumple con las directivas de Windows Vista con respecto a la confiabilidad.

-   Habilitar la cancelación de e/s.

    Los creadores de códec deben proporcionar una manera para que el usuario final cancele cualquier operación de ejecución prolongada. Los códecs WIC lo admiten mediante la implementación de IWICBitmapProgressNotification. Esto permite a una aplicación que llama especificar una función de devolución de llamada para que el códec llame a intervalos especificados para notificar al autor de la llamada sobre el progreso de la operación actual. Cuando una aplicación devuelve un ERROR \_ cancelado de la función de devolución de llamada, el códec debe cancelar la operación en curso y propagar el valor HRESULT de nuevo al autor de la llamada. Esto es especialmente importante en el caso de los códecs sin formato, ya que puede tardar varios segundos en descodificar una imagen sin formato de tamaño completo y las aplicaciones necesitan una forma de anular este procesamiento.

-   Asegúrese de que el código se ejecuta en el ámbito más pequeño necesario para realizar su función.

    Los creadores de códecs deben asegurarse de que el códec no consuma más recursos de los necesarios o que tengan un ámbito mayor del necesario. El ámbito de un códec en WIC es un archivo de imagen único; el códec se crea cuando se carga un archivo de imagen y el códec se libera cuando se cierra la imagen. Dado que WIC es una plataforma basada en componentes extensible, los códecs WIC tendrán cargas y descargaciones que se superponen, y se inicia y se detiene, todo dentro del mismo proceso. Si la infraestructura subyacente de un códec requiere operaciones de inicio y detención en un ámbito mayor que una sola imagen, la confiabilidad se verá afectada. Los códecs habilitados para WIC se utilizarán en el explorador de Windows, así como en otras aplicaciones. Por lo tanto, si un códec permanece cargado mientras dure el proceso, la memoria no se liberará de forma eficaz y un error del códec podría bloquear el explorador de Windows y requerir un reinicio del equipo. (Tenga en cuenta que el códec se invocará cada vez que una imagen se ponga en miniatura por primera vez en el explorador de Windows: es fundamental que se trata de una operación ligera).

-   Usar herramientas de análisis de código estático y dinámico.

    -   Herramientas de análisis estático:

        Prefijo: para detectar errores en tiempo de compilación.

        Rápido: para analizar código en busca de errores.

    -   Herramientas de análisis dinámico:

        AppVerifier, que ayuda a mejorar la resistencia de las aplicaciones mediante la simulación de problemas comunes del software real.

-   Compruebe todas las entradas en las revisiones de código.

    Todos los parámetros de los métodos exportados y todos los datos de archivo deben comprobarse cuidadosamente para comprobar su validez y rechazarse de forma sólida si se produce un error, con el fin de protegerse frente a saturaciones del búfer y subprocesos, desbordamientos aritméticos y subdesbordamientos, y tipos inesperados.

-   Utilice técnicas de aproximación de archivos para detectar posibles bloqueos y bloqueos.

    La aproximación de archivos es el proceso de probar el códec con entradas permutadas aleatoriamente.

    Hay dos formas de hacer una aproximación de archivos: las aproximaciones no directas (aleatorias) y las aproximadas dirigidas. La aproximación no dirigida realiza un volteo de bits aleatorio para ver si la entrada aleatoria puede bloquear el códec. La aproximación a la entrada se silencia en función de algún conocimiento del formato de archivo. Por ejemplo, si hay una comprobación de redundancia de ciclo (CRC) en el desplazamiento de bytes 32, es probable que el cambio de cualquier byte sin actualizar el CRC no ejerza la mayor parte de los rutas. En este ejemplo, un comparador dirigido debe corregir el CRC cuando se modifican los bytes.

    Se debe crear el conjunto de entrada de imágenes para la aproximación de archivos, de forma que se pruebe cada combinación de parámetros que admita el descodificador. Por ejemplo, si el descodificador admite archivos poco y big-endian y tres valores de compresión, el conjunto de entrada de imagen debe constar de archivos Little-Endian de cada configuración de compresión y archivos Big-Endian para cada configuración de compresión. Este enfoque producirá un conjunto grande, pero muy sólido, de imágenes de entrada que se van a probar. Incluso si ninguna cámara produce cada una de las combinaciones, pero el descodificador es compatible con estas combinaciones teóricas, los creadores de códecs deben aproximar estas entradas.

    La seguridad se puede mejorar considerablemente mediante la realización de pruebas aproximadas de archivos de imagen durante el desarrollo de códecs. Los códecs siempre deben ser capaces de detectar daños en los archivos de imagen y producir errores en el caso de una solicitud con formato incorrecto o de datos mal formados.

-   Haga hincapié en el código.

    Stress: Pruebe el códec, para lo que debe ejecutarlo continuamente en varios procesos simultáneos, realizando todas las operaciones admitidas en todas las secuencias posibles, en imágenes de tamaños diferentes (incluidas imágenes muy grandes) de cada cámara compatible.

-   Seguridad para subprocesos.

    A partir de Windows 7, WIC requiere que los CÓDECs sin formato tengan el tipo de Apartamento COM "both". Esto significa que debe realizar el bloqueo adecuado para administrar llamadores y llamadores entre apartamentos en escenarios de varios subprocesos. Se puede llamar a los objetos de un contenedor multiproceso (MTA) simultáneamente en cualquier número de subprocesos del MTA, lo que permite un mejor rendimiento en los sistemas de varios núcleos y en determinados escenarios de servidor. Además, los CÓDECs WIC que viven dentro de un MTA pueden llamar a otros objetos que viven dentro del MTA sin el costo de serialización asociado a la llamada entre subprocesos que residen en distintos apartamentos STA. En Windows 7, todos los CÓDECs WIC integrados se han actualizado para admitir MTA, como JPEG, TIFF, PNG, GIF, ICO y BMP. los CÓDECs de terceros que no son compatibles con los MTA provocarán importantes costos de rendimiento en las aplicaciones multiproceso debido a la serialización. La habilitación de la compatibilidad con MTA requiere que se implemente la sincronización adecuada en el códec de terceros. La implementación exacta de estas técnicas de sincronización está fuera del ámbito de este documento. A continuación se proporciona una referencia general para la sincronización de objetos COM.

    https://msdn.microsoft.com/library/ms809971.aspx

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Instrucciones de WIC para formatos de imagen RAW de cámara](-wic-rawguidelines.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



