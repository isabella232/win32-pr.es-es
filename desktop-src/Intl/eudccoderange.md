---
description: La clave del Registro EUDCCodeRange define intervalos de código de caracteres definidos por el usuario final (EUDC) para varias páginas de códigos (juegos de caracteres).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20dad72012a15f6f9b9d6db29d9dfea50b4dbf4068588f679b26b144f63036a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068235"
---
# <a name="eudccoderange"></a>EUDCCodeRange

La clave del Registro EUDCCodeRange define intervalos de código de caracteres definidos por el usuario final [(EUDC)](end-user-defined-characters.md) para varias páginas de códigos (juegos de caracteres). Solo la usan las herramientas que crean EUDC y no es una preocupación directa para los usuarios de EUDC. Esta clave del Registro tiene la siguiente ubicación del Registro:

HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ NLS \\ CodePage \\ EUDCCodeRange

El formato es:

EUDCCodeRange CodePage=FromTo \[ ,FromTo\]

donde:



| Value         | Descripción                                                                                                                                                                                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CodePage | Una de las cadenas "932" (japonés), "936" (chino simplificado), "949" (coreano), "950" (chino tradicional) o "Unicode" (Unicode). No se admiten otros valores.                                     |
| FromTo   | Valor de cadena que consta de un par de valores hexadecimales de 4 dígitos separados por un guion (-). Se pueden especificar hasta cuatro valores FromTo, pero cada uno debe separarse del valor anterior mediante una coma (,). |



 

Los siguientes son los valores correctos para la entrada del Registro.


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Entradas del Registro eudc](eudc-registry-entries.md)
</dt> <dt>

[EUDC](eudc.md)
</dt> </dl>

 

 



