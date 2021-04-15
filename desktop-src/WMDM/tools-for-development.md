---
title: Herramientas para desarrollo
description: Herramientas para desarrollo
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Media Administrador de dispositivos, herramientas de desarrollo
- Administrador de dispositivos, herramientas de desarrollo
- Windows Media Administrador de dispositivos, certificados
- Administrador de dispositivos, certificados
- Administrador de dispositivos de Windows Media, claves
- Administrador de dispositivos, claves
- Windows Media Administrador de dispositivos, bibliotecas
- Administrador de dispositivos, bibliotecas
- Windows Media Administrador de dispositivos, kit de desarrollo de software (SDK)
- Administrador de dispositivos, kit de desarrollo de software (SDK)
- SDK de Administrador de dispositivos de Windows Media
- SDK de Administrador de dispositivos
- SDK de Media Player de Windows
- SDK de Windows Media Format
- SDK de Windows Media Rights Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45a3e419b87c56a447ad2412234a80432b1598e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "105695794"
---
# <a name="tools-for-development"></a>Herramientas para desarrollo

En esta sección se describen los distintos certificados y claves, bibliotecas y SDK que se deben programar con el SDK de Windows Media Administrador de dispositivos.

Certificados y claves

El SDK de Windows Media Administrador de dispositivos incluye un par de claves/certificados de prueba (en el archivo Key. c) que puede usar una aplicación o un proveedor de servicios para usar los métodos de Administrador de dispositivos de Windows Media en contenido no protegido. Este par de clave y certificado permite que la aplicación o el proveedor de servicios usen la mayor parte de la funcionalidad de Windows Media Administrador de dispositivos.

Sin embargo, para desarrollar una aplicación o un proveedor de servicios que pueda controlar contenido protegido con DRM, debe solicitar uno o más certificados (cada uno con una clave) de la [Página de licencias de Windows Media](https://www.microsoft.com/licensing/default). Los certificados son necesarios para las siguientes aplicaciones u objetos:

-   Los proveedores de servicios que controlan contenido protegido con DRM requieren un certificado (y una clave) de proveedor de servicios de Windows Media Administrador de dispositivos.
-   Las aplicaciones que transfieren contenido protegido con DRM requieren un certificado (y una clave) de Windows Media Administrador de dispositivos Transfer
-   Las aplicaciones que reproducen contenido protegido con DRM requieren un certificado DRM (y una clave).
-   Los componentes de medición de licencias requieren un certificado de medición. Lo proporciona un servicio de medición de licencias basado en el SDK de Windows Media Rights Manager, que se puede solicitar en la página de administración de licencias de Windows Media.

Encabezados y bibliotecas

Además de las bibliotecas y los encabezados que se mencionan en [los archivos de encabezado y biblioteca necesarios para una aplicación](required-library-and-header-files-for-an-application.md) o las [bibliotecas y encabezados necesarios para un proveedor de servicios](required-libraries-and-headers-for-a-service-provider.md), cualquier aplicación o complemento que anteriormente se vinculó a WMDRMSDK. lib para llamar a las funciones del SDK de Windows Media Format debe estar vinculado ahora a WMDRMSDKStub. lib. Este archivo de biblioteca se usa para tener acceso a archivos protegidos con DRM. También puede solicitar esta biblioteca desde la página de licencias de Windows Media.

SDK relacionados

Los siguientes SDK de Microsoft proporcionan elementos que puede necesitar para diseñar soluciones para dispositivos multimedia portátiles.



| Se requiere SDK                     | Requerido para...                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SDK de Administrador de dispositivos de Windows Media | Aplicaciones del reproductor multimedia de escritorio que se comunican con dispositivos portátiles<br/> Aplicaciones de escritorio que pueden intercambiar archivos o información con dispositivos portátiles<br/> Windows Media Player medición de objetos COM<br/> |
| SDK de Media Player de Windows         | Complementos de Media Player de Windows<br/> Windows Media Player medición de objetos COM<br/> Máscaras de Windows Media Player<br/>                                                                                                   |
| SDK de Windows Media Format         | Reproductores de audio o vídeo que pueden crear o reproducir archivos (especialmente archivos ASF)<br/> Aplicaciones de edición de audio o vídeo<br/>                                                                                               |
| SDK de Windows Media Rights Manager | Las aplicaciones o los complementos que se reproducen en el equipo de escritorio o dispositivo.                                                                                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción**](getting-started.md)
</dt> </dl>

 

 





