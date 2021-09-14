---
title: Scripts de valores separados por comas (CSV)
description: Windows 2000 incluye una utilidad de línea de comandos, CSVDE, para importar objetos de directorio mediante archivos .csv y exportar objetos de directorio como .csv archivos.
ms.assetid: fda242eb-7561-444f-b560-94bd87fe4e39
ms.tgt_platform: multiple
keywords:
- Scripts de valores separados por comas ad
- Scripts, valores separados por comas de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec737f971bd7e462b8f6f0ef6e9e3df786a207cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160370"
---
# <a name="comma-separated-value-csv-scripts"></a>Scripts de valores separados por comas (CSV)

Windows 2000 incluye una utilidad de línea de comandos, CSVDE, para importar objetos de directorio mediante archivos .csv y exportar objetos de directorio como .csv archivos. Los scripts CSV se crean para facilitar su uso. La primera línea del script identifica los atributos de las líneas siguientes. Las columnas están separadas por comas. El formato de archivo es compatible con el Microsoft Excel .csv, por lo que los archivos se crean fácilmente. Use Excel o cualquier otra herramienta que pueda leer y escribir .csv archivos. CSVDE admite Unicode.

## <a name="example-csv-file"></a>Archivo CSV de ejemplo

El ejemplo de código siguiente es un archivo CSV que agrega una clase auxiliar.

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




