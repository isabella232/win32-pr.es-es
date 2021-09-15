---
description: Decoder-Specific entradas del Registro
ms.assetid: 64ef260a-ed7f-4253-a644-bd3352b0ee41
title: Decoder-Specific entradas del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17485e7adca62abd31643d84d371a0002724ea9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570316"
---
# <a name="decoder-specific-registry-entries"></a>Decoder-Specific entradas del Registro


Además de las entradas del Registro necesarias para todos los codificadores y descodificadores, se requieren las siguientes entradas del Registro específicamente para los descodificadores.

Estas entradas registran el descodificador en la categoría de descodificadores Windows Imaging Component (WIC). El primer GUID de estas entradas es el identificador de categoría (CATID) [**para WICBitmapDecoders.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)

```
HKEY_CLASSES_ROOT
   CLSID
      {7ED96837-96F0-4812-B211-F13C24117ED3}
         Instance
            {Decoder CLSID}
               CLSID = {Decoder CLSID}
               FriendlyName = {Name of Decoder}
```

Como se [](-wic-howwicworks.md) indicó en la sección Detección y arbitraje de Cómo funciona el componente de creación de imágenes de Windows, el mecanismo que permite detectar un descodificador adecuado para una imagen específica en tiempo de ejecución se basa en la coincidencia de un patrón de identificación insertado en el archivo de imagen con un patrón especificado en la entrada del registro del descodificador. Para habilitar la detección en tiempo de ejecución de descodificadores, debe registrar el patrón de identificación único para el formato de imagen como se muestra a continuación. Todas estas entradas del Registro son necesarias, excepto la **entrada EndOfStream,** que es opcional, como se describe en la tabla siguiente.

```
HKEY_CLASSES_ROOT
   CLSID
      {Decoder CLSID}
         Patterns
            {0}
               Position = Offset in block
               Length = Length of pattern
               Pattern = Pattern to match
               Mask = FF FF FF FF
               EndOfStream = 0|1
```



| Value       | Descripción                                                                                                                                                                                                                                                                                                                     |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Posición    | Desplazamiento en el archivo donde se puede encontrar el patrón.                                                                                                                                                                                                                                                                        |
| Length      | Longitud del patrón.                                                                                                                                                                                                                                                                                                      |
| Patrón     | Bits reales que representan el patrón. Estos son los bits que se comparan con el patrón de identificación en un archivo de imagen durante la detección.                                                                                                                                                                                |
| Máscara        | Permite valores comodín en patrones. La máscara se aplica realizando una operación AND lógica en el patrón y la máscara. Se omite cualquier bit del patrón que se corresponda con un bit de la máscara con un valor de 0.                                                                                                       |
| EndOfStream | El desplazamiento del patrón de identificación debe calcularse desde el final de la secuencia, en lugar de desde el principio. Algunos formatos de imagen coloca el patrón de identificación al final del archivo o cerca de este. Dado que el valor predeterminado es buscar desde el principio, a menos que el patrón esté cerca del final del archivo, puede omitir esta entrada. |



 

Un códec puede admitir más de un patrón de identificación. En ese caso, repetiría todas las claves bajo **HKEY \_ CLASSES ROOT \_ \\ CLSID \\ {Decoder CLSID} \\ Patterns** y usaría la clave numérica (0 en el ejemplo) para distinguir entre los distintos patrones. Debe incluir cada uno de los cuatro valores bajo la clave para cada patrón.

## <a name="registering-a-container-format-with-metadata-readers"></a>Registro de un formato de contenedor con lectores de metadatos

Si crea un nuevo formato de contenedor para el códec, también debe crear entradas del Registro para admitir la detección de lectores de metadatos para los bloques de metadatos de las imágenes, como hizo para los escritores de metadatos. Las siguientes entradas deben crearse en el identificador de clase (CLSID) del lector de metadatos para cada formato de metadatos que admita el formato de contenedor. (Tenga en cuenta que, si el códec usa un contenedor Tagged Image File Format (TIFF), esta información ya está en el registro).

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Reader CLSID}
         Containers
            {Container Format GUID}
               
                  Position = Offset relative to its container
                  Pattern = Pattern used for metadata header
                  Mask = FF FF FF FF
                  DataOffset = Offset from beginning of header
```

Dado que las entradas de los lectores de metadatos también se usan para la detección, son muy similares a las entradas de los descodificadores. El generador de componentes usa estas entradas para buscar los lectores de metadatos admitidos por el contenedor y para seleccionar el adecuado, cuando la implementación de [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) solicita un lector de metadatos.



| Value      | Descripción                                                                                                                                                                                                                                                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Posición   | Desplazamiento en el contenedor del bloque de metadatos donde se puede encontrar el encabezado de metadatos. Para los bloques de metadatos de nivel superior, este es el desplazamiento en la secuencia de archivos. Para los bloques de metadatos anidados en otros bloques de metadatos, es el desplazamiento relativo al bloque de metadatos que lo contiene. |
| Patrón    | Bits reales que representan el patrón. Estos son los bits que se comparan con el patrón de identificación en un archivo de imagen durante la detección.                                                                                                                            |
| Máscara       | Normalmente, el controlador de metadatos define el encabezado de metadatos. Debe usar el encabezado de metadatos estándar para cada lector, a menos que, por algún motivo, el patrón tenga un formato diferente en el contenedor.                                                          |
| DataOffset | Desplazamiento desde el principio del encabezado de metadatos en el que comienzan los datos reales. En los casos en los que los metadatos no se encuentran en un desplazamiento específico del encabezado, se puede omitir esta entrada.                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Entradas del Registro específicas del codificador](-wic-encoderregentries.md)
</dt> <dt>

[Integración con Windows Galería de fotos y Windows Explorer](-wic-integrationregentries.md)
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



