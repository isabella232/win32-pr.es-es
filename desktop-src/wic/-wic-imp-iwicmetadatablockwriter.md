---
description: Implementación de IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Implementación de IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467932"
---
# <a name="implementing-iwicmetadatablockwriter"></a>Implementación de IWICMetadataBlockWriter

## <a name="iwicmetadatablockwriter"></a>IWICMetadataBlockWriter

-   [InitializeFromBlockReader](#initializefromblockreader)
-   [GetWriterByIndex](#getwriterbyindex)
-   [AddWriter](#addwriter)
-   [SetWriterByIndex](#setwriterbyindex)
-   [RemoveWriterByIndex](#removewriterbyindex)

La clase de codificación de nivel de marco implementa esta interfaz para exponer todos los bloques de metadatos y solicitar el escritor de metadatos adecuado para cada bloque. Si el formato de imagen admite metadatos globales, fuera de cualquier fotograma individual, también debe implementar esta interfaz en la clase de codificador de nivel de contenedor. Para obtener una explicación más detallada de los controladores de metadatos, consulte la sección sobre [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) en la sección Sobre la implementación de un descodificador de WIC-Enabled.

``` syntax
interface IWICMetadataBlockWriter : IWICMetadataBlockReader
{
   // All methods required
   HRESULT InitializeFromBlockReader ( IWICMetadataBlockReader *pIMDBlockReader );
   HRESULT GetWriterByIndex ( UINT nIndex, IWICMetadataWriter **ppIMetadataWriter );
   HRESULT AddWriter (IWICMetadataWriter *pIMetadataWriter );
   HRESULT SetWriterByIndex ( UINT nIndex, IWICMetadataWriter *pIMetadataWriter );
   HRESULT RemoveWriterByIndex ( UINT nIndex );
}
```

### <a name="initializefromblockreader"></a>InitializeFromBlockReader

[**InitializeFromBlockReader usa**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) [**IWICMetadataBlockReader para**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) inicializar el escritor de bloques. Puede obtener **IWICMetadataBlockReader desde** el descodificador que descodificó la imagen.


```C++
UINT blockCount = 0;
IWICMetadataReader* pMetadataReader = NULL;
IWICMetadataWriter** ppMetadataWriter = NULL;
HRESULT hr;

hr = m_pBlockReader->GetCount(&blockCount);
ppMetadataWriter = IWICMetadataWriter*[blockCount];

for (UINT x=0; x < blockCount; x++)
{
   hr = m_pBlockReader->GetReaderByIndex(&pMetadataReader);
   hr = m_pComponentFactory->CreateMetadataWriterFromReader(
         pMetadataReader, NULL, &ppMetadataWriter[x]);
}
```



Dado que al inicializar [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) con [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) se crea una instancia de un escritor de metadatos para cada lector de metadatos expuesto por el objeto **IWICMetadataBlockReader,** la aplicación no tiene que solicitar explícitamente un escritor para cada bloque de metadatos.

### <a name="getwriterbyindex"></a>GetWriterByIndex

[**GetWriterByIndex devuelve**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) el [**objeto IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) para el enésimo bloque de metadatos, donde n es el valor pasado en el *parámetro nIndex.* Si no hay ningún escritor de metadatos registrado que pueda controlar el tipo de metadatos en el enésimo bloque, el generador de componentes devolverá el controlador de metadatos desconocido, que tratará el bloque de metadatos como un objeto binario grande (BLOB). La serializará como una secuencia de bits sin intentar analizarla.

### <a name="addwriter"></a>AddWriter

[**AddWriter permite**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) que un autor de la llamada agregue un nuevo escritor de metadatos. Esto es necesario si una aplicación desea agregar metadatos de un formato diferente al de cualquiera de los bloques de metadatos existentes. Por ejemplo, una aplicación puede querer agregar algunos metadatos XMP. Si no hay ningún bloque de metadatos XMP existente, la aplicación debe crear una instancia de un escritor de metadatos XMP y usar el **método AddWriter** para incluirlo en la colección de escritores de metadatos.

### <a name="setwriterbyindex"></a>SetWriterByIndex

[**SetWriterByIndex se**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) usa para agregar un escritor de metadatos en un índice específico de la colección. Si actualmente existe un escritor de metadatos en ese índice, el nuevo debe reemplazarlo.

### <a name="removewriterbyindex"></a>RemoveWriterByIndex

[**RemoveWriterByIndex se**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) usa para quitar un escritor de metadatos de la colección.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Implementación de IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[Instalación y registro de CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



