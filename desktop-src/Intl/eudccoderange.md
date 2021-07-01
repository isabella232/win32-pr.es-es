---
description: La clave del Registro EUDCCodeRange define intervalos de código de caracteres definidos por el usuario final (EUDC) para varias páginas de códigos (juegos de caracteres).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8619bce02f4ca66fa9b4ce6d25aff0c5a3e66f96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120680"
---
# <a name="eudccoderange"></a>EUDCCodeRange

La clave del Registro EUDCCodeRange define intervalos de código de caracteres definidos por el usuario final [(EUDC)](end-user-defined-characters.md) para varias páginas de códigos (juegos de caracteres). Solo lo usan herramientas que crean EUDC y no es un problema directo para los usuarios de EUDC. Esta clave del Registro tiene la siguiente ubicación del Registro:

HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ NLS \\ CodePage \\ EUDCCodeRange

El formato es:

EUDCCodeRange CodePage=FromTo \[ ,FromTo\]

donde:



| Value         | Descripción                                                                                                                                                                                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CodePage | Una de las cadenas "932" (japonés), "936" (chino simplificado), "949" (coreano), "950" (chino tradicional) o "Unicode" (Unicode). No se admite ningún otro valor.                                     |
| FromTo   | Valor de cadena que consta de un par de valores hexadecimales de 4 dígitos separados por un guion (-). Se pueden especificar hasta cuatro valores FromTo, pero cada uno debe estar separado del valor anterior por una coma (,). |



 

Estos son los valores correctos para la entrada del Registro.


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

 

 



