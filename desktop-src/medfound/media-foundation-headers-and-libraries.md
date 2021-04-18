---
description: En este tema se enumeran los encabezados y las bibliotecas que definen todas las API de Media Foundation.
ms.assetid: 69877842-fafe-408f-b55b-d2ff2277c756
title: Media Foundation encabezados y bibliotecas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d5412f3f306c6e0d7327c1da1eb4c48bb109a8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105660003"
---
# <a name="media-foundation-headers-and-libraries"></a>Media Foundation encabezados y bibliotecas

En este tema se enumeran los encabezados y las bibliotecas que definen todas las API de Media Foundation.

Para buscar el encabezado y la biblioteca de un elemento específico de la API, consulte las páginas de referencia de la [referencia de programación de Media Foundation](media-foundation-programming-reference.md).

## <a name="headers"></a>Encabezados

-   codecapi. h
-   d3d11. h
-   d3d9. h
-   d3d9caps. h
-   d3d9types. h
-   DXVA. h
-   dxva2api. h
-   dxvahd. h
-   EVR. h
-   evr9. h
-   mfapi. h
-   mfcaptureengine. h
-   mferrors. h
-   mfidl. h
-   mfmediacapture. h
-   mfmediaengine. h
-   mfmp2dlna. h
-   mfobjects. h
-   mfplat. lib
-   mfplay. h
-   mfreadwrite. h
-   mftransform. h
-   opmapi. h
-   wmcodecdsp. h
-   wmcontainer. h

## <a name="libraries"></a>Bibliotecas

-   dxva2. lib
-   EVR. lib
-   MF. lib
-   mfplat. lib
-   mfplay. lib
-   mfreadwrite. lib
-   mfuuid. lib

## <a name="library-changes-in-windows-7"></a>Cambios de biblioteca en Windows 7

A partir de Windows 7, algunas funciones de Media Foundation se exportan desde distintos archivos DLL que las versiones anteriores.

Estos cambios afectan a los siguientes archivos. lib:

-   EVR. lib
-   MF. lib
-   mfplat. lib

Una aplicación que usa cualquiera de estas funciones debe vincularse a un conjunto diferente de archivos. lib, en función de la versión del SDK y la plataforma de destino.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Versión del SDK</th>
<th>Bibliotecas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows SDK para Windows Vista<br/> Windows SDK para Windows Server 2008<br/></td>
<td>EVR. lib<br/> MF. lib<br/> mfplat. lib<br/></td>
</tr>
<tr class="even">
<td>Windows SDK para Windows 7</td>
<td>Si la plataforma de destino es Windows Vista o Windows Server 2008, vincule las siguientes bibliotecas:<br/>
<ul>
<li>evr_vista. lib</li>
<li>mf_vista. lib</li>
<li>mfplat_vista. lib</li>
</ul>
Si la plataforma de destino es Windows 7 o posterior, vincule las siguientes bibliotecas:<br/>
<ul>
<li>EVR. lib</li>
<li>MF. lib</li>
<li>mfplat. lib</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="additional-info-on-helper-functions"></a>Información adicional sobre las funciones auxiliares

Windows 8 MFPlat.dll es un componente del sistema operativo Microsoft Windows. Tiene varias funciones incluidas en el módulo.

MFPlat implementa la funcionalidad auxiliar para la asignación de memoria de bajo nivel, los FIFO de programación de operaciones y las abstracciones de acceso a archivos de Win32. Para ser más específico, proporciona compatibilidad para lo siguiente:

-   asignación e inicialización de búferes de memoria (conocidos como ' ejemplos ') y aplicaciones auxiliares para simplificar la administración de sus duraciones
-   funciones eficientes de copia de datos para los búferes de memoria
-   asignación e inicialización de FIFO de operación (conocido como "eventos")
-   implementar un objeto Clock simple
-   implementar un contenedor de archivos Win32
-   asignación e inicialización de matrices de búferes de memoria para CPU y GPU

Si el método [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) se ejecuta correctamente, MFPlat proporciona la siguiente funcionalidad de cola de trabajo:

-   compatibilidad interna de elementos de e/s (tal y como se usa en las bibliotecas de sockets y contenedores de archivos de Win32)
-   proporcionar una matriz de colas de trabajos multiproceso con compatibilidad con la prioridad de subprocesos
-   compatibilidad de elementos de trabajo, elementos de temporizador y elementos de espera a través de las colas de trabajos

MFPlat proporciona funcionalidad auxiliar para buscar y crear transformaciones multimedia y orígenes multimedia registrados en el sistema y crear y manipular tipos de medios, aunque el propio MFPlat no puede crear el medio real ni reproducirlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 




