---
description: Disponibilidad de códecs y compatibilidad con plataformas
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: Disponibilidad de códecs y compatibilidad con plataformas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5768cdbe149e87188bdd9d21f87508991feb841a70acacf5984ada408f5b58fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032329"
---
# <a name="codec-availability-and-platform-support"></a>Disponibilidad de códecs y compatibilidad con plataformas

Microsoft recomienda que los proveedores de cámaras incluyan códecs raw Windows Imaging Component (WIC) actualizados en la distribución de software con nuevas cámaras y que el códec actualizado se instale con la instalación de software del proveedor predeterminada Windows 7, Windows Vista y Windows XP. Los proveedores de cámaras también deben proporcionar el códec WIC más reciente como descarga desde sus sitios de soporte técnico.

## <a name="codec-discovery"></a>Detección de códecs

Microsoft hace lo siguiente para ayudar a los usuarios a los sitios web de los proveedores para las descargas de códecs:

-   En el Explorador de Windows, si un usuario hace doble clic en un archivo que no se reconoce (el caso predeterminado cuando un archivo RAW está en el equipo, pero el códec aún no está instalado), un cuadro de diálogo informa de que el archivo no se reconoce y pregunta si el usuario quiere encontrar un programa que comprenda el archivo. Microsoft mantiene un servicio de redireccionamiento existente para reenviar a los usuarios a los sitios web de los proveedores que pueden proporcionar el programa para comprender el archivo. Esta instalación existe en Windows XP y en Windows Vista.
-   El Windows Galería de fotos, Galería fotográfica de Windows Live y el Windows Visualizador de fotos 7 reconocen un conjunto de extensiones de archivo como archivos RAW. Si los archivos de ese conjunto se encuentran en carpetas que están observando cualquiera de estas aplicaciones y un códec para el archivo aún no está instalado, aparece un cuadro de diálogo, como se describe en el párrafo anterior.

Para obtener más información sobre la detección de códecs, vea Disponibilidad de códecs y Compatibilidad con plataformas.

## <a name="windows-xp-platform-support"></a>Windows Compatibilidad con la plataforma XP

Microsoft ha publicado Windows XP SP3 con WIC y un instalador de WIC independiente para Windows XP SP2. Estos usan códecs WIC para habilitar la compatibilidad con miniaturas y vistas previas en esas plataformas. Por lo tanto, es importante que la descarga e instalación de códecs se puedan y probar en Windows 7, Windows Vista y Windows XP.

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

 

 



