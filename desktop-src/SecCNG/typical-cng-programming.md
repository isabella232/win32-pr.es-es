---
description: La API de CNG implementa un modelo de proveedor extensible que permite cargar un proveedor especificando el algoritmo criptográfico necesario en lugar de un proveedor determinado.
ms.assetid: a88a089b-4afe-4201-96f7-97f19bce18a1
title: Programación típica de CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1cd45c68d7c34c3815008690b49cabfefff437222b29512abbf858cf3b370f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905526"
---
# <a name="typical-cng-programming"></a>Programación típica de CNG

La API de CNG implementa un modelo de proveedor extensible que permite cargar un proveedor especificando el algoritmo criptográfico necesario en lugar de un proveedor determinado. La ventaja es que un proveedor de algoritmos se puede reemplazar o actualizar y no tendrá que cambiar el código de ninguna manera para usar el nuevo proveedor. Además, si se determina que algún algoritmo no es seguro en el futuro, se puede instalar una versión más segura de ese algoritmo sin afectar al código. La mayoría de las API de CNG requieren un proveedor o un objeto creado por un proveedor.

Los pasos típicos implicados en el uso de la API de CNG para operaciones primitivas criptográficas son los siguientes:

1.  Abrir el proveedor de algoritmos
2.  Obtener o establecer propiedades de algoritmo
3.  Crear o importar una clave
4.  Realizar operaciones criptográficas
5.  Cerrar el proveedor de algoritmos

Para obtener más información, vea Ejemplos de programación.

## <a name="opening-the-algorithm-provider"></a>Abrir el proveedor de algoritmos

La [**función BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) proporciona un identificador de proveedor de algoritmos que se usa en las API de CNG posteriores, como [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) o [**BCryptGenerateKeyPair.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair)

## <a name="getting-or-setting-algorithm-properties"></a>Obtener o establecer propiedades de algoritmo

Puede usar el identificador del proveedor de algoritmos para obtener los detalles de implementación del algoritmo, como el tamaño de clave o el modo de operación actual. La función [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) se usa para obtener propiedades específicas.

También puede modificar las propiedades del algoritmo. Por ejemplo, si desea usar el encadenamiento de cifrado de bloques DE INDIG CON AES, establezca la propiedad **BCRYPT \_ CHAINING \_ MODE** de un algoritmo AES en **BCRYPT \_ CHAIN MODE \_ \_ ALGORITHM**; la propiedad se asigna a todas las claves AES creadas con este identificador de algoritmo, sin necesidad de configurar cada una de las claves AES. Use la función [**BCryptSetProperty para**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) modificar estas propiedades.

## <a name="creating-or-importing-a-key"></a>Crear o importar una clave

Dependiendo del tipo de algoritmo que use, es posible que tenga que crear o cargar una clave. Por ejemplo, la [**función BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) toma un identificador de clave para el primer parámetro. Si desea que esa función cifre los datos con un algoritmo de cifrado simétrico como AES, primero debe obtener una clave. La forma de obtener la clave depende del tipo de algoritmo que se usa y del origen de la clave.

Puede crear claves efímeras con las funciones [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) y [**BCryptGenerateKeyPair.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) También puede importar claves efímeras desde un BLOB de memoria con las funciones [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) y [**BCryptImportKeyPair.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair)

En el caso de las claves persistentes, use las funciones de almacenamiento de claves para cargar un proveedor de almacenamiento de claves y, a continuación, cree o cargue las claves. También puede usar estas funciones para crear o cargar claves efímeras pasando **NULL para** cualquier nombre de contenedor. Para obtener más información sobre las funciones de almacenamiento de claves, vea [CNG Key Storage Functions](cng-key-storage-functions.md).

## <a name="performing-cryptographic-operations"></a>Realizar operaciones criptográficas

Ahora está listo para realizar la operación criptográfica, como cifrar o descifrar datos mediante las funciones [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) o [**BCryptDecrypt,**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) respectivamente.

## <a name="closing-the-algorithm-provider"></a>Cerrar el proveedor de algoritmos

Cuando el proveedor ya no sea necesario, debe pasar el identificador a la función [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) para cerrar el proveedor. Esto hace que el proveedor libere todos los recursos que se han asignado para esa instancia del proveedor de algoritmos. Una vez cerrado un identificador de proveedor, no se puede reutilizar.

La carga de un proveedor puede ser un proceso relativamente largo. Por lo tanto, debe almacenar en caché todos los identificadores de proveedor a los que haga referencia varias veces durante la vigencia de la aplicación.

## <a name="programming-examples"></a>Ejemplos de programación

En los ejemplos siguientes se describe cómo realizar operaciones criptográficas específicas mediante CNG.

-   [Creación de un hash con CNG](creating-a-hash-with-cng.md)
-   [Firma de datos con CNG](signing-data-with-cng.md)
-   [Cifrado de datos con CNG](encrypting-data-with-cng.md)

 

 



