---
description: Al instalar un códec, debe registrarlo en el registro. También debe asegurarse de que la caché de miniaturas se actualiza en caso de que ya exista alguna imagen con el formato en el equipo.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Instalación y registro de códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83616071bebdbab14bfdc7dd0f879df3d49789d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359618"
---
# <a name="codec-installation-and-registration"></a>Instalación y registro de códecs

Al instalar un códec, debe registrarlo en el registro. También debe asegurarse de que la caché de miniaturas se actualiza en caso de que ya exista alguna imagen con el formato en el equipo.

Este tema contiene las siguientes secciones:

-   [Registro de un códec](#registering-a-codec)
-   [Actualizar la caché de miniaturas al instalar el códec](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [Hacer que el códec WIC-Enabled esté disponible para los usuarios](#making-your-wic-enabled-codec-available-to-users)
-   [Temas relacionados](#related-topics)

## <a name="registering-a-codec"></a>Registro de un códec

Cuando se registra un códec, realmente se registran dos componentes: el codificador y el descodificador. También debe crear entradas del Registro para registrar el formato de contenedor con los controladores de metadatos para los formatos de metadatos que admite el formato de imagen.

En los temas siguientes se describen las entradas del Registro que necesita para registrar el códec:

[Entradas generales del Registro](-wic-generalregentries.md)

[Entradas del Registro específicas del codificador](-wic-encoderregentries.md)

[Entradas del Registro específicas del descodificador](-wic-decoderregentries.md)

[Integración con Windows Galería de fotos y Windows Explorer](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a>Actualizar la caché de miniaturas al instalar el códec

Cuando se instala un códec, el instalador debe llamar a la siguiente función después de escribir sus entradas del Registro.


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



Esta llamada notifica a Windows que hay disponible nueva información de asociación de archivos. Si las imágenes en formato de imagen ya existen en el equipo, la caché de miniaturas contendrá miniaturas predeterminadas para ellas porque no había ningún descodificador disponible para extraer las miniaturas cuando se adquirieron las imágenes por primera vez. Cuando notifica a Windows que hay disponible una nueva asociación de archivos, la caché de miniaturas descarta las miniaturas vacías y extrae las miniaturas reales de los archivos que ahora se pueden descodificar.

## <a name="making-your-wic-enabled-codec-available-to-users"></a>Hacer que el códec WIC-Enabled esté disponible para los usuarios

Si es fabricante de cámaras, puede enviar los códecs sin procesar en la caja con las cámaras. También puede publicar los códecs en la página Descargar del sitio web. Sin embargo, si un usuario adquiere un archivo de imagen en el formato de otro origen, como un amigo, un asociado comercial o algún otro sitio web, es posible que no sepa dónde obtener el códec con el que descodificarlo.

Debido a este problema, Windows ofrece una manera más sencilla para que los usuarios del formato de imagen encuentren el códec y lo descarguen en su equipo, empezando por Windows Vista. Si el Windows Galería de fotos reconoce una extensión de nombre de archivo como formato de imagen y el códec de ese formato no está instalado, un cuadro de diálogo indica al usuario que no se puede mostrar la foto y pregunta si el usuario quiere descargar el software necesario para mostrarla. Cuando el usuario acepta, aparece un sitio web hospedado por Microsoft con un vínculo al sitio de descarga del fabricante del códec. (Opcionalmente, puede solicitar que los usuarios se alo den directamente al sitio de descarga).

Si desea que el Windows Galería de fotos reconozca las extensiones de nombre de archivo del formato de imagen para que los usuarios puedan dirigirse al sitio de descarga, debe hacer lo siguiente:

1.  Proporcione un sitio de descarga para el códec. (Puede tener una página independiente para cada códec que proporcione, o una página que proporcione descargas para todos los códecs).

    El sitio de descarga se debe localizar y buscar fácilmente mediante el modelo de cámara.

2.  Proporcione a Microsoft una lista de extensiones para los formatos de imagen y las direcciones URL de los sitios de descarga.

Debe informar a Microsoft de las extensiones de los códecs nuevos que desarrolle en el futuro y de los cambios en las direcciones URL de los sitios de descarga para que la nueva información se pueda agregar a la Windows Galería de fotos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Implementación de IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Conclusión (Cómo escribir un códec de WIC-Enabled)](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



