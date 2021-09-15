---
description: Implementación de IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: Implementación de IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bfe53e87dae52d004fa90d1104fb60f252085d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467933"
---
# <a name="implementing-iwicmetadatablockreader"></a>Implementación de IWICMetadataBlockReader

## <a name="iwicmetadatablockreader"></a>IWICMetadataBlockReader

A menudo existen varios bloques de metadatos dentro de una imagen, y cada uno expone distintos tipos de información en formatos diferentes. En el Windows componente de creación de imágenes (WIC), los controladores de metadatos son componentes distintos que, como los descodificadores, se pueden detectar en tiempo de ejecución. Cada formato de metadatos tiene un controlador independiente y cada uno de estos controladores de metadatos se puede usar con cualquier formato de imagen que admita el formato de metadatos que controla. Por lo tanto, si el formato de imagen admite EXIF, XMP, IPTC u otro formato, puede aprovechar los controladores de metadatos estándar para estos formatos que se incluyen con WIC y no es necesario escribir los suyos propios. Por supuesto, si crea un nuevo formato de metadatos, debe escribir un controlador de metadatos para él, que se detectará e invocará en tiempo de ejecución igual que los estándar.

> [!Note]  
> Si el formato de imagen se basa en un contenedor Tagged Image File Format (TIFF) o JPEG, no tendrá que escribir ningún controlador de metadatos (a menos que desarrolle un formato de metadatos nuevo o propietario). En los contenedores TIFF y JPEG, los bloques de metadatos se encuentran dentro de IFD y cada contenedor tiene una estructura IFD diferente. WIC proporciona controladores IFD para ambos formatos de contenedor que navegan por la estructura DE IFD y delegan a los controladores de metadatos estándar para acceder a los metadatos dentro de ellos. Por lo tanto, si el formato de imagen se basa en cualquiera de estos contenedores, puede aprovechar automáticamente los controladores DE WIC IFD. Sin embargo, si tiene un formato de contenedor propietario que tiene su propia estructura de metadatos de nivel superior única, debe escribir un controlador que pueda navegar por esa estructura de nivel superior y delegar en los controladores de metadatos adecuados, como hacen los controladores IFD).

 

De la misma manera que WIC proporciona una capa de abstracción para las aplicaciones que les permite trabajar con todos los formatos de imagen de la misma manera a través de un conjunto coherente de interfaces, WIC proporciona una capa de abstracción para los autores de códecs con respecto a los formatos de metadatos. Como se indicó anteriormente, los autores de códecs generalmente no necesitan trabajar directamente con los distintos formatos de metadatos que pueden estar presentes en una imagen. Sin embargo, cada autor de códecs es responsable de proporcionar una manera de enumerar los bloques de metadatos para que se pueda detectar y crear instancias de un controlador de metadatos adecuado para cada bloque.

Debe implementar esta interfaz en la clase decoding de nivel de marco. También es posible que tenga que implementarlo en la clase de descodificador de nivel de contenedor si el formato de imagen expone metadatos globales fuera de cualquier fotograma de imagen individual.

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
-   [Getenumerator](#getenumerator)
-   [GetReaderByIndex](#getreaderbyindex)

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat es**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) igual que el [método GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) en [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

### <a name="getcount"></a>GetCount

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) devuelve el número de bloques de metadatos de nivel superior asociados al marco.

### <a name="getenumerator"></a>GetEnumerator

[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) devuelve un enumerador que el autor de la llamada puede usar para enumerar los bloques de metadatos del marco y leer sus metadatos. Para implementar este método, debe crear un lector de metadatos para cada bloque de metadatos e implementar un objeto de enumeración que enumera la colección de lectores de metadatos. El objeto de enumeración debe implementar [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) para que pueda convertirlo en IEnumUnknown cuando lo devuelva en el parámetro *ppIEnumMetadata.*

Al implementar el objeto de enumeración, puede crear todos los lectores de metadatos cuando cree por primera vez el objeto [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) o cuando cree por primera vez el objeto de enumeración, o bien puede crearlos de forma descomunal dentro de la implementación del método [IEnumUnknown::Next.](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) En muchos casos, es más eficaz crearlos de forma rápida, pero, en el ejemplo siguiente, todos los lectores de bloques se crean en el constructor para ahorrar espacio.


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



Para crear los lectores de metadatos, use el [**método CreateMetadataReaderFromContainer.**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) Al invocar este método, se pasa el GUID del formato de contenedor en el *parámetro guidContainerFormat.* Si tiene preferencia de proveedor para un lector de metadatos, puede pasar el GUID de su proveedor preferido en el *parámetro pGuidVendor.* Por ejemplo, si su empresa escribe controladores de metadatos y desea usar los suyos propios si están presentes, puede pasar el GUID del proveedor. En la mayoría de los casos, simplemente se pasa **NULL** y se permite que el sistema seleccione el lector de metadatos adecuado. Si solicita un proveedor específico y ese proveedor tiene instalado un lector de metadatos en el equipo, WIC devolverá el lector de ese proveedor. Sin embargo, si el proveedor solicitado no tiene instalado un lector de metadatos en el equipo y hay un lector de metadatos adecuado disponible, ese lector se devolverá aunque no sea del proveedor preferido. Si no hay ningún lector de metadatos en el equipo para el tipo de metadatos del bloque, el generador de componentes devolverá el controlador de metadatos desconocido, que tratará el bloque de metadatos como un objeto binario grande (BLOB) y deserializará el bloque de metadatos del archivo sin ningún intento de analizarlo.

Para el *parámetro dwOptions,* realice una operación OR entre [**el WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) adecuado con el [**WICMetadataCreationOptions adecuado.**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) **WICPersistOptions** describe cómo se ha diseñado el contenedor. Little-endian es el valor predeterminado.

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

[**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) especifica si desea recuperar UnknownMetadataHandler si no se encuentra ningún lector de metadatos en la máquina que pueda leer el formato de metadatos de un bloque determinado. **WICMetadataCreationAllowUnknown** es el valor predeterminado y siempre debe permitir la creación de UnknownMetadtataHandler. UnknownMetadataHandler trata los metadatos no reconocidos como BLOB. No puede analizarlo, pero lo escribe en la secuencia como blob y lo conserva intacto cuando se escribe de nuevo en la secuencia durante la codificación. Esto hace que sea seguro crear controladores de metadatos para metadatos propietarios o formatos de metadatos que no se envían con el sistema. Dado que los metadatos se conservan intactos, aunque no haya ningún controlador en el equipo que los reconozca, cuando se instale posteriormente un controlador de metadatos adecuado, los metadatos seguirán estando allí y se pueden leer. Si no permite la creación de UnknownMetadataHandler, la alternativa es descartar o sobrescribir metadatos no reconocidos. Se trata de una forma de pérdida de datos.

> [!Note]  
> Si escribe su propio controlador de metadatos para metadatos propietarios, nunca debe incluir referencias a nada fuera del propio bloque de metadatos. Aunque UnknownMetadataHandler conserva los metadatos intactos, los metadatos se mueven cuando se editan los archivos y las referencias a cualquier elemento fuera de su propio bloque ya no serán válidas cuando esto suceda.

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

El *parámetro pIStream* es la secuencia real que se está descodando. Antes de pasar la secuencia, debe buscar al principio del bloque de metadatos para el que solicita un lector. El lector de metadatos adecuado para el bloque de metadatos en la posición actual de [IStream](/windows/desktop/api/objidl/nn-objidl-istream) se devolverá en el *parámetro pppReader.*

### <a name="getreaderbyindex"></a>GetReaderByIndex

[**GetReaderByIndex devuelve**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) el lector de metadatos en el índice solicitado de la colección.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Implementación de IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Implementación de IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
