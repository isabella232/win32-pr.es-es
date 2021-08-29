---
description: Crea un archivo de catálogo sin signo, que contiene los valores hash de un conjunto de archivos junto con los atributos asociados de cada archivo del conjunto. Un archivo de catálogo permite al usuario firmar un archivo (el catálogo) en lugar de firmar numerosos archivos individuales.
ms.assetid: 0a6ce2cd-db1f-4b47-990c-36fa87c28a60
title: Uso de MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abfc2da9bbff53af48cb21a6f60c2373885ba271f8965705dc991b78f4b4d25b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896789"
---
# <a name="using-makecat"></a>Uso de MakeCat

La [herramienta MakeCat](makecat.md) crea un archivo de catálogo sin signo, que contiene los [*hashes*](../secgloss/h-gly.md) de un conjunto de archivos junto con los atributos asociados de cada archivo del conjunto. Un archivo de catálogo permite al usuario firmar un archivo (el catálogo) en lugar de firmar numerosos archivos individuales.

Una vez firmado y transmitido el archivo de catálogo sin firmar, el receptor puede comparar los hashes de los archivos originales con los hashes contenidos en el archivo de catálogo y comprobar que los archivos no están manipulados.

Antes de usar la [herramienta MakeCat,](makecat.md) el usuario debe preparar un archivo de definición de catálogo (.cdf) mediante cualquier editor de texto. El archivo .cdf contiene la lista de archivos y los atributos de los archivos que se van a catalogar (las especificaciones se enumeran a continuación). La herramienta MakeCat examina el archivo .cdf, comprueba la lista de atributos de cada archivo enumerado, agrega los atributos enumerados al propio catálogo, aplica un algoritmo hash a cada uno de los archivos enumerados y almacena los hashes de cada archivo en el archivo de catálogo. Cada archivo tiene sus hash y atributos almacenados por separado dentro del catálogo. Este archivo de catálogo se puede firmar y transmitir. Posteriormente, el receptor puede comparar el hash de cada archivo del catálogo con el hash de los archivos originales para demostrar que el contenido original no está manipulado. MakeCat no modifica el archivo .cdf.

En los ejemplos siguientes se [usan comandos MakeCat.](makecat.md)

-   Genere un archivo de catálogo a partir del archivo Good.cdf.

    **MakeCat -v good.cdf**

Un archivo, Good.cdf, genera un archivo de catálogo, Good.cat, analizando los archivos UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, Unsigned.Class y SignedPE.exe. Los archivos analizados, junto con Good.cdf y los archivos recién Good.cat, están todos en el mismo directorio.

``` syntax
[CatalogHeader]
Name=Good.cat
ResultDir=.\
PublicVersion=0x00000001
EncodingType=
CATATTR1=0x10010001:Movie1:FirstMovie
CATATTR2=0x10010001:Movie2:SecondMovie
CATATTR3=0x10010001:Movie3:ThirdMovie

[CatalogFiles]
UnsignedPE=.\UnsignedPE.EXE
UnsignedDOS=.\UnsignedDOS.EXE
<HASH>UnsignedCAB=.\Unsigned.CAB
UnsignedClass=.\Unsigned.Class
SignedPE=.\SignedPE.EXE
```

> [!Note]  
> La última entrada del archivo .cdf siempre debe tener un carácter de nueva línea explícito al final de la línea.

 

 

 
