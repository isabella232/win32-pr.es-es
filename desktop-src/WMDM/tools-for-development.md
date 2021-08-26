---
title: Herramientas para el desarrollo
description: Herramientas para el desarrollo
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Herramientas de Administrador de dispositivos,herramientas de desarrollo
- Administrador de dispositivos,herramientas de desarrollo
- Windows Media Administrador de dispositivos,certificates
- Administrador de dispositivos,certificates
- Windows Claves Administrador de dispositivos multimedia
- Administrador de dispositivos,keys
- Windows Archivos Administrador de dispositivos,bibliotecas
- Administrador de dispositivos,libraries
- Windows Media Administrador de dispositivos,software development kit (SDK)
- Administrador de dispositivos,software development kit (SDK)
- Windows SDK de Administrador de dispositivos multimedia
- ADMINISTRADOR DE DISPOSITIVOS SDK
- Reproductor de Windows Media Sdk
- Windows SDK de formato multimedia
- Windows Media Rights Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e517a97246c2bf9b2ac5670a7cf696e714777a2f5926a37e1b2d37ecbe45c9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031615"
---
# <a name="tools-for-development"></a>Herramientas para el desarrollo

En esta sección se describen los distintos certificados y claves, bibliotecas y SDK que necesitará programar mediante el SDK de Windows Media Administrador de dispositivos.

Certificados y claves

El SDK de Windows Media Administrador de dispositivos se distribuye con un par de claves y certificados de prueba (en el archivo key.c) que puede usar una aplicación o un proveedor de servicios para usar métodos de Windows Media Administrador de dispositivos en contenido no protegido. Este par clave-certificado permite que la aplicación o el proveedor de servicios usen la mayor parte de Windows funcionalidad de Administrador de dispositivos multimedia.

Sin embargo, para desarrollar una aplicación o un proveedor de servicios que pueda administrar contenido protegido con DRM, debe solicitar uno o varios certificados (cada uno con una clave) de la página de licencias multimedia de [Windows](https://www.microsoft.com/licensing/default). Los certificados son necesarios para las siguientes aplicaciones u objetos:

-   Los proveedores de servicios que controlan el contenido protegido con DRM requieren un certificado Windows media Administrador de dispositivos service provider (y una clave)
-   Las aplicaciones que transfieren contenido protegido con DRM requieren un certificado Windows multimedia Administrador de dispositivos de transferencia (y clave)
-   Las aplicaciones que reproducen contenido protegido con DRM requieren un certificado DRM (y una clave).
-   Los componentes de medición de licencias requieren un certificado de medición. Esto lo proporciona un servicio de medición de licencias basado en el SDK de Windows Media Rights Manager, que se puede solicitar en la Windows licencias multimedia.

Encabezados y bibliotecas

Además de las bibliotecas y [](required-library-and-header-files-for-an-application.md) los encabezados mencionados en Biblioteca requerida y Archivos de encabezado para una aplicación o Bibliotecas y [encabezados](required-libraries-and-headers-for-a-service-provider.md)necesarios para un proveedor de servicios , cualquier aplicación o complemento que anteriormente vinculara a WMDRMSDK.lib para llamar a las funciones del SDK de formato multimedia de Windows ahora debería vincularse ahora a WMDRMSDKStub.Lib. Este archivo de biblioteca se usa para acceder a archivos protegidos con DRM. También puede solicitar esta biblioteca desde la página Windows licencias multimedia.

SDK relacionados

Los siguientes SDK de Microsoft proporcionan elementos que puede necesitar para diseñar soluciones para dispositivos multimedia portátiles.



| SDK requerido                     | Necesario para...                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows SDK de Administrador de dispositivos multimedia | Aplicaciones de reproductor multimedia de escritorio que se comunican con dispositivos portátiles<br/> Aplicaciones de escritorio que pueden intercambiar archivos o información con dispositivos portátiles<br/> Reproductor de Windows Media objetos COM de medición<br/> |
| Reproductor de Windows Media Sdk         | Reproductor de Windows Media complementos<br/> Reproductor de Windows Media objetos COM de medición<br/> Reproductor de Windows Media máscaras<br/>                                                                                                   |
| Windows SDK de formato multimedia         | Reproductores de audio o vídeo que pueden crear o reproducir archivos (especialmente archivos ASF)<br/> Aplicaciones de edición de audio o vídeo<br/>                                                                                               |
| Windows Media Rights Manager SDK | Las aplicaciones o complementos que mida la reproducción cuentan en el escritorio o el dispositivo.                                                                                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas iniciales**](getting-started.md)
</dt> </dl>

 

 





