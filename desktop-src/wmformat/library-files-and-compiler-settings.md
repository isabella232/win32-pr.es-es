---
title: Archivos de biblioteca y archivos del compilador Configuración
description: Archivos de biblioteca y archivos del compilador Configuración
ms.assetid: ae043b1e-1d61-4d5a-be98-54f899fa24ed
keywords:
- Windows SDK de formato multimedia, archivos de biblioteca
- Windows SDK de formato multimedia, configuración del compilador
- Windows SDK de formato multimedia, archivos de encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176f6c7acb9516e8c7ac38a067091bcbb0c8f7cf49cfdb9e65b396768158b233
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930665"
---
# <a name="library-files-and-compiler-settings"></a>Archivos de biblioteca y archivos del compilador Configuración

Para desarrollar una aplicación mediante el SDK Windows Media Format, debe usar Microsoft Visual C++ versión 6.0 o posterior. Los únicos lenguajes de programación adecuados para el desarrollo son C++ y C.

El contenido de los distintos archivos de encabezado incluidos con este SDK se describe en la tabla siguiente.



| Archivo de encabezado                 | Descripción                                                                                                                                                                                                                                         |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| asferr.h                    | Define códigos de error relacionados con las operaciones de archivo ASF. Este encabezado se incluye en wmsdk.h.                                                                                                                                                            |
| drternals.h              | Define estructuras, enumeraciones y constantes que se usan para la administración de derechos digitales (DRM). Incluya este encabezado al escribir una aplicación que use DRM.                                                                                            |
| dshowasf.h                  | Define los filtros DirectShow QASF de Microsoft. Incluya este encabezado al escribir una aplicación DirectShow que crea o lee archivos ASF. Para obtener más información, [vea DirectShow y Windows Media](directshow-and-windows-media.md).               |
| msnetobj.h                  | Define la [**interfaz IRMGetLicense,**](irmgetlicense.md) que se implementa en una de las bibliotecas en tiempo de ejecución instaladas con el SDK Windows Media Format.                                                                                     |
| nserror.h                   | Define códigos de error para Windows Media Technologies. Solo un subconjunto de estos códigos de error son relevantes para el SDK Windows Media Format. Este encabezado se incluye en wmsdk.h.                                                                            |
| wmdxva.h                    | Incluye otros encabezados y definiciones necesarios para habilitar la aceleración de vídeo de Microsoft DirectX para la reproducción Windows contenido basado en multimedia. Para más información, consulte [Habilitación de la aceleración de vídeo de DirectX.](enabling-directx-video-acceleration.md) |
| wmnetsourcecreator.h        | Contiene la información necesaria para crear complementos de origen de red.                                                                                                                                                                                      |
| wmsbuffer.h                 | Define las interfaces utilizadas por los objetos de búfer. Incluya este encabezado al crear sus propios búferes para la lectura de archivos.                                                                                                                                 |
| wmsdk.h                     | Encabezado principal de las aplicaciones que usan el SDK Windows Media Format. Este encabezado no contiene definiciones, pero incluye asferr.h, nserror.h, windows.h y wmsdkidl.h. Incluya este encabezado para todas las aplicaciones que usan este SDK.                     |
| wmsdkidl.h                  | Define las interfaces, funciones, estructuras, enumeraciones y constantes para la mayoría de los objetos del SDK Windows Media Format. Este encabezado se incluye en wmsdk.h.                                                                             |
| wmsinternaladminnetsource.h | Define las interfaces de los complementos de origen de red.                                                                                                                                                                                                  |
| wmsysprf.h                  | Define las constantes para los perfiles del sistema. Incluya este encabezado en las aplicaciones que cargan perfiles del sistema por identificador.                                                                                                                         |



 

Para usar Windows SDK de formato multimedia, el compilador debe estar configurado correctamente. La configuración es diferente para compilar en modo de depuración que para el modo de versión. Configure la configuración según la tabla siguiente. Todas estas opciones se configuran en el cuadro Project Configuración de diálogo. Para llegar al cuadro de diálogo, **seleccione Configuración** en el **Project** de texto.



| Configuración                                                                 | Valor de depuración                                                                              | Valor de versión                                                                           |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (pestaña C/C++, Categoría = Generación de código) Uso de la biblioteca en tiempo de ejecución            | Depurar dll multiproceso                                                                  | DLL multiproceso                                                                       |
| (Pestaña Vínculo, Categoría = General) Omitir todas las bibliotecas predeterminadas (casilla) | Seleccionado                                                                                 | Seleccionado                                                                                |
| (Pestaña Vínculo, Categoría = General) Módulos de objeto o biblioteca                   | Incluya Msvcrtd.lib y Wmvcore.lib.Do no incluya Libc.lib ni ninguna variación.<br/> | Incluya Msvcrt.lib y Wmvcore.lib.Do no incluya Libc.lib ni ninguna variación.<br/> |



 

Si usa .NET Microsoft Visual Studio, la configuración se ha cambiado a ubicaciones diferentes, como se muestra en la tabla siguiente. Todas estas opciones se configuran en el cuadro **de diálogo Páginas de** propiedades . Para llegar al cuadro de diálogo, haga clic con el botón derecho en el proyecto en el **panel** Explorador de soluciones y seleccione **Propiedades** en el menú contextual.



| Configuración                                                                  | Valor de depuración                                                                              | Valor de versión                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Propiedades de configuración/ C/C++ / Generación de código) Biblioteca en tiempo de ejecución     | DLL de depuración multiproceso (/MDd)                                                          | DLL multiproceso (/MD)                                                                |
| (Propiedades de configuración/Vinculador/Entrada) Dependencias adicionales      | Incluya Msvcrtd.lib y Wmvcore.lib.Do no incluya Libc.lib ni ninguna variación.<br/> | Incluya Msvcrt.lib y Wmvcore.lib.Do no incluya Libc.lib ni ninguna variación.<br/> |
| (Propiedades de configuración/Vinculador/Entrada) Omitir todas las bibliotecas predeterminadas | Sí                                                                                      | Sí                                                                                     |



 

Si desea retrasar la carga de Wmvcore.dll o cualquier otro archivo DLL, use la opción de vínculo /DELAYLOAD en Microsoft Visual C++ 6.0 o archivos DLL de carga retrasada en Microsoft Visual C++ .NET.

Además, debe incluir los directorios de las bibliotecas y encabezados del SDK Windows Media Format. Para buscar la configuración del directorio Visual C++ 6.0, en el menú Herramientas, haga clic en Opciones y, a continuación, haga clic en **la pestaña** Directorios.  Al usar Visual C++ .NET,  haga clic  en Opciones en el menú Herramientas y, a continuación, seleccione Proyectos o VC++ directorios en la lista de opciones. Agregue directorios como se muestra en la tabla siguiente. Si ha cambiado el directorio de instalación del SDK Windows Media Format, la ruta de acceso será diferente.



| Tipo de directorio | Ruta de acceso predeterminada                 |
|----------------|------------------------------|
| Archivos de inclusión  | C: \\ WMSDK \\ WMFSDK11 \\ include |
| Archivos de biblioteca  | C: \\ biblioteca WMSDK \\ WMFSDK11 \\     |



 

Si usa el SDK de plataforma, las rutas de acceso predeterminadas aparecerán de la siguiente manera:



| Tipo de directorio | Ruta de acceso predeterminada                                              |
|----------------|-----------------------------------------------------------|
| Archivos de inclusión  | C: \\ Archivos de programa Microsoft \\ SDsK \\ Windows \\ v6.0 \\ Include |
| Archivos de biblioteca  | C: \\ Archivos de programa Microsoft \\ SDsK \\ Windows biblioteca \\ v6.0 \\     |



 

Antes de llamar a cualquiera de las funciones de creación, COM debe inicializarse con una llamada a **Coinitialize** o **CoinitializeEx**. Se puede usar el modelo de subprocesamiento libre o el modelo de subprocesamiento de apartamento, pero el modelo de subprocesamiento de apartamento impone restricciones de subprocesamiento en la aplicación. Para obtener más información sobre El modelo de objetos componentes (COM) de Microsoft, vea la página COM en el [sitio web de Microsoft](../com/the-component-object-model.md).

**Nota** Las aplicaciones que reproducen o crean archivos protegidos por Digital Rights Management (DRM) requieren una biblioteca estática individualizada que se debe obtener por separado de Microsoft. Para obtener más información, vea el Windows de licencias multimedia en el sitio [web de Microsoft](https://www.microsoft.com/licensing/default). Si usa la biblioteca DRM, no debe vincular a Wmvcore.lib.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas iniciales**](getting-started.md)
</dt> </dl>

 

