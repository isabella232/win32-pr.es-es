---
description: Este tema se aplica a Windows Vista y versiones posteriores.
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: Integración con la Galería fotográfica de Windows y el explorador de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ab2bb725b151a069f53a94a8fb2e31766132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648507"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a>Integración con la Galería fotográfica de Windows y el explorador de Windows

Este tema se aplica a Windows Vista y versiones posteriores. Contiene las secciones siguientes:

-   [Introducción](#introduction)
-   [Integración con el almacén de propiedades de Windows](#integration-with-the-windows-property-store)
-   [Integración con la Galería fotográfica de Windows](#integration-with-the-windows-photo-gallery)
-   [Integración con la caché en miniatura de Windows](#integration-with-the-windows-thumbnail-cache)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Para habilitar la Galería fotográfica de Windows y el explorador de Windows para Mostrar miniaturas y buscar y actualizar los metadatos de imagen estándar, un códec debe tener una implementación de las interfaces [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) y [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) asociadas a él. La interfaz IThumbnailProvider se usa para recuperar miniaturas y rellenar la caché en miniatura, y la interfaz IPropertyStore se usa para buscar y actualizar los metadatos asociados a un archivo. A partir de Windows Vista, todos los tipos de archivo tienen vistas en miniatura y metadatos, pero los distintos tipos de archivo requieren implementaciones diferentes de estas interfaces para recuperar o generar las miniaturas y metadatos para ellos. El sistema proporciona implementaciones predeterminadas de estas interfaces. La implementación predeterminada de IThumbnailProvider se puede usar para cualquier formato de imagen habilitado para Windows Imaging Component (WIC). La implementación predeterminada de IPropertyStore se puede usar con cualquier formato de imagen habilitado para WIC que esté basado en un contenedor Tagged Image File Format (TIFF) o JPEG. Para asociar el formato de imagen con las implementaciones predeterminadas de estas dos interfaces, debe agregar solo algunas entradas del registro.

Las siguientes entradas indican a la Galería fotográfica de Windows y al explorador de Windows que una extensión de nombre de archivo (. ext) y su tipo MIME asociado están asociados a un formato de imagen.

La entrada siguiente indica a Windows y a las aplicaciones que usan el tipo de contenido (también conocido como tipo MIME) que un archivo con una extensión determinada (. ext) es un formato de imagen. El propietario del tipo de archivo debe elegir un `<image sub type value>` que identifique de forma única el formato de archivo y este valor de tipo de contenido debe registrarse con IANA.

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

La entrada siguiente indica a Windows, a Windows Search y a las aplicaciones que usan [System. Kind](../properties/props-system-kind.md) que una extensión de nombre de archivo (. ext) debe tratarse como una imagen. En concreto, indica que la propiedad System. Kind de la extensión de archivo debe establecerse en Picture.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     {.ext} = Picture
```

## <a name="integration-with-the-windows-property-store"></a>Integración con el almacén de propiedades de Windows

A veces, las mismas propiedades de metadatos se exponen en distintos esquemas de metadatos, a menudo con distintos nombres de propiedad. Cuando se actualiza una de estas propiedades, pero no las demás, los metadatos del archivo pueden no estar sincronizados. El controlador de propiedades de fotografía proporciona la implementación predeterminada de **IPropertyStore** para las imágenes y la usan las aplicaciones, así como la Galería fotográfica de Windows y el explorador de Windows para asegurarse de que todos los metadatos de una imagen permanecen sincronizados y que las propiedades mostradas por las aplicaciones son coherentes con las que se muestran en la Galería fotográfica de Windows y el explorador de Windows. Cuando el controlador de propiedades de la fotografía actualiza los metadatos, se asegura de que estas propiedades se actualizan de forma coherente en todos los formatos de metadatos comunes que se encuentran en el archivo.

El controlador de la propiedad Photo debe comprender el formato del contenedor y cómo buscar las distintas propiedades que contiene. En general, no es posible que el controlador de la propiedad Photo sepa cómo se colocan los distintos bloques de metadatos en un formato de contenedor propietario. Sin embargo, si los metadatos del formato de contenedor se disponen de la misma manera que los metadatos en un formato de contenedor TIFF o en un formato de contenedor JPEG, el controlador de propiedades de fotografía puede aprovechar este conocimiento para actualizar los metadatos de forma coherente también en el formato de contenedor.

Puede registrar esta asociación creando la siguiente entrada del registro. Esta entrada notifica al controlador de propiedades de la fotografía que el formato de contenedor identificado por este GUID entiende las mismas rutas de acceso de lenguaje de consulta de metadatos que el formato de contenedor con el GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3. (163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 es el GUID para el formato de contenedor TIFF).

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  ContainerAssociations
                     {Container Format GUID} = {163bcc30-e2e9-4f0b-961d-a3e9fdb788a3}
```

La entrada siguiente asocia la implementación predeterminada del controlador de la propiedad de foto de **IPropertyStore** con los archivos que tienen la extensión ". ext". El primer GUID es el IID de la interfaz **IPropertyStore** y el segundo es el GUID de la implementación del controlador de propiedades de la fotografía.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  {.ext}
                     (Default) = {a38b883c-1682-497e-97b0-0a3a9e801682}
```

Los códecs que usan un formato propietario que no es compatible con el formato de contenedor TIFF o JPEG deben escribir su propia implementación de **IPropertyStore** .

## <a name="integration-with-the-windows-photo-gallery"></a>Integración con la Galería fotográfica de Windows

La Galería fotográfica de Windows se basa en WIC y puede mostrar cualquier formato de imagen habilitado para WIC para el que esté instalado el códec. Para notificar al sistema que el formato de imagen se puede abrir en la Galería fotográfica de Windows, debe crear una asociación de archivo creando las siguientes entradas del registro.

```
HKEY_CLASSES_ROOT
   {.ext}
      (Default) = {ProgID} for example, jpegfile)
      OpenWithProgids
         {ProgID}
      OpenWithList
         PhotoViewer.dll
      ShellEx
         ContextMenuHandlers
            ShellImagePreview
               (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   SystemFileAssociations
      {.ext}
         OpenWithList
            PhotoViewer.dll
         ShellEx
            ContextMenuHandlers
               ShellImagePreview
                  (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   {Image Format ProgID}
      (Default) = Name of Image Format
      DefaultIcon
         (Default) = Path to icon for type, icon index
      shell
         open
            MuiVerb = @%PROGRAMFILES%\Windows Photo Gallery\photoviewer.dll,-3043
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%ProgramFiles%\Windows Photo Gallery\PhotoViewer.dll", ImageView_Fullscreen %1
            DropTarget
               Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
         printo
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%SystemRoot%\System32\shimgvw.dll", ImageView_PrintTo /pt "%1" "%2" "%3" "%4"
```

El ProgID suele ser la extensión de nombre de archivo anexada con la palabra "File". (Por ejemplo, si la extensión de nombre de archivo es. txt, el ProgID sería normalmente "TXTfile").

Hay otras entradas de registro estándar que es posible que tenga que crear para admitir asociaciones de archivo. sin embargo, como los the'y no son específicos de WIC, quedan fuera del ámbito de este tema.

## <a name="integration-with-the-windows-thumbnail-cache"></a>Integración con la caché en miniatura de Windows

Las dos entradas siguientes indican que la implementación del proveedor de miniaturas de WIC estándar se puede usar para recuperar miniaturas de archivos con esta extensión. El primer GUID es el IID de la interfaz [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) y el segundo es el GUID de la implementación estándar del sistema de esta interfaz. (Todas las entradas de HLCR \\ . ext \\ ShellEx \\ se repiten en HKCR \\ SystemFileAssociations \\ . ext \\ ShellEx \\ ).

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Entradas del registro específicas del codificador](-wic-decoderregentries.md)
</dt> <dt>

[Instalación y registro de CÓDECs](-wic-codecinstallandreg.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
