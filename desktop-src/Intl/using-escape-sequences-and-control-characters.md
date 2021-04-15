---
description: Cuando una aplicación convierte cadenas de ASCII o de una página de códigos de Windows (ANSI) a Unicode, debe convertir las secuencias de escape carácter a carácter en Unicode.
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: Usar secuencias de escape y caracteres de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4211a487a31d5a79454d7be15159f48cdc3d5beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688701"
---
# <a name="using-escape-sequences-and-control-characters"></a>Usar secuencias de escape y caracteres de control

Cuando una aplicación convierte cadenas de ASCII o de una [Página de códigos de Windows (ANSI)](code-pages.md) a Unicode, debe convertir las secuencias de escape carácter a carácter en Unicode. Cuando se convierte un archivo de texto ASCII u otro archivo de 8 bits en Unicode, existe la posibilidad de que se convierta posteriormente. Convertir secuencias de escape en Unicode carácter a carácter, en lugar de combinarlas como un solo carácter Unicode, permite realizar la conversión inversa sin necesidad de reconocer y analizar las secuencias de escape como tal. Por ejemplo, ESC + A debe ser 0x001B (ESC), 0x0041 (A), en lugar de 0x411B.

Los primeros valores de código de 32 16 bits en Unicode están diseñados para los caracteres de control 32. Esta especificación admite el uso existente de caracteres de control para la aplicación de formato. Las aplicaciones Unicode pueden tratar estos caracteres de control exactamente de la misma manera que tratan sus equivalentes ASCII.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar caracteres especiales en Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



