---
title: Asistente para impresión de fotos
description: El Asistente para impresión de fotos ayuda a los usuarios a imprimir fotos al proporcionar una interfaz de asistente fácil de usar.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Asistente para impresión de fotos
- IDropTarget,Asistente para impresión de fotos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708f051f658739cebd08e4f8643e5dd7fc0c6f7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168258"
---
# <a name="photo-printing-wizard"></a>Asistente para impresión de fotos

El Asistente para impresión de fotos ayuda a los usuarios a imprimir fotos al proporcionar una interfaz de asistente fácil de usar. El asistente permite al usuario especificar tamaños de impresión de fotos y otras opciones de impresión y, a continuación, envía las fotos a la impresora. El asistente está diseñado para que cualquier aplicación que quiera ofrecer a los usuarios la capacidad de imprimir fotos y especificar el tamaño y otras opciones de impresión pueda invocarlo mediante programación. El Asistente para impresión de fotos está disponible en Windows XP y Windows Vista.

-   [Características proporcionadas por el Asistente para impresión de fotos](#features-provided-by-the-photo-print-wizard)
-   [Formatos de archivo de fotos admitidos](#supported-photo-file-formats)
-   [Iniciar el Asistente para impresión de fotos mediante programación](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a>Características proporcionadas por el Asistente para impresión de fotos

El Asistente para impresión de fotos ofrece varias opciones que pueden no estar disponibles en cuadros de diálogo de impresora comunes, como plantillas de varios diseños con dimensiones precisas. Las plantillas de diseño permiten a los usuarios hacer el uso más eficaz del espacio disponible en papel de impresión gráfica. Otras opciones a las que se puede especificar o acceder a través del Asistente para impresión de fotos incluyen:

-   Seleccionar una impresora de una lista de impresoras disponibles o destinos de impresión virtual (por ejemplo, Escritor de documentos XPS de Microsoft). En Windows Vista, pueden estar disponibles las siguientes opciones, en función de las funcionalidades de la impresora o el destino de impresión virtual:
    -   Tamaño del papel. Por ejemplo, "Letter", "Legal", "A3".
    -   Calidad de impresión, en términos de resoluciones de puntos por pulgada (ppp) admitidas.
    -   Tipo de papel. Por ejemplo, "Plain" o "Glossy".
-   Iniciar las preferencias de impresión y las propiedades de una impresora determinada.
-   Establecer las **copias de cada** imagen (en Windows Vista) o número de veces para usar cada imagen (en Windows XP) valores de cuadro de número. 
-   Especificar una plantilla de diseño de impresión. Por ejemplo, **la foto de página completa** o Wallet **imprime**.
-   Selección de la **opción Ajustar imagen a marco** (disponible solo Windows Vista).
-   Vista previa de la foto impresa con las opciones especificadas actualmente.
-   Acceso a las opciones de impresión avanzadas, como **Ajuste para impresión** y **Administración** de colores (disponible solo Windows Vista).

Cualquier aplicación puede beneficiarse de las características y la funcionalidad de impresión de fotos que ofrece el Asistente para impresión de fotos. Una aplicación puede pasar los archivos que se imprimirán. A continuación, el Asistente para impresión de fotos se encarga de preparar el archivo para imprimirlo en función de las opciones especificadas por el usuario y envía los archivos preparados a la impresora.

En la ilustración siguiente se muestra la interfaz del Asistente para impresión de fotos Windows Vista

![El Asistente para impresión de fotos en Windows Vista](images/ppw-vista.png)

En la ilustración siguiente se muestra la interfaz del Asistente para impresión de fotos Windows XP

![El Asistente para impresión de fotos en Windows XP](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a>Formatos de archivo de fotos admitidos

En Windows XP, el Asistente para impresión de fotos admite todos los formatos de archivo de gráficos compatibles con Windows GDI+. Actualmente, estos formatos de archivo incluyen:

-   Mapa de bits (BMP)
-   Formato de intercambio de gráficos (GIF)
-   Formato JPEG (Joint Photographic Experts Group)
-   Archivo de imagen intercambiable (EXIF)
-   Formato PNG (Portable Network Graphics)
-   Tagged Image File Format (TIFF)

Para obtener más información sobre los formatos de archivo de gráficos GDI+, vea [Tipos de mapas de bits.](../gdiplus/-gdiplus-types-of-bitmaps-about.md)

En Windows Vista, el Asistente para impresión de fotos admite cualquier formato de archivo de imagen para el que esté instalado un códec Windows Imaging Component (WIC). WIC proporciona varios códecs estándar, entre los que se incluyen:

-   Mapa de bits (BMP)
-   GIF
-   Formato de icono (ICO)
-   JPEG
-   PNG
-   TIFF
-   Windows Formato de foto multimedia

Para obtener más información sobre los códecs WIC y WIC, vea Windows Imaging Component (Componente [de creación de imágenes).](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)

## <a name="programmatically-launching-the-photo-print-wizard"></a>Iniciar el Asistente para impresión de fotos mediante programación

Para invocar al Asistente para impresión de fotos, llame a la [interfaz IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) con el siguiente identificador de clase (CLSID):


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



Los archivos que va a procesar el Asistente para impresión de fotos se especifican en un [objeto IDataObject.](/windows/win32/api/objidl/nn-objidl-idataobject)

En el ejemplo de código siguiente se muestra cómo invocar el Asistente para impresión de fotos.


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
            
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PrintPhotosDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



 

 