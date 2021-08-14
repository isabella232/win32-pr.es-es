---
description: Puede importar y exportar claves simétricas y claves asimétricas con CNG. Y puede usar la funcionalidad de exportación e importación de claves para mover claves entre máquinas.
ms.assetid: 37bda1e0-5dd2-455c-9627-4e7e1b0e04d3
title: Importación y exportación de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a4b6c26069911d771697bf06f7464aa14ab7f099e4a0e06991d2fd992efa44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907706"
---
# <a name="key-import-and-export"></a>Importación y exportación de claves

Puede importar y exportar claves [*simétricas y*](/windows/desktop/SecGloss/s-gly) claves asimétricas con CNG. Y puede usar la funcionalidad de exportación e importación de claves para mover claves entre máquinas.

## <a name="symmetric-keys"></a>Claves simétricas

Para importar o exportar claves simétricas (o de sesión) en las que se usa la misma clave para cifrar y descifrar algunos datos, puede usar las funciones [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) y [**BCryptExportKey.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) Normalmente, primero se exporta una clave mediante la función **BCryptExportKey** antes de importar mediante la **función BCryptImportKey.** Las funciones están diseñadas para habilitar el cifrado de claves exportadas e importadas mediante los *parámetros hExportKey* y *hImportKey;* sin embargo, la implementación de Microsoft de estas funciones no admite el cifrado de claves exportadas e importadas.

## <a name="asymmetric-keys"></a>Claves asimétricas

Para importar pares [](/windows/desktop/SecGloss/p-gly)de claves asimétricas (o públicas o privadas) en las que se usa una clave para cifrar y la otra para descifrar algunos datos, puede usar cualquiera de las funciones [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) o [**NCryptImportKey.**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) Un proveedor de CNG debe codificar el par de claves mediante un tipo [*blob de clave*](/windows/desktop/SecGloss/k-gly) compatible. [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) se puede usar para crear el blob de clave codificada. [Estructuras CNG](cng-structures.md) describe los tipos y estructuras de BLOB clave que admite el proveedor de Storage Microsoft Key.

Para [**que BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) cree un par de claves persistente, la clave de entrada BLOB debe contener [*una clave privada*](/windows/desktop/SecGloss/p-gly). [*Las claves públicas*](/windows/desktop/SecGloss/p-gly) no se conservan.

El nombre de clave y la directiva de exportación no forman parte de la [*estructura BLOB*](/windows/desktop/SecGloss/b-gly) definida en [estructuras CNG](cng-structures.md). Sin embargo, si un BLOB es de un tipo blob opaco (por ejemplo, la imagen de memoria de un estado de clave interna), el BLOB podría contener el nombre de clave y las propiedades de la directiva de exportación.

En el procedimiento siguiente se describe cómo importar una clave privada persistente con sus propiedades.

**Para importar una clave persistente**

1.  Cree una clave persistente mediante la función [**NCryptCreatePersistedKey.**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
2.  Establezca las propiedades deseadas en el objeto de clave mediante la [**función NCryptSetProperty.**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
3.  Establezca la clave de importación BLOB como una propiedad en la clave, con el tipo BLOB como nombre de propiedad.
4.  Finalizar la importación de clave persistente mediante la [**función NCryptFinalizeKey.**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey)

 

 
