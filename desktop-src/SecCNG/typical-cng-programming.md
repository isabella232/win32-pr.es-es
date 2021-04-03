---
description: La API CNG implementa un modelo de proveedor extensible que le permite cargar un proveedor especificando el algoritmo criptográfico necesario en lugar de un proveedor determinado.
ms.assetid: a88a089b-4afe-4201-96f7-97f19bce18a1
title: Programación de CNG típica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1119da63ca1ea0613444b150914c06664f36c121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809895"
---
# <a name="typical-cng-programming"></a>Programación de CNG típica

La API CNG implementa un modelo de proveedor extensible que le permite cargar un proveedor especificando el algoritmo criptográfico necesario en lugar de un proveedor determinado. La ventaja es que un proveedor de algoritmos se puede reemplazar o actualizar y no tendrá que cambiar el código de ninguna manera para usar el nuevo proveedor. Además, si se determina que algún algoritmo no es seguro en el futuro, se puede instalar una versión más segura de ese algoritmo sin que ello afecte al código. La mayoría de las API de CNG requieren un proveedor o un objeto creado por un proveedor.

Los pasos típicos implicados en el uso de la API de CNG para las operaciones primitivas criptográficas son los siguientes:

1.  Abrir el proveedor de algoritmos
2.  Obtener o establecer las propiedades del algoritmo
3.  Crear o importar una clave
4.  Realización de operaciones criptográficas
5.  Cerrar el proveedor de algoritmos

Para obtener más información, vea ejemplos de programación.

## <a name="opening-the-algorithm-provider"></a>Abrir el proveedor de algoritmos

La función [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) proporciona un identificador de proveedor de algoritmos que se usa en las API CNG posteriores, como [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) o [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair).

## <a name="getting-or-setting-algorithm-properties"></a>Obtener o establecer las propiedades del algoritmo

Puede usar el identificador del proveedor de algoritmos para obtener los detalles de implementación del algoritmo, como el tamaño de la clave o el modo de funcionamiento actual. La función [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) se usa para obtener propiedades específicas.

También puede modificar las propiedades del algoritmo. Por ejemplo, si desea usar el encadenamiento de cifrado de bloques ECB con AES, establezca la propiedad del **\_ \_ modo de encadenamiento BCRYPT** de un algoritmo AES en el **\_ modo de cadena \_ \_ bcrypt**. la propiedad se asigna a todas las claves AES creadas con este identificador de algoritmo, sin necesidad de configurar cada una de las claves AES. Utilice la función [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) para modificar estas propiedades.

## <a name="creating-or-importing-a-key"></a>Crear o importar una clave

Dependiendo del tipo de algoritmo que use, puede que tenga que crear o cargar una clave. Por ejemplo, la función [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) toma un identificador de clave para el primer parámetro. Si desea que esa función Cifre los datos con un algoritmo de cifrado simétrico como AES, primero debe obtener una clave. La forma de obtener la clave depende del tipo de algoritmo que se use y el origen de la clave.

Puede crear claves efímeras con las funciones [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) y [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) . También puede importar claves efímeras de un BLOB en memoria con las funciones [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) y [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) .

En el caso de las claves persistentes, utilice las funciones de almacenamiento de claves para cargar un proveedor de almacenamiento de claves y, a continuación, cree o cargue las claves. También puede usar estas funciones para crear o cargar claves efímeras pasando **null** para cualquier nombre de contenedor. Para obtener más información sobre las funciones de almacenamiento de claves, consulte [funciones de almacenamiento de claves CNG](cng-key-storage-functions.md).

## <a name="performing-cryptographic-operations"></a>Realización de operaciones criptográficas

Ahora está listo para realizar la operación criptográfica, como cifrar o descifrar los datos mediante las funciones [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) o [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) , respectivamente.

## <a name="closing-the-algorithm-provider"></a>Cerrar el proveedor de algoritmos

Cuando el proveedor ya no sea necesario, debe pasar el identificador a la función [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) para cerrar el proveedor. Esto hace que el proveedor libere los recursos asignados para esa instancia del proveedor de algoritmos. Una vez cerrado un identificador de proveedor, no se puede volver a usar.

Cargar un proveedor puede ser un proceso que consume mucho tiempo. Por lo tanto, debe almacenar en caché todos los identificadores de proveedor a los que hará referencia varias veces durante la vigencia de la aplicación.

## <a name="programming-examples"></a>Ejemplos de programación

En los ejemplos siguientes se describe cómo realizar operaciones criptográficas específicas mediante CNG.

-   [Crear un hash con CNG](creating-a-hash-with-cng.md)
-   [Firmar datos con CNG](signing-data-with-cng.md)
-   [Cifrar datos con CNG](encrypting-data-with-cng.md)

 

 



