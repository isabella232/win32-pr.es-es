---
description: Implementar IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: Implementar IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bfe53e87dae52d004fa90d1104fb60f252085d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910166"
---
# <a name="implementing-iwicmetadatablockreader"></a>Implementar IWICMetadataBlockReader

## <a name="iwicmetadatablockreader"></a>IWICMetadataBlockReader

A menudo existen varios bloques de metadatos en una imagen, cada uno de los cuales expone diferentes tipos de información en distintos formatos. En el modelo de componentes de imágenes de Windows (WIC), los controladores de metadatos son componentes distintos que, como los descodificadores, son reconocibles en tiempo de ejecución. Cada formato de metadatos tiene un controlador independiente, y cada uno de estos controladores de metadatos se puede usar con cualquier formato de imagen que admita el formato de metadatos que controla. Por lo tanto, si el formato de imagen admite EXIF, XMP, IPTC u otro formato, puede aprovechar los controladores de metadatos estándar para estos formatos que se distribuyen con WIC y no es necesario que escriba los suyos propios. Por supuesto, si crea un nuevo formato de metadatos, debe escribir un controlador de metadatos para él, que se detectará y se invocará en tiempo de ejecución del mismo modo que los estándares.

> [!Note]  
> Si el formato de la imagen se basa en un contenedor Tagged Image File Format (TIFF) o JPEG, no tendrá que escribir ningún controlador de metadatos (a menos que desarrolle un formato de metadatos nuevo o propietario). En los contenedores TIFF y JPEG, los bloques de metadatos se encuentran dentro de IFDs y cada contenedor tiene una estructura de IFD diferente. WIC proporciona controladores de IFD para ambos formatos de contenedor que navegan por la estructura de IFD y delegan en los controladores de metadatos estándar para tener acceso a los metadatos de ellos. Por lo tanto, si el formato de la imagen se basa en cualquiera de estos contenedores, puede aprovechar automáticamente los controladores de la IFD de WIC. Sin embargo, si tiene un formato de contenedor propietario que tiene su propia estructura de metadatos de nivel superior única, debe escribir un controlador que pueda navegar por esa estructura de nivel superior y delegar en los controladores de metadatos adecuados, al igual que hacen los controladores de IFD.

 

Del mismo modo que WIC proporciona una capa de abstracción para aplicaciones que les permite trabajar con todos los formatos de imagen de la misma manera a través de un conjunto coherente de interfaces, WIC proporciona una capa de abstracción para los autores de códecs con respecto a los formatos de metadatos. Como se indicó anteriormente, los creadores de códecs no suelen tener que trabajar directamente con los distintos formatos de metadatos que pueden estar presentes en una imagen. Sin embargo, cada autor de códec es responsable de proporcionar una manera de enumerar los bloques de metadatos para que se pueda detectar y crear una instancia de un controlador de metadatos adecuado para cada bloque.

Debe implementar esta interfaz en la clase de descodificación de nivel de marco. También puede ser necesario implementarlo en la clase descodificador de nivel de contenedor si el formato de la imagen expone metadatos globales fuera de los fotogramas de imagen individuales.

``` syntax
interface IWICMetadataBlockReader : IUnknown
{
   // All methods required
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetCount ( UINT *pcCount );
   HRESULT GetEnumerator ( IEnumUnknown **ppIEnumMetadata );
   HRESULT GetReaderByIndex ( UINT nIndex, IWICMetadataReader **ppIMetadataReader );
}
```

-   [GetContainerFormat](#getcontainerformat)
-   [GetCount](#getcount)
-   [GetEnumerator](#getenumerator)
-   [GetReaderByIndex](#getreaderbyindex)

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) es el mismo que el método [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) en la [implementación de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

### <a name="getcount"></a>GetCount

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) devuelve el número de bloques de metadatos de nivel superior asociados al marco.

### <a name="getenumerator"></a>GetEnumerator

[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) devuelve un enumerador que el llamador puede utilizar para enumerar los bloques de metadatos del marco y leer sus metadatos. Para implementar este método, debe crear un lector de metadatos para cada bloque de metadatos e implementar un objeto de enumeración que Enumere la colección de lectores de metadatos. El objeto de enumeración debe implementar [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) para que pueda convertirlo en IEnumUnknown cuando lo devuelva en el parámetro *ppIEnumMetadata* .

Al implementar el objeto de enumeración, se pueden crear todos los lectores de metadatos cuando se crea por primera vez el objeto [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) o cuando se crea por primera vez el objeto de enumeración, o se pueden crear de forma diferida dentro de la implementación del método [IEnumUnknown:: Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) . En muchos casos, es más eficaz crearlos de forma diferida pero, en el ejemplo siguiente, se crean todos los lectores de bloque en el constructor para ahorrar espacio.


```C++
public class MetadataReaderEnumerator : public IEnumUnknown
{
   UINT m_current;
   UINT m_blockCount;
   IWICMetadataReader** m_ppMetadataReader;
   IStream* m_pStream;

   MetadataReaderEnumerator() 
   {
       // Set m_blockCount to the number of metadata blocks in the frame. 
      ...
      m_ppMetadataReader = IWICMetadataReader*[m_blockCount];
       m_current = 0;

      for (UINT x=0; x < m_blockCount; x++) 
      {
         // Find the position in the file where the xth
         // block of metadata lives and seek m_piStream 
         // to that position.
         ...

         m_pComponentFactory->CreateMetadataReaderFromContainer(
            GUID_ContainerFormatTiff,
                        NULL,
                        WICPersistOptions.WICPersistOptionsDefault | 
            WICMetadataCreationOptions.WICMetadataCreationDefault, 
                        m_pStream, &m_ppMetadataReader[x]);
        }
    }

    // Implementation of IEnumUnknown and IUnknown interfaces
    ...
}
```



Para crear los lectores de metadatos, se usa el método [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) . Al invocar este método, se pasa el GUID del formato de contenedor en el parámetro *guidContainerFormat* . Si tiene una preferencia de proveedor para un lector de metadatos, puede pasar el GUID de su proveedor preferido en el parámetro *pGuidVendor* . Por ejemplo, si su compañía escribe controladores de metadatos y desea utilizar el suyo propio, puede pasar el GUID del proveedor. En la mayoría de los casos, simplemente pasaría **null** y dejar que el sistema Seleccione el lector de metadatos adecuado. Si solicita un proveedor específico y ese proveedor tiene un lector de metadatos instalado en el equipo, WIC devolverá el lector del proveedor. Sin embargo, si el proveedor solicitado no tiene un lector de metadatos instalado en el equipo y está disponible un lector de metadatos adecuado, se devolverá ese lector aunque no sea del proveedor preferido. Si no hay ningún lector de metadatos en el equipo para el tipo de metadatos en el bloque, el generador de componentes devolverá el controlador de metadatos desconocido, que tratará el bloque de metadatos como un objeto binario grande (BLOB) y deserializará el bloque de metadatos del archivo sin que se intente analizarlo.

Para el parámetro *dwOptions* , realice una operación OR entre el [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) adecuado con el [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions)adecuado. El **WICPersistOptions** describe cómo se diseña el contenedor. Little-Endian es el valor predeterminado.

``` syntax
enum WICPersistOptions
{   
   WICPersistOptionDefault,
   WICPersistOptionLittleEndian,
   WICPersistOptionBigEndian,
   WICPersistOptionStrictFormat,
   WICPersistOptionNoCacheStream,
   WICPersistOptionPreferUTF8
};
```

El [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) especifica si desea obtener el UnknownMetadataHandler si no se encuentra ningún lector de metadatos en el equipo que pueda leer el formato de metadatos de un bloque determinado. **WICMetadataCreationAllowUnknown** es el valor predeterminado y siempre debe permitir la creación de UnknownMetadtataHandler. UnknownMetadataHandler trata los metadatos no reconocidos como un BLOB. No puede analizarlo, pero lo escribe en la secuencia como un BLOB y lo conserva intacto cuando se vuelve a escribir en la secuencia durante la codificación. Esto hace que sea seguro crear controladores de metadatos para metadatos de propietario o formatos de metadatos que no se distribuyen con el sistema. Dado que los metadatos se conservan intactos, incluso si no hay ningún controlador en el equipo que lo reconozca, cuando se instale posteriormente un controlador de metadatos adecuado, los metadatos seguirán estando allí y se podrán leer. Si no permite la creación de UnknownMetadataHandler, la alternativa es descartar o sobrescribir metadatos no reconocidos. Se trata de una forma de pérdida de datos.

> [!Note]  
> Si escribe su propio controlador de metadatos para los metadatos de propiedad, nunca debe incluir referencias a nada fuera del propio bloque de metadatos. Aunque el UnknownMetadataHandler conserva los metadatos intactos, los metadatos se mueven cuando se editan los archivos y las referencias a cualquier elemento que esté fuera de su propio bloque dejarán de ser válidos cuando esto suceda.

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

El parámetro *pIStream* es el flujo real que se va a descodificar. Antes de pasar el flujo, debe buscar el principio del bloque de metadatos para el que está solicitando un lector. El lector de metadatos adecuado para el bloque de metadatos en la posición actual en [IStream](/windows/desktop/api/objidl/nn-objidl-istream) se devolverá en el parámetro *ppiReader* .

### <a name="getreaderbyindex"></a>GetReaderByIndex

[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) devuelve el lector de metadatos en el índice solicitado de la colección.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Vista**
</dt> <dt>

[Implementación de IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Implementación de IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
