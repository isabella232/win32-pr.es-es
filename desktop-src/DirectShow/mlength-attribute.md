---
description: El atributo mlength especifica la duración de un archivo de código fuente. Este valor debe ser la duración real o pueden producirse errores de representación.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: Atributo mlength
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eadc288e29d99df0e6af7f06e1404d86f6a938
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173762"
---
# <a name="mlength-attribute"></a>Atributo mlength

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `mlength` atributo especifica la duración de un archivo de código fuente. Este valor debe ser la duración real o pueden producirse errores de representación.

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md)

## <a name="possible-values"></a>Valores posibles

Debe ser una cadena con el formato *hh:mm:ss.ff,* donde *hh* = hours, *mm* = minutes, *ss* = seconds y *ff* = fractions of seconds. Ejemplo: 1:04:30.512. Se pueden omitir las unidades iniciales. Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



