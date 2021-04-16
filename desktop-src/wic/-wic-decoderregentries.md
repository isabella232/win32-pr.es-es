---
description: Decoder-Specific entradas del registro
ms.assetid: 64ef260a-ed7f-4253-a644-bd3352b0ee41
title: Decoder-Specific entradas del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17485e7adca62abd31643d84d371a0002724ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720751"
---
# <a name="decoder-specific-registry-entries"></a>Decoder-Specific entradas del registro


Además de las entradas del registro necesarias para todos los codificadores y descodificadores, se requieren las siguientes entradas del registro específicamente para los descodificadores.

Estas entradas registran el descodificador en la categoría de descodificadores de componentes de creación de imágenes de Windows (WIC). El primer GUID de estas entradas es el identificador de categoría (CATId) para [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

```
HKEY_CLASSES_ROOT
   CLSID
      {7ED96837-96F0-4812-B211-F13C24117ED3}
         Instance
            {Decoder CLSID}
               CLSID = {Decoder CLSID}
               FriendlyName = {Name of Decoder}
```

Como se indicó en la sección de [detección y arbitraje](-wic-howwicworks.md) de cómo funciona el componente de creación de imágenes de Windows, el mecanismo que permite detectar un descodificador adecuado para una imagen específica se detecta en tiempo de ejecución se basa en la coincidencia de un patrón de identificación incrustado en el archivo de imagen con un patrón especificado en la entrada del registro del descodificador. Para habilitar la detección en tiempo de ejecución de los descodificadores, debe registrar el patrón de identificación único para el formato de imagen como se indica a continuación. Todas estas entradas del registro son necesarias, a excepción de la entrada **EndOfStream** , que es opcional, como se describe en la tabla siguiente.

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
| Patrón     | Bits reales que componen el modelo. Estos son los bits que se comparan con el patrón de identificación en un archivo de imagen durante la detección.                                                                                                                                                                                |
| Máscara        | Permite valores comodín en los patrones. La máscara se aplica mediante la realización de una operación AND lógica en el patrón y la máscara. Cualquier bit del patrón que se corresponda con un bit de la máscara con un valor de 0 se omite.                                                                                                       |
| EndOfStream | El desplazamiento del patrón de identificación se debe calcular desde el final de la secuencia, en lugar de desde el principio. Algunos formatos de imagen colocan el patrón de identificación en el final del archivo o cerca de él. Dado que el valor predeterminado es buscar desde el principio, a menos que el patrón esté cerca del final del archivo, puede omitir esta entrada. |



 

Un códec puede admitir más de un patrón de identificación. En ese caso, se repiten todas las claves de **\_ las clases HKEY \_ raíz \\ CLSID \\ {Encoder CLSID} \\ patrones** y se usa la clave numérica (0 en el ejemplo) para distinguir entre los distintos patrones. Debe incluir cada uno de los cuatro valores de la clave para cada patrón.

## <a name="registering-a-container-format-with-metadata-readers"></a>Registro de un formato de contenedor con lectores de metadatos

Si crea un nuevo formato de contenedor para el códec, también debe crear entradas del registro para admitir la detección de lectores de metadatos para los bloques de metadatos de las imágenes, tal como hizo con los escritores de metadatos. Las siguientes entradas deben crearse en el identificador de clase (CLSID) del lector de metadatos para cada formato de metadatos que admita el formato de contenedor. (Tenga en cuenta que, si el códec usa un contenedor de Tagged Image File Format (TIFF), esta información ya está en el registro).

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

Dado que las entradas de los lectores de metadatos también se usan para la detección, son muy similares a las entradas de los descodificadores. El generador de componentes usa estas entradas para buscar los lectores de metadatos admitidos por el contenedor y seleccionar el adecuado cuando la implementación de [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) solicita un lector de metadatos.



| Value      | Descripción                                                                                                                                                                                                                                                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Posición   | Desplazamiento en el contenedor del bloque de metadatos donde se puede encontrar el encabezado de metadatos. En el caso de los bloques de metadatos de nivel superior, este es el desplazamiento en la secuencia de archivos. En el caso de los bloques de metadatos anidados en otros bloques de metadatos, es el desplazamiento relativo al bloque de metadatos contenedor. |
| Patrón    | Bits reales que componen el modelo. Estos son los bits que se comparan con el patrón de identificación en un archivo de imagen durante la detección.                                                                                                                            |
| Máscara       | El encabezado de metadatos se define generalmente mediante el controlador de metadatos. Debe utilizar el encabezado de metadatos estándar para cada lector a menos que, por algún motivo, el patrón deba tener un formato diferente en el contenedor.                                                          |
| DataOffset | Desplazamiento desde el principio del encabezado de metadatos en el que se inician los datos reales. En los casos en los que los metadatos no se encuentran en un desplazamiento específico del encabezado, esta entrada se puede omitir.                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Entradas del registro específicas del codificador](-wic-encoderregentries.md)
</dt> <dt>

[Integración con la Galería fotográfica de Windows y el explorador de Windows](-wic-integrationregentries.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



