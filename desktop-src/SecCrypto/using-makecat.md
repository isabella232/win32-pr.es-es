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
# <a name="using-makecat"></a><span data-ttu-id="a7c5e-104">Usar MakeCat</span><span class="sxs-lookup"><span data-stu-id="a7c5e-104">Using MakeCat</span></span>

<span data-ttu-id="a7c5e-105">La herramienta [MakeCat](makecat.md) crea un archivo de catálogo sin firmar, que contiene los [*valores hash*](../secgloss/h-gly.md) de un conjunto de archivos junto con los atributos asociados de cada archivo del conjunto.</span><span class="sxs-lookup"><span data-stu-id="a7c5e-105">The [MakeCat](makecat.md) tool makes an unsigned catalog file, which contains the [*hashes*](../secgloss/h-gly.md) of a set of files along with associated attributes of each file in the set.</span></span> <span data-ttu-id="a7c5e-106">Un archivo de catálogo permite al usuario firmar un archivo (el catálogo) en lugar de firmar numerosos archivos individuales.</span><span class="sxs-lookup"><span data-stu-id="a7c5e-106">A catalog file allows the user to sign one file (the catalog) instead of signing numerous individual files.</span></span>

<span data-ttu-id="a7c5e-107">Una vez firmado y transmitido el archivo de catálogo sin firmar, el receptor puede comparar los valores hash de los archivos originales con los valores hash contenidos en el archivo de catálogo y comprobar que los archivos no están alterados.</span><span class="sxs-lookup"><span data-stu-id="a7c5e-107">After the unsigned catalog file is signed and transmitted, the receiver can compare the hashes of the original files to the hashes contained within the catalog file and verify that the files are free of tampering.</span></span>

<span data-ttu-id="a7c5e-108">Antes de usar la herramienta [MakeCat](makecat.md) , el usuario debe preparar un archivo de definición de catálogo (. CDF) mediante cualquier editor de texto.</span><span class="sxs-lookup"><span data-stu-id="a7c5e-108">Prior to using the [MakeCat](makecat.md) tool, the user must prepare a Catalog Definition File (.cdf), by using any text editor.</span></span> <span data-ttu-id="a7c5e-109">El archivo. CDF contiene la lista de archivos y los atributos de los archivos que se van a catalogar (las especificaciones se enumeran a continuación).</span><span class="sxs-lookup"><span data-stu-id="a7c5e-109">The .cdf file contains the list of files and the attributes of the files to be cataloged (the specifications are listed below).</span></span> <span data-ttu-id="a7c5e-110">La herramienta MakeCat examina el archivo. CDF, comprueba la lista de atributos de cada archivo de la lista, agrega los atributos enumerados al propio catálogo, aplica un algoritmo hash a cada uno de los archivos enumerados y almacena los valores hash de cada archivo en el archivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="a7c5e-110">The MakeCat tool scans the .cdf file, verifies the list of attributes of each listed file, adds the listed attributes to the catalog itself, hashes each of the listed files, and stores the hashes of each file into the catalog file.</span></span> <span data-ttu-id="a7c5e-111">Cada archivo tiene su hash y sus atributos almacenados por separado en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="a7c5e-111">Each file has its hash and attributes stored separately within the catalog.</span></span> <span data-ttu-id="a7c5e-112">Este archivo de catálogo se puede firmar y transmitir.</span><span class="sxs-lookup"><span data-stu-id="a7c5e-112">This catalog file can then be signed and transmitted.</span></span> <span data-ttu-id="a7c5e-113">Posteriormente, el receptor puede comparar el hash de cada archivo del catálogo con el hash de los archivos originales para demostrar que el contenido original no está alterado.</span><span class="sxs-lookup"><span data-stu-id="a7c5e-113">The receiver can subsequently compare the hash of each file within the catalog with the hash of the original files to prove that the original content is free of tampering.</span></span> <span data-ttu-id="a7c5e-114">MakeCat no modifica el archivo. CDF.</span><span class="sxs-lookup"><span data-stu-id="a7c5e-114">MakeCat does not modify the .cdf file.</span></span>

<span data-ttu-id="a7c5e-115">En los ejemplos siguientes se usan comandos [MakeCat](makecat.md) .</span><span class="sxs-lookup"><span data-stu-id="a7c5e-115">The following examples use [MakeCat](makecat.md) commands.</span></span>

-   <span data-ttu-id="a7c5e-116">Genere un archivo de catálogo a partir del archivo Good. CDF.</span><span class="sxs-lookup"><span data-stu-id="a7c5e-116">Generate a catalog file from the file Good.cdf.</span></span>

    <span data-ttu-id="a7c5e-117">**MakeCat-v Good. CDF**</span><span class="sxs-lookup"><span data-stu-id="a7c5e-117">**MakeCat -v good.cdf**</span></span>

<span data-ttu-id="a7c5e-118">Un archivo, Good. CDF, genera un archivo de catálogo, Good.cat, mediante el análisis de los archivos UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, Unsigned. Class y SignedPE.exe.</span><span class="sxs-lookup"><span data-stu-id="a7c5e-118">A file, Good.cdf, produces a catalog file, Good.cat, by parsing the files UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, Unsigned.Class, and SignedPE.exe.</span></span> <span data-ttu-id="a7c5e-119">Los archivos analizados, junto con Good. CDF y los Good.cat recién generados, se encuentran en el mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="a7c5e-119">The parsed files, along with Good.cdf and the newly generated Good.cat, are all in the same directory.</span></span>

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
> <span data-ttu-id="a7c5e-120">La última entrada del archivo. CDF siempre debe tener un carácter de nueva línea explícito al final de la línea.</span><span class="sxs-lookup"><span data-stu-id="a7c5e-120">The last entry in the .cdf file must always have an explicit newline character at the end of the line.</span></span>

 

 

 
