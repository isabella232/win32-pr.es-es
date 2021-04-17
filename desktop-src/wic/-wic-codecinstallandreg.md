---
description: Al instalar un códec, debe registrarlo en el registro. También debe asegurarse de que la memoria caché de miniaturas se actualiza en caso de que ya existan imágenes en el formato en el equipo.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Instalación y registro de códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83616071bebdbab14bfdc7dd0f879df3d49789d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706483"
---
# <a name="codec-installation-and-registration"></a>Instalación y registro de códecs

Al instalar un códec, debe registrarlo en el registro. También debe asegurarse de que la memoria caché de miniaturas se actualiza en caso de que ya existan imágenes en el formato en el equipo.

Este tema contiene las siguientes secciones:

-   [Registro de un códec](#registering-a-codec)
-   [Actualización de la caché en miniatura al instalar el códec](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [Poner el códec de WIC-Enabled a disposición de los usuarios](#making-your-wic-enabled-codec-available-to-users)
-   [Temas relacionados](#related-topics)

## <a name="registering-a-codec"></a>Registro de un códec

Al registrar un códec, en realidad está registrando dos componentes: el codificador y el descodificador. También debe crear entradas del registro para registrar el formato de contenedor con los controladores de metadatos para los formatos de metadatos que admite el formato de imagen.

En los temas siguientes se describen las entradas del registro necesarias para registrar el códec:

[Entradas generales del registro](-wic-generalregentries.md)

[Entradas del registro específicas del codificador](-wic-encoderregentries.md)

[Entradas del registro específicas del descodificador](-wic-decoderregentries.md)

[Integración con la Galería fotográfica de Windows y el explorador de Windows](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a>Actualización de la caché en miniatura al instalar el códec

Cuando se instala un códec, el instalador debe llamar a la función siguiente después de escribir sus entradas del registro.


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



Esta llamada notifica a Windows que la nueva información de Asociación de archivos está disponible. Si ya existen imágenes en el formato de imagen en el equipo, la caché en miniatura contendrá miniaturas predeterminadas, ya que no hay ningún descodificador disponible para extraer las miniaturas cuando se adquirieron por primera vez. Al notificar a Windows que hay disponible una nueva asociación de archivos, la caché en miniatura descarta cualquier miniatura vacía y extrae las miniaturas reales de los archivos que ahora se pueden descodificar.

## <a name="making-your-wic-enabled-codec-available-to-users"></a>Poner el códec de WIC-Enabled a disposición de los usuarios

Si es un fabricante de la cámara, puede enviar sus códecs sin formato en el cuadro con las cámaras. También puede publicar los códecs en la página de descarga del sitio Web. Sin embargo, si un usuario adquiere un archivo de imagen en el formato de otro origen, como un amigo, un socio comercial o algún otro sitio web, es posible que no sepa dónde obtener el códec para descodificarlo.

Debido a este problema, Windows ofrece una forma más fácil de que los usuarios del formato de imagen encuentren el códec y lo descarguen en su equipo, a partir de Windows Vista. Si la Galería fotográfica de Windows reconoce una extensión de nombre de archivo como formato de imagen y el códec para ese formato no está instalado, un cuadro de diálogo indica al usuario que no se puede mostrar la foto y pregunta si el usuario desea descargar el software necesario para mostrarlo. Cuando el usuario acepta, aparece un sitio web hospedado por Microsoft con un vínculo al sitio de descarga del fabricante del códec. (Opcionalmente, puede solicitar que los usuarios se tomen directamente en el sitio de descarga).

Si desea que la Galería fotográfica de Windows reconozca las extensiones de nombre de archivo del formato de imagen para que los usuarios puedan dirigirse al sitio de descarga, debe hacer lo siguiente:

1.  Proporcione un sitio de descarga para el códec. (Puede tener una página independiente para cada códec que proporcione o una página que proporcione descargas para todos los códecs).

    El sitio de descarga debe localizarse y buscarse fácilmente en el modelo de cámara.

2.  Proporcione a Microsoft una lista de extensiones para los formatos de imagen y las direcciones URL de los sitios de descarga.

Debe informar a Microsoft de las extensiones de los nuevos códecs que desarrolle en el futuro y de cualquier cambio en las direcciones URL de los sitios de descarga, de modo que la nueva información se pueda agregar a la Galería fotográfica de Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Implementación de IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Conclusión (cómo escribir un códec WIC-Enabled)](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



