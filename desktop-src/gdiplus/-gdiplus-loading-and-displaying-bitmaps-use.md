---
description: Para mostrar una imagen de trama (mapa de bits) en la pantalla, necesita un objeto de imagen y un objeto gráfico.
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: Cargar y mostrar mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ab2405462db5017215893d50d93dc0b228633cfb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "104987421"
---
# <a name="loading-and-displaying-bitmaps"></a>Cargar y mostrar mapas de bits

Consulte también la [aplicación de ejemplo GDI+ del visor WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).

Para mostrar una imagen de trama (mapa de bits) en la pantalla, necesita un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Pase el nombre de un archivo (o un puntero a un flujo) a un constructor de **imagen** . Después de crear un objeto de **imagen** , pase la dirección de ese objeto de **imagen** al método **DrawImage** de un objeto **Graphics** .

En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir de un archivo JPEG y, a continuación, se dibuja la imagen con la esquina superior izquierda en (60, 10):

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

En la ilustración siguiente se muestra la imagen dibujada en la ubicación especificada.

![captura de pantalla de una ventana que contiene una imagen, con una llamada para el punto de origen ](images/imageposition1.png)

La clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) proporciona métodos básicos para cargar y mostrar imágenes de trama e imágenes vectoriales. La clase [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) , que hereda de la clase **Image** , proporciona métodos más especializados para cargar, mostrar y manipular imágenes de tramas. Por ejemplo, puede crear un objeto de **mapa de bits** a partir de un identificador de icono (HICON).

En el ejemplo siguiente se obtiene un identificador de un icono y, a continuación, se usa ese identificador para construir un objeto de [**mapa de bits**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) . El código muestra el icono pasando la dirección del objeto de **mapa de bits** al método **DrawImage** de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a>Vea también

[Aplicación de ejemplo GDI+ del visor WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
