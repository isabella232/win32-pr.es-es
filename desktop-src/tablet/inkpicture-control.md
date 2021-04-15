---
description: Tema de referencia sobre el control InkPicture para Tablet PC.
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: InkPicture (control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded5295d48e4bb14b3c0d83713f33939a360cff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668391"
---
# <a name="inkpicture-control"></a>InkPicture (control)

El control [InkPicture](inkpicture-control-reference.md) le permite colocar una imagen (formato. jpg,. bmp,. png o. gif) en una aplicación a la que los usuarios pueden agregar tinta. Está diseñado para escenarios en los que no es necesario reconocer la tinta como texto, sino que se almacena como entrada de lápiz.

Los usuarios agregan tinta a una capa transparente con un lápiz. Los usuarios pueden cambiar el tamaño de una ventana de [InkPicture](inkpicture-control-reference.md) sin perder ninguna información de la tinta, incluso si se recorta la tinta al cambiar el tamaño.

El control [InkPicture](inkpicture-control-reference.md) incluye compatibilidad básica con la impresión. sin embargo, depende de usted implementar la vista previa de impresión u otras capacidades de impresión avanzadas.

La implementación administrada (.NET Framework) de [InkPicture](/previous-versions/ms583740(v=vs.100)) hereda de la clase [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) .

De forma predeterminada, la tinta está coloreada en negro Si no está en modo de contraste alto; de lo contrario, se establece en el valor de la configuración de color del sistema actual (COLOR \_ WINDOWTEXT). Además, de forma predeterminada, [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) es **false**.

En el control [InkPicture](inkpicture-control-reference.md) , use el objeto de [**entrada manuscrita**](inkdisp-class.md) para cargar y guardar la entrada manuscrita.

> [!Note]  
> Cuando se establece [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) en **Delete** o **Select**, se desencadenan otros eventos (como el evento [**Stroke**](inkpicture-stroke.md) ). Estos eventos son útiles si desea implementar sus propios modos de eliminación o selección.

 

Para obtener información de referencia detallada sobre el control [InkPicture](inkpicture-control-reference.md) , vea InkPicture.

En las secciones siguientes se detalla el uso del control [InkPicture](inkpicture-control-reference.md) :

-   [Trabajar con imágenes](working-with-pictures.md)
-   [Usar InkPicture en versiones anteriores de Windows](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
