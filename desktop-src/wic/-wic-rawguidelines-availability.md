---
description: Compatibilidad de plataforma y disponibilidad de códecs
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: Compatibilidad de plataforma y disponibilidad de códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc485c5f8db9ff7883263cd614578705eccd3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278181"
---
# <a name="codec-availability-and-platform-support"></a>Compatibilidad de plataforma y disponibilidad de códecs

Microsoft recomienda que los proveedores de cámaras incluyan códecs de componentes de imágenes de Windows (WIC) sin procesar actualizados en la distribución de software con nuevas cámaras y que el códec actualizado se instale con la instalación de software de proveedor predeterminada Windows 7, Windows Vista y Windows XP. Los proveedores de cámaras también deben proporcionar el códec WIC más reciente como descarga de sus sitios de soporte técnico.

## <a name="codec-discovery"></a>Detección de códecs

Microsoft está haciendo lo siguiente para ayudar a los usuarios a dirigirse a los sitios web de los proveedores para descargar códecs:

-   En el explorador de Windows, si un usuario hace doble clic en un archivo que no se reconoce (el caso predeterminado en el que un archivo sin formato está en el equipo, pero el códec todavía no está instalado), un cuadro de diálogo informa de que el archivo no se reconoce y pregunta si el usuario desea encontrar un programa que entienda el archivo. Microsoft mantiene un servicio de redireccionamiento existente para reenviar a los usuarios a sitios web de los proveedores que pueden proporcionar el programa para comprender el archivo. Esta instalación existe en Windows XP y en Windows Vista.
-   La Galería fotográfica de Windows, la Galería fotográfica de Windows Live y el visor de fotografías de Windows 7 reconocen un conjunto de extensiones de archivo como archivos sin formato. Si los archivos de ese conjunto se encuentran en carpetas que cualquiera de estas aplicaciones están examinando y no hay instalado un códec para el archivo, se mostrará un cuadro de diálogo, tal como se describe en el párrafo anterior.

Para obtener más información acerca de la detección de códecs, consulte compatibilidad con códecs y plataforma.

## <a name="windows-xp-platform-support"></a>Compatibilidad con la plataforma Windows XP

Microsoft ha lanzado Windows XP SP3 con WIC y un instalador de WIC independiente para Windows XP SP2. Estos usan códecs WIC para habilitar la compatibilidad con miniaturas y vistas previas en esas plataformas. Por lo tanto, es importante que la descarga e instalación de códecs se admita y pruebe en Windows 7, Windows Vista y Windows XP.

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

 

 



