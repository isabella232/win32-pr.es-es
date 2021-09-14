---
description: Cuando una aplicación convierte cadenas de ASCII o de una página de códigos Windows (ANSI) a Unicode, debe traducir secuencias de escape carácter a carácter en Unicode.
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: Usar secuencias de escape y caracteres de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4211a487a31d5a79454d7be15159f48cdc3d5beb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254889"
---
# <a name="using-escape-sequences-and-control-characters"></a>Usar secuencias de escape y caracteres de control

Cuando una aplicación convierte cadenas de ASCII o de una página de códigos [Windows (ANSI)](code-pages.md) a Unicode, debe traducir secuencias de escape carácter a carácter en Unicode. Cuando un archivo de texto ASCII u otro archivo de texto de 8 bits se convierte en Unicode, existe la posibilidad de que posteriormente se vuelva a convertir. La conversión de secuencias de escape en Unicode por carácter, en lugar de combinarlas como un único carácter Unicode, permite realizar la conversión inversa sin necesidad de reconocer y analizar las secuencias de escape como tales. Por ejemplo, ESC+A debe convertirse en 0x001B (ESC), 0x0041 (A), en lugar de 0x411B.

Los primeros 32 valores de código de 16 bits en Unicode están diseñados para los 32 caracteres de control. Esta especificación admite el uso existente de caracteres de control con fines de formato. Las aplicaciones Unicode pueden tratar estos caracteres de control exactamente de la misma manera que tratan sus equivalentes ASCII.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar caracteres especiales en Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



