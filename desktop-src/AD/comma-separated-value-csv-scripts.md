---
title: Scripts de valores separados por comas (CSV)
description: Windows 2000 incluye una utilidad de línea de comandos, CSVDE, para importar objetos de directorio mediante archivos. csv y exportar objetos de directorio como archivos. csv.
ms.assetid: fda242eb-7561-444f-b560-94bd87fe4e39
ms.tgt_platform: multiple
keywords:
- Scripts de valores separados por comas AD
- Scripts, anuncio de valor separado por comas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec737f971bd7e462b8f6f0ef6e9e3df786a207cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772738"
---
# <a name="comma-separated-value-csv-scripts"></a><span data-ttu-id="93e8a-105">Scripts de valores separados por comas (CSV)</span><span class="sxs-lookup"><span data-stu-id="93e8a-105">Comma-separated Value (CSV) Scripts</span></span>

<span data-ttu-id="93e8a-106">Windows 2000 incluye una utilidad de línea de comandos, CSVDE, para importar objetos de directorio mediante archivos. csv y exportar objetos de directorio como archivos. csv.</span><span class="sxs-lookup"><span data-stu-id="93e8a-106">Windows 2000 includes a command-line utility, CSVDE, to import directory objects using .csv files and export directory objects as .csv files.</span></span> <span data-ttu-id="93e8a-107">Los scripts CSV se crean para facilitar su uso.</span><span class="sxs-lookup"><span data-stu-id="93e8a-107">CSV scripts are created for ease-of-use.</span></span> <span data-ttu-id="93e8a-108">La primera línea del script identifica los atributos de las líneas siguientes.</span><span class="sxs-lookup"><span data-stu-id="93e8a-108">The first line in the script identifies the attributes in the lines that follow.</span></span> <span data-ttu-id="93e8a-109">Las columnas se separan mediante comas.</span><span class="sxs-lookup"><span data-stu-id="93e8a-109">Columns are separated by commas.</span></span> <span data-ttu-id="93e8a-110">El formato de archivo es compatible con el formato de Microsoft Excel. csv, por lo que los archivos se crean fácilmente.</span><span class="sxs-lookup"><span data-stu-id="93e8a-110">The file format is compatible with the Microsoft Excel .csv format, so that files are easily created.</span></span> <span data-ttu-id="93e8a-111">Use Excel o cualquier otra herramienta que pueda leer y escribir archivos. csv.</span><span class="sxs-lookup"><span data-stu-id="93e8a-111">Use Excel or any other tool that can read and write .csv files.</span></span> <span data-ttu-id="93e8a-112">CSVDE es compatible con Unicode.</span><span class="sxs-lookup"><span data-stu-id="93e8a-112">CSVDE supports Unicode.</span></span>

## <a name="example-csv-file"></a><span data-ttu-id="93e8a-113">Archivo CSV de ejemplo</span><span class="sxs-lookup"><span data-stu-id="93e8a-113">Example CSV File</span></span>

<span data-ttu-id="93e8a-114">El ejemplo de código siguiente es un archivo CSV que agrega una clase auxiliar.</span><span class="sxs-lookup"><span data-stu-id="93e8a-114">The following code example is a CSV file that adds an auxiliary class.</span></span>

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




