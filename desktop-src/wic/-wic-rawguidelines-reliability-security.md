---
description: Confiabilidad y seguridad
ms.assetid: 1cbfabce-3d56-4e23-b9a7-02369c67e392
title: Confiabilidad y seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a4704b84d09698fd6fabcf2d190050063ec3b3190904aa669fa78799c5d0158
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441735"
---
# <a name="reliability-and-security"></a>Confiabilidad y seguridad

Dado que Windows Imaging Component (WIC) códecs se invocarán desde el shell de Windows y Galería de fotos, los autores de códecs deben hacer todo lo posible para garantizar un alto nivel de confiabilidad y seguridad en sus códecs WIC.

La escritura de código confiable depende en gran medida de procedimientos de codificación correctos, revisiones de código eficaces y pruebas unitarias exhaustivas y pruebas de escenarios. Además, las siguientes directrices le ayudarán a garantizar que el códec cumple las Windows Vista con respecto a la confiabilidad.

-   Habilite la cancelación de E/S.

    Los autores de códecs deben proporcionar una manera de que el usuario final cancele cualquier operación de ejecución larga. Los códecs wic admiten esto mediante la implementación de IWICBitmapProgressNotification. Esto permite que una aplicación que realiza la llamada especifique una función de devolución de llamada para que el códec llame a intervalos especificados para notificar al autor de la llamada el progreso de la operación actual. Cuando una aplicación devuelve ERROR CANCELLED desde la función de devolución de llamada, el códec debe cancelar cualquier operación que esté en curso y propagar el HRESULT de nuevo \_ al autor de la llamada. Esto es especialmente importante para los códecs RAW, ya que puede tardar varios segundos en descodificar una imagen RAW de tamaño completo y las aplicaciones necesitan una manera de anular este procesamiento.

-   Asegúrese de que el código se ejecuta en el ámbito más pequeño necesario para realizar su función.

    Los autores de códecs deben asegurarse de que el códec no consume más recursos de los necesarios o tienen un ámbito mayor del necesario. El ámbito de un códec en WIC es un único archivo de imagen; el códec se crea cuando se carga un archivo de imagen y el códec se libera cuando se cierra la imagen. Dado que WIC es una plataforma extensible basada en componentes, los códecs WIC tendrán cargas y descargas superpuestas, y se inician y detienen, todo dentro del mismo proceso. Si la infraestructura subyacente de un códec requiere operaciones de inicio y detenerse en un ámbito mayor que una sola imagen, la confiabilidad se verá afectada. Los códecs habilitados para WIC se usarán en Windows Explorer, así como en otras aplicaciones. Por lo tanto, si un códec permanece cargado durante la vigencia del proceso, la memoria no se liberará de forma eficaz y un error del códec podría Windows Explorer y, potencialmente, requerir que se reinicie la máquina. (Tenga en cuenta que el códec se invocará cada vez que se cree una imagen en miniatura por primera vez en Windows Explorer: es esencial que se trata de una operación ligera).

-   Use herramientas de análisis de código estático y dinámico.

    -   Herramientas de análisis estático:

        PREfix: para detectar errores en tiempo de compilación.

        PREfast: para analizar el código en busca de errores.

    -   Herramientas de análisis dinámico:

        AppVerifier: ayuda a que las aplicaciones sean más resistentes mediante la simulación de problemas de software comunes del mundo real.

-   Compruebe todas las entradas en las revisiones de código.

    Todos los parámetros de los métodos exportados y todos los datos de archivo deben comprobarse cuidadosamente para comprobar su validez y rechazarse de forma sólida si son defectuosos, con el fin de protegerse contra saturaciones y saturaciones del búfer, desbordamientos aritméticos y subdesbordes, y tipos inesperados.

-   Use técnicas de información aproximada de archivos para detectar posibles bloqueos y bloqueos.

    La información aproximada de archivos es el proceso de probar el códec con entradas permutadas aleatoriamente.

    Hay dos formas de aproximada de archivos: la aproximada no dirigida (aleatoria) y la aproximada dirigida. La información aproximada no dirigida realiza algunas volteos de bits aleatorios para ver si la entrada aleatoria puede bloquear el códec. La información aproximada dirigida permuta la entrada en función de algún conocimiento del formato de archivo. Por ejemplo, si hay una comprobación de redundancia de ciclo (CRC) en el desplazamiento de bytes 32, es probable que cambiar los bytes sin actualizar el CRC no ejecte la mayoría de las rutas de código. En este ejemplo, un fuzzer dirigido debe corregir el CRC cuando se modifican los bytes.

    Se debe crear el conjunto de entrada de imágenes para la información aproximada de archivos para que se prueba cada combinación de parámetros que admite el descodificador. Por ejemplo, si el descodificador admite archivos little- y big-endian y tres configuraciones de compresión, el conjunto de entrada de imagen debe constar de archivos little-endian de cada configuración de compresión y archivos big-endian para cada configuración de compresión. Este enfoque dará como resultado un conjunto grande pero muy sólido de imágenes de entrada que se van a probar. Incluso si ninguna cámara produce cada una de las combinaciones, pero el descodificador admite estas combinaciones teóricas, los autores de códecs deben aproximadas estas entradas.

    La seguridad se puede mejorar enormemente mediante la realización periódica de pruebas aproximadas de archivos de imagen durante el desarrollo de códecs. Los códecs siempre deben ser capaces de detectar daños en el archivo de imagen y producir errores correctamente en el caso de una solicitud con un formato correcto o de datos con formato correcto.

-   Estrese el código.

    Realice una prueba de esfuerzo del códec ejecutándose continuamente en varios procesos simultáneos, realizando todas las operaciones admitidas en todas las secuencias posibles, en imágenes de distintos tamaños (incluidas imágenes muy grandes) de todas las cámaras compatibles.

-   Seguridad para subprocesos.

    A partir Windows 7, WIC requiere que los CODECs RAW sean del tipo de apartamento COM "Both". Esto significa que debe realizar el bloqueo adecuado para controlar los autores de llamadas entre departamentos y los llamadores en escenarios multiproceso. Cualquier número de subprocesos del MTA puede llamar simultáneamente a los objetos dentro de un apartamento multiproceso (MTA), lo que permite un mejor rendimiento en sistemas de varios núcleos y determinados escenarios de servidor. Además, los CODEC de WIC que se encuentran dentro de un MTA pueden llamar a otros objetos que se encuentran dentro del MTA sin el costo de cálculo de la base de datos asociado a la llamada entre subprocesos que se encuentran en diferentes departamentos sta. En Windows 7, se han actualizado todos los CODEC DE WIC incluidos para admitir MTA, incluidos JPEG, TIFF, PNG, GIF, ICO y BMP. Los CODECs de terceros que no admiten MTA provocarán costos de rendimiento significativos en aplicaciones multiproceso debido a la serialización. La habilitación de la compatibilidad con MTA requiere que se implemente la sincronización adecuada en el códec de terceros. La implementación exacta de estas técnicas de sincronización está fuera del ámbito de este documento. A continuación se proporciona una referencia general para sincronizar objetos COM.

    https://msdn.microsoft.com/library/ms809971.aspx

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Directrices de WIC para formatos de imagen raw de cámara](-wic-rawguidelines.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



