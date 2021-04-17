---
description: Crea un archivo de catálogo sin firmar, que contiene los valores hash de un conjunto de archivos junto con los atributos asociados de cada archivo del conjunto. Un archivo de catálogo permite al usuario firmar un archivo (el catálogo) en lugar de firmar numerosos archivos individuales.
ms.assetid: 0a6ce2cd-db1f-4b47-990c-36fa87c28a60
title: Usar MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36c83531df38b95bde03edd719d98be325dbeac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687075"
---
# <a name="using-makecat"></a>Usar MakeCat

La herramienta [MakeCat](makecat.md) crea un archivo de catálogo sin firmar, que contiene los [*valores hash*](../secgloss/h-gly.md) de un conjunto de archivos junto con los atributos asociados de cada archivo del conjunto. Un archivo de catálogo permite al usuario firmar un archivo (el catálogo) en lugar de firmar numerosos archivos individuales.

Una vez firmado y transmitido el archivo de catálogo sin firmar, el receptor puede comparar los valores hash de los archivos originales con los valores hash contenidos en el archivo de catálogo y comprobar que los archivos no están alterados.

Antes de usar la herramienta [MakeCat](makecat.md) , el usuario debe preparar un archivo de definición de catálogo (. CDF) mediante cualquier editor de texto. El archivo. CDF contiene la lista de archivos y los atributos de los archivos que se van a catalogar (las especificaciones se enumeran a continuación). La herramienta MakeCat examina el archivo. CDF, comprueba la lista de atributos de cada archivo de la lista, agrega los atributos enumerados al propio catálogo, aplica un algoritmo hash a cada uno de los archivos enumerados y almacena los valores hash de cada archivo en el archivo de catálogo. Cada archivo tiene su hash y sus atributos almacenados por separado en el catálogo. Este archivo de catálogo se puede firmar y transmitir. Posteriormente, el receptor puede comparar el hash de cada archivo del catálogo con el hash de los archivos originales para demostrar que el contenido original no está alterado. MakeCat no modifica el archivo. CDF.

En los ejemplos siguientes se usan comandos [MakeCat](makecat.md) .

-   Genere un archivo de catálogo a partir del archivo Good. CDF.

    **MakeCat-v Good. CDF**

Un archivo, Good. CDF, genera un archivo de catálogo, Good.cat, mediante el análisis de los archivos UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, Unsigned. Class y SignedPE.exe. Los archivos analizados, junto con Good. CDF y los Good.cat recién generados, se encuentran en el mismo directorio.

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
> La última entrada del archivo. CDF siempre debe tener un carácter de nueva línea explícito al final de la línea.

 

 

 
