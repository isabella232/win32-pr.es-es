---
description: El atributo stretchmode especifica cómo extender una imagen que no coincide con las dimensiones de salida.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: Atributo stretchmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed398fbe193ef262bdfc9a28cf66bef3a5b11f759d90c460cc99342ec7cd66b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903875"
---
# <a name="stretchmode-attribute"></a>Atributo stretchmode

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `stretchmode` atributo especifica cómo extender una imagen que no coincide con las dimensiones de salida.

## <a name="possible-values"></a>Valores posibles

Debe tener uno de los siguientes valores.

-   "stretch": la imagen se ajusta para ajustarse al tamaño del marco de salida sin conservar la relación de aspecto. (Es el valor predeterminado).
-   "crop": la imagen se recorta para ajustarse al tamaño del marco de salida.
-   "preserveaspectratio": se conserva la relación de aspecto original, con un cuadro de letras negro a lo largo de la dimensión más corta.
-   "preserveaspectrationoletterbox": se cambia el tamaño de la imagen para rellenar todo el marco de destino a la vez que se conserva la relación de aspecto.

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



