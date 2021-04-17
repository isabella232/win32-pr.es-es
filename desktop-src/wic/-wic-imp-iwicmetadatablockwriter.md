---
description: Implementación de IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Implementación de IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547051"
---
# <a name="implementing-iwicmetadatablockwriter"></a>Implementación de IWICMetadataBlockWriter

## <a name="iwicmetadatablockwriter"></a>IWICMetadataBlockWriter

-   [InitializeFromBlockReader](#initializefromblockreader)
-   [GetWriterByIndex](#getwriterbyindex)
-   [AddWriter](#addwriter)
-   [SetWriterByIndex](#setwriterbyindex)
-   [RemoveWriterByIndex](#removewriterbyindex)

La clase de codificación de nivel de marco implementa esta interfaz para exponer todos los bloques de metadatos y solicitar el escritor de metadatos adecuado para cada bloque. Si el formato de imagen admite metadatos globales, fuera de cualquier marco individual, también debe implementar esta interfaz en la clase de codificador de nivel de contenedor. Para obtener una explicación más detallada de los controladores de metadatos, consulte la sección sobre [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) en la sección sobre la implementación de un descodificador de WIC-Enabled.

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

[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) usa un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) para inicializar el escritor de bloque. Puede obtener el **IWICMetadataBlockReader** desde el descodificador que descodifica la imagen.


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



Dado que la inicialización de [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) con un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) crea una instancia de un escritor de metadatos para cada lector de metadatos expuesto por el objeto **iwicmetadatablockreader** , la aplicación no tiene que solicitar explícitamente un escritor para cada bloque de metadatos.

### <a name="getwriterbyindex"></a>GetWriterByIndex

[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) devuelve el objeto [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) para el bloque de metadatos nth, donde n es el valor que se pasa en el parámetro *NINDEX* . Si no hay ningún escritor de metadatos registrado que pueda controlar el tipo de metadatos en el bloque nth, el generador de componentes devolverá el controlador de metadatos desconocido, que tratará el bloque de metadatos como un objeto binario grande (BLOB). Lo serializará como un flujo de bits sin intentar analizarlo.

### <a name="addwriter"></a>AddWriter

[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) permite que un llamador agregue un nuevo escritor de metadatos. Esto es necesario si una aplicación desea agregar metadatos de un formato diferente al de cualquiera de los bloques de metadatos existentes. Por ejemplo, es posible que una aplicación desee agregar algunos metadatos XMP. Si no hay ningún bloque de metadatos XMP existente, la aplicación debe crear una instancia de un escritor de metadatos XMP y usar el método **AddWriter** para incluirlo en la colección de escritores de metadatos.

### <a name="setwriterbyindex"></a>SetWriterByIndex

[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) se utiliza para agregar un escritor de metadatos en un índice específico de la colección. Si actualmente existe un escritor de metadatos en ese índice, el nuevo debe reemplazarlo.

### <a name="removewriterbyindex"></a>RemoveWriterByIndex

[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) se utiliza para quitar un escritor de metadatos de la colección.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Implementar IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[Instalación y registro de CÓDECs](-wic-codecinstallandreg.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



