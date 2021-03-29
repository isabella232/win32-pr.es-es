---
description: Puede importar y exportar claves simétricas y claves asimétricas con CNG. Y puede usar la funcionalidad de importación y exportación de claves para trasladar claves entre equipos.
ms.assetid: 37bda1e0-5dd2-455c-9627-4e7e1b0e04d3
title: Importación y exportación de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be59cc5f5c4b3d1a98fa30cf4e967d5469d2f1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666218"
---
# <a name="key-import-and-export"></a>Importación y exportación de claves

Puede importar y exportar [*claves simétricas*](/windows/desktop/SecGloss/s-gly) y claves asimétricas con CNG. Y puede usar la funcionalidad de importación y exportación de claves para trasladar claves entre equipos.

## <a name="symmetric-keys"></a>Claves simétricas

Para importar o exportar claves simétricas (o de sesión) en las que se usa la misma clave para cifrar y descifrar algunos datos, puede usar las funciones [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) y [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) . Normalmente, primero se exporta una clave mediante la función **BCryptExportKey** antes de la importación mediante la función **BCryptImportKey** . Las funciones están diseñadas para habilitar el cifrado de las claves exportadas y importadas mediante los parámetros *hExportKey* y *hImportKey* . sin embargo, la implementación de Microsoft de estas funciones no admite el cifrado de claves exportadas y importadas.

## <a name="asymmetric-keys"></a>Claves asimétricas

Para importar pares de claves asimétricas (o [*públicas y privadas*](/windows/desktop/SecGloss/p-gly)) en las que se usa una clave para cifrar y la otra se usa para descifrar algunos datos, puede utilizar cualquiera de las funciones [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) o [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) . Un proveedor de CNG debe codificar el par de claves mediante un tipo de [*BLOB de clave*](/windows/desktop/SecGloss/k-gly) compatible. [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) se puede usar para crear el BLOB de clave codificado. Las [estructuras CNG](cng-structures.md) describen los tipos de BLOB de clave y las estructuras que admite el proveedor de almacenamiento de claves de Microsoft.

Para que [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) cree un par de claves persistentes, el BLOB de clave de entrada debe contener una [*clave privada*](/windows/desktop/SecGloss/p-gly). [*Las claves públicas*](/windows/desktop/SecGloss/p-gly) no se conservan.

El nombre de clave y la Directiva de exportación no forman parte de la estructura de [*BLOB*](/windows/desktop/SecGloss/b-gly) definida en las [estructuras de CNG](cng-structures.md). Sin embargo, si un BLOB es de un tipo de BLOB opaco (como la imagen de memoria de un estado de clave interna), el BLOB podría contener el nombre de clave y las propiedades de la Directiva de exportación.

En el procedimiento siguiente se describe cómo importar una clave privada persistente con sus propiedades.

**Para importar una clave persistente**

1.  Cree una clave persistente mediante la función [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) .
2.  Establezca las propiedades deseadas en el objeto de clave mediante la función [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) .
3.  Establezca el BLOB de la clave de importación como una propiedad de la clave, con el tipo de BLOB como el nombre de la propiedad.
4.  Finalice la importación de clave conservada mediante la función [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) .

 

 
