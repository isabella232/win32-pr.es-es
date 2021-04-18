---
description: La compilación del códec en la plataforma de Windows Imaging Component (WIC) permite a todas las aplicaciones compiladas en WIC obtener la misma compatibilidad de plataforma para el formato de imagen que obtienen para los formatos de imagen comunes que se incluyen con la plataforma.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Conclusión (cómo escribir un códec WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de165f20ff81094c3b64d7e9667795f0bf80cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720554"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a>Conclusión (cómo escribir un códec WIC-Enabled)

La compilación del códec en la plataforma de Windows Imaging Component (WIC) permite a todas las aplicaciones compiladas en WIC obtener la misma compatibilidad de plataforma para el formato de imagen que obtienen para los formatos de imagen comunes que se incluyen con la plataforma. También permite que la Galería fotográfica de Windows Vista, el explorador de Windows y el visor fotográfico muestren miniaturas y vistas previas de imágenes en el formato mediante el descodificador que proporcione. En el caso de los formatos sin procesar, permite que las aplicaciones de imágenes más sofisticadas aprovechen las capacidades de procesamiento sin procesar del descodificador. En función de las opciones del codificador que admita, también puede exponer capacidades exclusivas del codificador para permitir que las aplicaciones saquen el máximo partido de las características avanzadas del formato de imagen.

El desarrollo de un códec habilitado para WIC requiere la implementación de algunas interfaces nuevas. En muchos casos, puede escribir un contenedor para el códec existente que implementa estas interfaces. Al instalar el códec, debe realizar algunas entradas del registro para que la plataforma WIC pueda detectar el códec y asociarlo con los controladores de metadatos adecuados. También debe invocar una API para borrar la memoria caché en miniatura de las miniaturas predeterminadas (vacías) que puedan haber asociado previamente a las imágenes en el formato. Si lo desea, puede habilitar la Galería fotográfica de Windows Vista para proporcionar a los usuarios un vínculo para descargar el códec cuando la Galería fotográfica encuentre una imagen con la extensión de nombre de archivo. Para ello, debe proporcionar a Microsoft información sobre la extensión de nombre de archivo del códec y la dirección URL del sitio de descarga.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Instalación y registro de CÓDECs](-wic-codecinstallandreg.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



