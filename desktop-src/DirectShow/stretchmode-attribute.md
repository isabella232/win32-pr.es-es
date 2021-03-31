---
description: El atributo stretchmode especifica cómo ajustar una imagen que no coincide con las dimensiones de salida.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: Atributo stretchmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a629a34dc1875a7f1d3669e32c53d0e8d3d29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911702"
---
# <a name="stretchmode-attribute"></a>Atributo stretchmode

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `stretchmode` atributo especifica cómo ajustar una imagen que no coincide con las dimensiones de salida.

## <a name="possible-values"></a>Valores posibles

Debe tener uno de los valores siguientes.

-   "stretch": la imagen se ajusta para ajustarse al tamaño del marco de salida sin conservar la relación de aspecto. (Es el valor predeterminado).
-   "recortar": la imagen se recorta para ajustarse al tamaño del marco de salida.
-   "PreserveAspectRatio": se conserva la relación de aspecto original, con una panorámica negra a lo largo de la dimensión más corta.
-   "preserveaspectrationoletterbox": la imagen cambia de tamaño para rellenar todo el marco de destino conservando la relación de aspecto.

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



