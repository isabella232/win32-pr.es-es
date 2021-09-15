---
description: En este tema se enumeran los encabezados y bibliotecas que definen todas las MEDIA FOUNDATION API.
ms.assetid: 69877842-fafe-408f-b55b-d2ff2277c756
title: Media Foundation encabezados y bibliotecas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6db7650c98f6491fa6db4010273475b4bd103a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468737"
---
# <a name="media-foundation-headers-and-libraries"></a>Media Foundation encabezados y bibliotecas

En este tema se enumeran los encabezados y bibliotecas que definen todas las MEDIA FOUNDATION API.

Para buscar el encabezado y la biblioteca de un elemento de API específico, consulte las páginas de referencia de Media Foundation [Programming Reference](media-foundation-programming-reference.md).

## <a name="headers"></a>encabezados

-   codecapi.h
-   d3d11.h
-   d3d9.h
-   d3d9caps.h
-   d3d9types.h
-   dxva.h
-   dxva2api.h
-   dxvahd.h
-   evr.h
-   evr9.h
-   mfapi.h
-   mfcaptureengine.h
-   mferrors.h
-   mfidl.h
-   mfmediacapture.h
-   mfmediaengine.h
-   mfmp2dlna.h
-   mfobjects.h
-   mfplat.lib
-   mfplay.h
-   mfreadwrite.h
-   mftransform.h
-   opmapi.h
-   wmcodecdsp.h
-   wmcontainer.h

## <a name="libraries"></a>Bibliotecas

-   dxva2.lib
-   evr.lib
-   mf.lib
-   mfplat.lib
-   mfplay.lib
-   mfreadwrite.lib
-   mfuuid.lib

## <a name="library-changes-in-windows-7"></a>Cambios de biblioteca en Windows 7

A partir de Windows 7, ciertas funciones Media Foundation se exportan desde archivos DLL diferentes a las versiones anteriores.

Estos cambios afectan a los siguientes archivos .lib:

-   evr.lib
-   mf.lib
-   mfplat.lib

Una aplicación que use cualquiera de estas funciones debe vincularse a un conjunto diferente de archivos .lib, según la versión del SDK y la plataforma de destino.




| Versión del SDK | Bibliotecas | 
|-------------|-----------|
| Windows SDK para Windows Vista<br /> Windows SDK para Windows Server 2008<br /> | evr.lib<br /> mf.lib<br /> mfplat.lib<br /> | 
| Windows SDK para Windows 7 | Si la plataforma de destino Windows Vista o Windows Server 2008, vincule las bibliotecas siguientes:<br /><ul><li>evr_vista.lib</li><li>mf_vista.lib</li><li>mfplat_vista.lib</li></ul>Si la plataforma de destino Windows 7 o posterior, vincule las siguientes bibliotecas:<br /><ul><li>evr.lib</li><li>mf.lib</li><li>mfplat.lib</li></ul> | 




 

## <a name="additional-info-on-helper-functions"></a>Información adicional sobre las funciones auxiliares

El Windows 8 MFPlat.dll es un componente del sistema operativo microsoft Windows. Tiene varias funciones incluidas en el módulo.

MFPlat implementa la funcionalidad auxiliar para la asignación de memoria de bajo nivel, la programación de operaciones FIFOs y abstracciones de acceso a archivos win32. Para ser más específico, proporciona compatibilidad con lo siguiente:

-   asignar e inicializar búferes de memoria (conocidos como "ejemplos") y asistentes para simplificar la administración de su duración
-   funciones eficaces de copia de datos para búferes de memoria
-   asignar e inicializar operaciones FIFO (conocidas como "eventos").
-   implementar un objeto de reloj simple
-   implementar un contenedor de archivos win32
-   asignar e inicializar matrices de búferes de memoria para CPU y GPU

Si el [**método MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) se realiza correctamente, MFPlat proporciona la siguiente funcionalidad de cola de trabajo:

-   admitir internamente elementos de E/S (tal y como lo usan el contenedor de archivos win32 y las bibliotecas de sockets)
-   proporcionar una matriz de colas de trabajo multiproceso con compatibilidad con prioridad de subproceso
-   admitir elementos de trabajo, elementos de temporizador y elementos de espera a través de las colas de trabajo

MFPlat proporciona funcionalidad auxiliar para buscar y crear transformaciones de medios y orígenes multimedia registrados en el sistema, y para crear y manipular tipos de medios, aunque MFPlat no puede crear el medio real ni reproducirlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 




