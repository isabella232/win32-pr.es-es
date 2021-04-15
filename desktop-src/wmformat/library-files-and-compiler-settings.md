---
title: Archivos de biblioteca y configuración del compilador
description: Archivos de biblioteca y configuración del compilador
ms.assetid: ae043b1e-1d61-4d5a-be98-54f899fa24ed
keywords:
- SDK de Windows Media Format, archivos de biblioteca
- SDK de Windows Media Format, configuración del compilador
- Windows Media Format SDK, archivos de encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 079636c8f01decdcfb90e36641e26c62354a7893
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104488452"
---
# <a name="library-files-and-compiler-settings"></a>Archivos de biblioteca y configuración del compilador

Para desarrollar una aplicación con el SDK de Windows Media Format, debe usar Microsoft Visual C++ versión 6,0 o posterior. Los únicos lenguajes de programación adecuados para el desarrollo son C++ y C.

El contenido de los diversos archivos de encabezado incluidos con este SDK se describe en la tabla siguiente.



| Archivo de encabezado                 | Descripción                                                                                                                                                                                                                                         |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| asferr. h                    | Define los códigos de error relacionados con las operaciones de archivo ASF. Este encabezado está incluido en wmsdk. h.                                                                                                                                                            |
| drmexternals. h              | Define las estructuras, las enumeraciones y las constantes que se usan para la administración de derechos digitales (DRM). Incluya este encabezado al escribir una aplicación que use DRM.                                                                                            |
| dshowasf. h                  | Define los filtros de QASF de Microsoft DirectShow. Incluya este encabezado al escribir una aplicación de DirectShow que cree o lea archivos ASF. Para obtener más información, consulte [DirectShow y Windows Media](directshow-and-windows-media.md).               |
| msnetobj. h                  | Define la interfaz [**IRMGetLicense**](irmgetlicense.md) , que se implementa en una de las bibliotecas en tiempo de ejecución instaladas con el SDK de Windows Media Format.                                                                                     |
| NSError. h                   | Define los códigos de error para las tecnologías de Windows Media. Solo un subconjunto de estos códigos de error es relevante para el SDK de Windows Media Format. Este encabezado está incluido en wmsdk. h.                                                                            |
| wmdxva. h                    | Incluye otros encabezados y definiciones necesarios para habilitar la aceleración de vídeo de Microsoft DirectX para la reproducción de contenido basado en Windows Media. Para obtener más información, consulte [Habilitar la aceleración de vídeo de DirectX](enabling-directx-video-acceleration.md). |
| wmnetsourcecreator. h        | Contiene la información necesaria para crear complementos de origen de red.                                                                                                                                                                                      |
| wmsbuffer. h                 | Define las interfaces utilizadas por los objetos de búfer. Incluya este encabezado al crear sus propios búferes para la lectura de archivos.                                                                                                                                 |
| wmsdk. h                     | Encabezado principal de las aplicaciones que usan el SDK de Windows Media Format. Este encabezado no contiene definiciones, pero incluye asferr. h, NSError. h, Windows. h y wmsdkidl. h. Incluya este encabezado para todas las aplicaciones que usan este SDK.                     |
| wmsdkidl. h                  | Define las interfaces, funciones, estructuras, enumeraciones y constantes para la mayoría de los objetos del SDK de formato de Windows Media. Este encabezado está incluido en wmsdk. h.                                                                             |
| wmsinternaladminnetsource. h | Define las interfaces de los complementos de origen de red.                                                                                                                                                                                                  |
| wmsysprf. h                  | Define las constantes para los perfiles del sistema. Incluya este encabezado en aplicaciones que carguen perfiles del sistema por identificador.                                                                                                                         |



 

Para usar el SDK de Windows Media Format, el compilador debe estar configurado correctamente. La configuración es diferente para compilar en modo de depuración que para el modo de versión. Configure el valor de acuerdo con la tabla siguiente. Todos estos valores se configuran en el cuadro de diálogo Configuración del proyecto. Para llegar al cuadro de diálogo, seleccione **configuración** en el menú **proyecto** .



| Configuración                                                                 | Valor de depuración                                                                              | Valor de versión                                                                           |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Pestaña C/C++, categoría = generación de código) Usar la biblioteca en tiempo de ejecución            | Depurar DLL Multiproceso                                                                  | DLL Multiproceso                                                                       |
| (Pestaña vínculo, categoría = general) Omitir todas las bibliotecas predeterminadas (casilla) | Seleccionado                                                                                 | Seleccionado                                                                                |
| (Pestaña vínculo, categoría = general) Módulos de objeto/biblioteca                   | Incluya msvcrtd. lib y Wmvcore.lib.Do no incluya libc. lib o cualquier variación.<br/> | Incluye msvcrt. lib y Wmvcore.lib.Do no incluyen libc. lib o cualquier variación.<br/> |



 

Si usa Microsoft Visual Studio .NET, la configuración se ha cambiado a ubicaciones diferentes, como se muestra en la tabla siguiente. Todas estas opciones se configuran en el cuadro de diálogo **páginas de propiedades** . Para llegar al cuadro de diálogo, haga clic con el botón derecho en el proyecto en el panel de **Explorador de soluciones** y seleccione **propiedades** en el menú contextual.



| Configuración                                                                  | Valor de depuración                                                                              | Valor de versión                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Propiedades de configuración/C/C++/generación de código) Biblioteca en tiempo de ejecución     | DLL de depuración multiproceso (/MDd)                                                          | DLL multiproceso (/MD)                                                                |
| (Propiedades de configuración/vinculador/entrada) Dependencias adicionales      | Incluya msvcrtd. lib y Wmvcore.lib.Do no incluya libc. lib o cualquier variación.<br/> | Incluye msvcrt. lib y Wmvcore.lib.Do no incluyen libc. lib o cualquier variación.<br/> |
| (Propiedades de configuración/vinculador/entrada) Omitir todas las bibliotecas predeterminadas | Sí                                                                                      | Sí                                                                                     |



 

Si desea retrasar la carga de Wmvcore.dll o cualquier otro archivo DLL, use la opción de vínculo/DELAYLOAD en Microsoft Visual C++ 6,0 o retrasar las DLL cargadas en Microsoft Visual C++ .NET.

Además, debe incluir los directorios de las bibliotecas y los encabezados del SDK de Windows Media Format. Para buscar la configuración del directorio para Visual C++ 6,0, en el menú **herramientas** , haga clic en **Opciones** y, a continuación, haga clic en la pestaña **directorios** . Cuando use Visual C++ .NET, haga clic en **Opciones** en el menú **herramientas** y, a continuación, seleccione proyectos/directorios de VC + + en la lista de opciones. Agregue directorios como se muestra en la tabla siguiente. Si ha cambiado el directorio de instalación del SDK de Windows Media Format, la ruta de acceso será diferente.



| Tipo de directorio | Ruta de acceso predeterminada                 |
|----------------|------------------------------|
| Archivos de inclusión  | C: \\ WMSDK \\ WMFSDK11 \\ include |
| Archivos de biblioteca  | C: \\ WMSDK \\ WMFSDK11 \\ lib     |



 

Si usa el SDK de la plataforma, las rutas de acceso predeterminadas aparecerán de la siguiente manera:



| Tipo de directorio | Ruta de acceso predeterminada                                              |
|----------------|-----------------------------------------------------------|
| Archivos de inclusión  | C: \\ archivos de programa \\ Microsoft SDsK \\ Windows \\ v 6.0 \\ include |
| Archivos de biblioteca  | C: \\ archivos de programa \\ Microsoft SDsK \\ Windows \\ v 6.0 \\ lib     |



 

Antes de llamar a cualquiera de las funciones de creación, COM debe inicializarse con una llamada a **CoInitialize** o **CoinitializeEx**. Se puede usar el modelo de subprocesamiento libre o el modelo de subprocesos de apartamento, pero el modelo de subprocesos de Apartamento impone restricciones de subprocesos en la aplicación. Para obtener más información sobre el modelo de objetos componentes (COM) de Microsoft, vea la página COM en el [sitio web de Microsoft](../com/the-component-object-model.md).

**Nota:** Las aplicaciones que reproducen o crean archivos protegidos por Rights Management digital (DRM) requieren una biblioteca estática individualizada que se debe obtener por separado de Microsoft. Para obtener más información, vea el formulario de licencias de Windows Media en el [sitio web de Microsoft](https://www.microsoft.com/licensing/default). Si usa la biblioteca DRM, no debe vincular a wmvcore. lib.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción**](getting-started.md)
</dt> </dl>

 

