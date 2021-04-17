---
description: La clave del registro EUDCCodeRange define los intervalos de código del carácter definido por el usuario final (EUDC) para varias páginas de códigos (juegos de caracteres).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e68c71751ca5d13cd04c95ff66c84067fd1d46d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688339"
---
# <a name="eudccoderange"></a>EUDCCodeRange

La clave del registro EUDCCodeRange define los intervalos de código del [carácter definido por el usuario final (EUDC)](end-user-defined-characters.md) para varias páginas de códigos (juegos de caracteres). Solo se usa en las herramientas que crean EUDCs y no es de interés directo para los usuarios de EUDC. Esta clave del registro tiene la siguiente ubicación del registro:

HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ NLS \\ CodePage \\ EUDCCodeRange

El formato es:

EUDCCodeRange CodePage = Fromto \[ , fromto\]

donde:



|          |                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CodePage | Una de las cadenas "932" (japonés), "936" (Chino Simplificado), "949" (Coreano), "950" (chino tradicional) o "Unicode" (Unicode). No se admiten otros valores.                                     |
| Fromto   | Valor de cadena que consta de un par de valores hexadecimales de 4 dígitos separados por un guión (-). Se pueden especificar hasta cuatro valores de a, pero cada uno debe estar separado del valor anterior por una coma (,). |



 

A continuación se muestran los valores correctos para la entrada del registro.


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Entradas del registro de EUDC](eudc-registry-entries.md)
</dt> <dt>

[EUDC](eudc.md)
</dt> </dl>

 

 



