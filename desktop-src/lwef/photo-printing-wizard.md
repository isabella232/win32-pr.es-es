---
title: Asistente para impresión fotográfica
description: El Asistente para impresión de fotografías ayuda a los usuarios a imprimir fotos proporcionando una interfaz de asistente fácil de usar.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Asistente para impresión fotográfica
- IDropTarget, Asistente para impresión fotográfica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708f051f658739cebd08e4f8643e5dd7fc0c6f7f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420690"
---
# <a name="photo-printing-wizard"></a>Asistente para impresión fotográfica

El Asistente para impresión de fotografías ayuda a los usuarios a imprimir fotos proporcionando una interfaz de asistente fácil de usar. El asistente permite al usuario especificar tamaños de impresión fotográfica y otras opciones de impresión y, a continuación, envía las fotos a la impresora. El asistente está diseñado para que se pueda invocar mediante programación por cualquier aplicación que desee ofrecer a los usuarios la posibilidad de imprimir fotografías y especificar el tamaño y otras opciones de impresión. El Asistente para impresión de fotografías está disponible en Windows XP y Windows Vista.

-   [Características proporcionadas por el Asistente para impresión fotográfica](#features-provided-by-the-photo-print-wizard)
-   [Formatos de archivo fotográfico admitidos](#supported-photo-file-formats)
-   [Inicio mediante programación del Asistente para impresión fotográfica](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a>Características proporcionadas por el Asistente para impresión fotográfica

El Asistente para impresión fotográfica ofrece varias opciones que pueden no estar disponibles en los cuadros de diálogo de impresora comunes, como las plantillas de diseño múltiple con dimensiones precisas. Las plantillas de diseño permiten a los usuarios hacer el uso más eficaz del espacio disponible en el papel de impresión fotográfica. Otras opciones que se pueden especificar o a las que se puede tener acceso a través del Asistente para impresión fotográfica incluyen:

-   Seleccionar una impresora de una lista de impresoras o destinos de impresión virtuales disponibles (por ejemplo, escritor de documentos XPS de Microsoft). En Windows Vista, pueden estar disponibles las siguientes opciones, en función de las capacidades de la impresora o del destino de impresión virtual:
    -   Tamaño del papel. Por ejemplo, "Letter", "legal", "a3".
    -   Calidad de impresión, en términos de resoluciones de puntos por pulgada (PPP) admitidas.
    -   Tipo de papel. Por ejemplo, "Plain" o "satinada".
-   Inicio de las preferencias de impresión y las propiedades de una impresora determinada.
-   Establecer las **copias de cada imagen** (en Windows Vista) o el **número de veces que se usan** los valores del cuadro de número de cada imagen (en Windows XP).
-   Especificar una plantilla de diseño de impresión. Por ejemplo, **fotos de página completa** o **impresiones de Wallet**.
-   Seleccionar la opción **ajustar la imagen al marco** (solo disponible en Windows Vista).
-   Obtener una vista previa de la foto impresa con las opciones especificadas actualmente.
-   Obtener acceso a opciones de impresión avanzadas, como **enfocar para la impresión** y la **Administración del color** (solo disponible en Windows Vista).

Cualquier aplicación puede beneficiarse de las características y la funcionalidad de impresión fotográfica que ofrece el Asistente para impresión fotográfica. Una aplicación puede pasar los archivos que se van a imprimir. A continuación, el Asistente para impresión fotográfica se encarga de preparar el archivo para imprimirlo en función de las opciones especificadas por el usuario y de enviar los archivos preparados a la impresora.

En la siguiente ilustración se muestra la interfaz del Asistente para impresión fotográfica en Windows Vista.

![el Asistente para impresión fotográfica en Windows Vista](images/ppw-vista.png)

La siguiente ilustración muestra la interfaz del Asistente para impresión de fotografías en Windows XP

![el Asistente para impresión fotográfica en Windows XP](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a>Formatos de archivo fotográfico admitidos

En Windows XP, el Asistente para impresión fotográfica admite todos los formatos de archivo de gráficos compatibles con Windows GDI+. Actualmente, estos formatos de archivo incluyen:

-   Mapa de bits (BMP)
-   Formato de intercambio de gráficos (GIF)
-   Formato JPEG (Joint Photographic Experts Group)
-   Archivo de imagen intercambiable (EXIF)
-   Formato PNG (Portable Network Graphics)
-   Tagged Image File Format (TIFF)

Para obtener más información sobre los formatos de archivo de gráficos compatibles con GDI+, vea [tipos de mapas de bits](../gdiplus/-gdiplus-types-of-bitmaps-about.md).

En Windows Vista, el Asistente para impresión fotográfica admite cualquier formato de archivo de imagen para el que esté instalado un códec de Windows Imaging Component (WIC). WIC proporciona varios códecs estándar, entre los que se incluyen:

-   Mapa de bits (BMP)
-   GIF
-   Formato de icono (ICO)
-   JPEG
-   PNG
-   TIFF
-   Formato de Windows Media Photo

Para obtener más información acerca de los códecs WIC y WIC, vea [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)

## <a name="programmatically-launching-the-photo-print-wizard"></a>Inicio mediante programación del Asistente para impresión fotográfica

Para invocar el Asistente para impresión de fotografías, llame a la interfaz [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) con el siguiente identificador de clase (CLSID):


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



Los archivos que se van a procesar mediante el Asistente para impresión fotográfica se especifican en un objeto [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .

En el ejemplo de código siguiente se muestra cómo invocar el Asistente para impresión fotográfica.


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



 

 