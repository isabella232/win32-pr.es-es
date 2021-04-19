---
description: El componente de creación de imágenes de Windows (WIC) proporciona una API basada en el modelo de objetos componentes (COM) para su uso en C y C++.
ms.assetid: 74b14b5e-70e9-410f-a6e6-d8873a5f4fa4
title: Información general sobre la API WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86e5a876010e52489adac9baa7ce57fdfdf80f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720566"
---
# <a name="wic-api-overview"></a>Información general sobre la API WIC

El componente de creación de imágenes de Windows (WIC) proporciona una API basada en el modelo de objetos componentes (COM) para su uso en C y C++. La API de WIC expone una variedad de funcionalidades relacionadas con la imagen, entre las que se incluyen:

-   Códecs integrados para los formatos de imagen web estándar.
-   Compatibilidad integrada con formatos de metadatos estándar.
-   Gran variedad de compatibilidad con el formato de píxeles.
-   Compatibilidad de alto color; incluye formatos de intervalo extendido de 30 bits, alta precisión de 30 bits y alta precisión de 48 bits y de gama ancha.
-   Marco extensible para códecs de imagen, formatos de píxeles y formatos de metadatos.

Este tema contiene los temas siguientes.

-   [Archivos de encabezado WIC](#wic-header-files)
-   [Archivos de biblioteca](#library-files)
-   [Generadores de clases](#class-factories)
-   [Componentes de creación de imágenes](#imaging-components)
-   [Vea también](#see-also)

## <a name="wic-header-files"></a>Archivos de encabezado WIC

Las API de WIC se definen en los siguientes archivos de encabezado y de lenguaje de definición de interfaz (IDL):



| Archivo              | Descripción                                          |
|-------------------|------------------------------------------------------|
| wincodec. h        | Define las versiones de C y C++ de las API de WIC principales.  |
| wincodec. idl      | Define las interfaces de WIC principales.                  |
| wincodecsdk. h     | Define las versiones de C y C++ de las API de WIC de metadatos. |
| wincodecsdk. idl   | Define las interfaces de metadatos de WIC.                 |
| wincodec \_ proxy. h | Define las exportaciones del proxy WIC.                       |



 

Para usar WIC, las aplicaciones deben incluir wincodec. h y/o wincodecsdk. h, en función de la API que necesite la aplicación.

## <a name="library-files"></a>Archivos de biblioteca

Archivos de la biblioteca WIC:



| Archivo              | Descripción                                                            |
|-------------------|------------------------------------------------------------------------|
| WindowsCodecs. lib | Biblioteca de importación proporcionada por el kit de desarrollo de software (SDK) de Windows. |
| windowscodecs.dll | Biblioteca de implementación de acciones proporcionada por el sistema operativo.         |



 

Para vincular a las API de WIC, la aplicación debe incluir windowscodec. lib como una dependencia del enlazador adicional.

## <a name="class-factories"></a>Generadores de clases

En la tabla siguiente se describen los dos generadores de clases COM que las API de WIC proporcionan para crear componentes de WIC.



| Interfaz de fábrica                                               | Descripción                                                                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)     | Generador de clases principal para el desarrollo de aplicaciones mediante componentes de WIC. Este generador crea componentes como descodificadores de imágenes, codificadores y secuencias.   |
| [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) | Generador de clases destinado a desarrolladores de componentes de WIC. Los componentes creados a partir de este generador se utilizan principalmente en el desarrollo de códecs y controladores de metadatos. |



 

Para crear un generador de clases, utilice la función com [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) . En el ejemplo siguiente se muestra la creación de la factoría de imágenes WIC.


```C++
// Initialize COM
CoInitialize(NULL);

// The factory pointer
IWICImagingFactory *pFactory = NULL;

// Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&pFactory)
);
```



## <a name="imaging-components"></a>Componentes de creación de imágenes

Las API de WIC proporcionan varios tipos de componentes de creación de imágenes. En la tabla siguiente se describen algunos de los componentes de WIC comunes. Para obtener una lista completa de los componentes disponibles, consulte [interfaces de WIC](-wic-codec-ifaces.md).



| Tipo de componente                                                      | Descripción                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**Bitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                             | Representa una representación en memoria grabable de un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource). |
| [**Descodificador**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)                     | Se usa para descodificar los datos de imagen de una secuencia en un formato útil para el procesamiento de imágenes.                    |
| [**Codificador**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)                     | Escribe datos de imagen en una secuencia.                                                                                |
| [**Stream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)                             | Se usa para leer y escribir datos de un archivo, un recurso de red, un bloque de memoria, etc.                      |
| [**Convertidor de formato**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)          | Se utiliza para convertir de un formato de píxel a otro.                                                             |
| [**Lector de consultas de metadatos**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) | Se usa para leer los metadatos de un marco de imagen o imagen.                                                             |
| [**Escritor de consultas de metadatos**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) | Se usa para escribir metadatos en un marco de imagen o imagen.                                                            |



 

## <a name="see-also"></a>Consulte también

[Referencias](-wic-codec-reference.md)


[Ejemplos y ejemplos de código](-wic-samples.md)


 

 
