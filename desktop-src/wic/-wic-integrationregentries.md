---
description: Este tema se aplica a Windows Vista y versiones posteriores.
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: Integración con Windows Galería de fotos y Windows Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ab2bb725b151a069f53a94a8fb2e31766132d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247562"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a>Integración con Windows Galería de fotos y Windows Explorer

Este tema se aplica a Windows Vista y versiones posteriores. Contiene las secciones siguientes:

-   [Introducción](#introduction)
-   [Integración con el Windows Almacén de propiedades](#integration-with-the-windows-property-store)
-   [Integración con el Windows Galería de fotos](#integration-with-the-windows-photo-gallery)
-   [Integración con la caché Windows miniaturas](#integration-with-the-windows-thumbnail-cache)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Para permitir que Windows Galería de fotos y Windows Explorer muestren miniaturas y busquen y actualicen metadatos de imagen estándar, un códec debe tener asociada una implementación de las interfaces [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) e [IPropertyStore.](/windows/win32/api/propsys/nn-propsys-ipropertystore) La interfaz IThumbnailProvider se usa para recuperar miniaturas y rellenar la caché de miniaturas, y la interfaz IPropertyStore se usa para buscar y actualizar los metadatos asociados a un archivo. A Windows Vista, todos los tipos de archivo tienen miniaturas y metadatos, pero los distintos tipos de archivo requieren implementaciones diferentes de estas interfaces para recuperar o generar las miniaturas y los metadatos para ellos. El sistema proporciona implementaciones predeterminadas de estas interfaces. La implementación predeterminada de IThumbnailProvider se puede usar para cualquier formato de imagen Windows Imaging Component (WIC) habilitado. La implementación predeterminada de IPropertyStore se puede usar con cualquier formato de imagen habilitado para WIC basado en un contenedor Tagged Image File Format (TIFF) o JPEG. Para asociar el formato de imagen a las implementaciones predeterminadas de ambas interfaces, debe agregar solo algunas entradas del Registro.

Las siguientes entradas indican al explorador Windows Galería de fotos y Windows que una extensión de nombre de archivo (.ext) y su tipo MIME asociado están asociados a un formato de imagen.

La entrada siguiente indica a Windows y aplicaciones que usan el tipo de contenido (también conocido como tipo mime) que un archivo con una extensión determinada (.ext) es un formato de imagen. El propietario del tipo de archivo debe elegir un que identifique de forma única el formato de archivo y este valor de tipo de contenido debe registrarse `<image sub type value>` en IANA.

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

La entrada siguiente indica Windows, Windows búsqueda y aplicaciones que usan [System.Kind](../properties/props-system-kind.md) que una extensión de nombre de archivo (.ext) debe tratarse como una imagen. En concreto, indica que la propiedad System.Kind de la extensión de archivo debe establecerse en Picture.

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

## <a name="integration-with-the-windows-property-store"></a>Integración con el Windows Almacén de propiedades

A veces, las mismas propiedades de metadatos se exponen en esquemas de metadatos diferentes, a menudo con nombres de propiedad diferentes. Cuando se actualiza una de estas propiedades, pero las demás no, los metadatos del archivo pueden no estar sincronizados. El controlador de propiedades photo proporciona la implementación predeterminada de **IPropertyStore** para las imágenes, y lo usan las aplicaciones, así como el explorador de Windows Galería de fotos y Windows para garantizar que todos los metadatos de una imagen permanecen sincronizados y que las propiedades mostradas por las aplicaciones son coherentes con las mostradas por el Explorador de Windows Galería de fotos y Windows. Cuando el controlador de propiedades photo actualiza los metadatos, se asegura de que estas propiedades se actualizan de forma coherente en todos los formatos de metadatos comunes que están presentes en el archivo.

El controlador de propiedades photo debe comprender el formato del contenedor y cómo localizar las distintas propiedades dentro de él. En general, no es posible que el controlador de propiedades de foto sepa cómo se han diseñado los distintos bloques de metadatos en un formato de contenedor propietario. Sin embargo, si los metadatos en el formato de contenedor se establecen de la misma manera que los metadatos en un formato de contenedor TIFF o en un formato de contenedor JPEG, el controlador de propiedades de foto puede aprovechar ese conocimiento para actualizar los metadatos de forma coherente también en el formato de contenedor.

Puede registrar esta asociación mediante la creación de la siguiente entrada del Registro. Esta entrada notifica al controlador de propiedades photo que el formato de contenedor identificado por este GUID entiende las mismas rutas de acceso del lenguaje de consulta de metadatos que el formato de contenedor con el GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3. (163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 es el GUID del formato de contenedor TIFF).

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

La entrada siguiente asocia la implementación predeterminada del controlador de propiedades photo de **IPropertyStore** con los archivos que tienen la extensión ".ext". El primer GUID es el IID de la interfaz **IPropertyStore** y el segundo es el GUID de la implementación del controlador de propiedades photo de él.

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

Los códecs que usan un formato propietario que no es compatible con el formato de contenedor TIFF o JPEG deben escribir su propia **implementación de IPropertyStore.**

## <a name="integration-with-the-windows-photo-gallery"></a>Integración con el Windows Galería de fotos

Windows Galería de fotos se basa en WIC y puede mostrar cualquier formato de imagen habilitado para WIC para el que esté instalado el códec. Para notificar al sistema que el formato de imagen se puede abrir en Windows Galería de fotos, debe crear una asociación de archivos mediante la creación de las siguientes entradas del Registro.

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

El ProgID suele ser la extensión de nombre de archivo anexada con la palabra "file". (Por ejemplo, si la extensión de nombre de archivo .txt, el ProgID normalmente sería "txtfile").

Hay otras entradas estándar del Registro que puede que necesite crear para admitir asociaciones de archivos. sin embargo, dado que y no son específicos de WIC, están fuera del ámbito de este tema.

## <a name="integration-with-the-windows-thumbnail-cache"></a>Integración con la caché Windows miniaturas

Las dos entradas siguientes indican que la implementación del proveedor de miniaturas de WIC estándar se puede usar para recuperar miniaturas de archivos con esta extensión. El primer GUID es el IID de la [interfaz IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) y el segundo es el GUID de la implementación estándar del sistema de esta interfaz. (Todas las entradas de HLCR \\ .ext \\ ShellEx se repiten en \\ HKCR \\ SystemFileAssociations \\ .ext \\ ShellEx \\ ).

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

**Conceptual**
</dt> <dt>

[Entradas del Registro específicas del codificador](-wic-decoderregentries.md)
</dt> <dt>

[Instalación y registro de CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
