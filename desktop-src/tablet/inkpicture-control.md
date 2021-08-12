---
description: Tema de referencia del control InkPicture para tablet PC.
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: InkPicture Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef9cb4b5e1919e111e84cc6b654b56b14eff93cfb5aedacc15400fb3ef1af07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451104"
---
# <a name="inkpicture-control"></a>InkPicture Control

El control [InkPicture](inkpicture-control-reference.md) permite colocar una imagen (formato .jpg, .bmp, .png o .gif) en una aplicación a la que los usuarios pueden agregar entrada de lápiz. Está pensado para escenarios en los que no es necesario reconocer la entrada de lápiz como texto, sino que se almacena como entrada de lápiz.

Los usuarios agregan entrada de lápiz a una capa transparente mediante un lápiz. Los usuarios pueden cambiar el tamaño de una [ventana InkPicture](inkpicture-control-reference.md) sin perder ninguna información de entrada de lápiz, incluso si la entrada de lápiz se recorta al cambiar el tamaño.

El [control InkPicture](inkpicture-control-reference.md) incluye compatibilidad básica con la impresión; sin embargo, es usted el que tiene que implementar la vista previa de impresión u otras funcionalidades avanzadas de impresión.

La implementación administrada (.NET Framework) de [InkPicture](/previous-versions/ms583740(v=vs.100)) hereda de la [clase PictureBox.](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1)

De forma predeterminada, la entrada de lápiz se coloreó en negro si no está en modo de contraste alto; de lo contrario, se establece en el valor de configuración de color del sistema actual (COLOR \_ WINDOWTEXT). Además, de forma [**predeterminada FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) es **FALSE.**

En el control [InkPicture,](inkpicture-control-reference.md) use el [**objeto Ink**](inkdisp-class.md) para cargar y guardar la entrada de lápiz.

> [!Note]  
> Al establecer [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) en **Eliminar** o **Seleccionar**, se desencadenan otros eventos (como el [**evento Stroke).**](inkpicture-stroke.md) Estos eventos son útiles si desea implementar sus propios modos de eliminación o selección.

 

Para obtener información de referencia detallada sobre el control [InkPicture,](inkpicture-control-reference.md) vea InkPicture.

En las secciones siguientes se detalla el uso del control [InkPicture:](inkpicture-control-reference.md)

-   [Trabajar con imágenes](working-with-pictures.md)
-   [Uso de InkPicture en versiones anteriores de Windows](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
