---
description: La creación del códec en la plataforma Windows Imaging Component (WIC) permite que todas las aplicaciones creadas en WIC obtengan la misma compatibilidad de plataforma para el formato de imagen que obtienen para los formatos de imagen comunes incluidos con la plataforma.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Conclusión (Cómo escribir un códec WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de165f20ff81094c3b64d7e9667795f0bf80cef8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575628"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a>Conclusión (Cómo escribir un códec WIC-Enabled)

La creación del códec en la plataforma Windows Imaging Component (WIC) permite que todas las aplicaciones creadas en WIC obtengan la misma compatibilidad de plataforma para el formato de imagen que obtienen para los formatos de imagen comunes incluidos con la plataforma. También permite que Windows Vista Galería de fotos, Windows Explorer y Visualizador de fotos muestren miniaturas y vistas previas de imágenes en su formato mediante el descodificador que proporcione. En el caso de los formatos sin procesar, permite que las aplicaciones de creación de imágenes más sofisticadas aprovechen las funcionalidades de procesamiento sin procesar del descodificador. En función de las opciones de codificador que admita, también puede exponer funcionalidades únicas del codificador para permitir que las aplicaciones aprovechen al máximo las características avanzadas del formato de imagen.

El desarrollo de un códec habilitado para WIC requiere que implemente algunas interfaces nuevas. En muchos casos, puede escribir un contenedor para el códec existente que implemente estas interfaces. Al instalar el códec, debe crear algunas entradas del Registro para que la plataforma WIC lo detecte y asociarlo a los controladores de metadatos adecuados. También debe invocar una API para borrar la caché de miniaturas de las miniaturas predeterminadas (vacías) que se puedan haber asociado previamente a imágenes en su formato. Si lo desea, puede habilitar Windows Vista Galería de fotos para proporcionar a los usuarios un vínculo para descargar el códec cuando el Galería de fotos encuentra una imagen con la extensión de nombre de archivo. Para ello, debe proporcionar a Microsoft información sobre la extensión de nombre de archivo del códec y la dirección URL del sitio de descarga.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Instalación y registro de CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



