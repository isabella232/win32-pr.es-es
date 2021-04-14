---
description: Explica cómo generar, intercambiar, importar y exportar claves de Diffie-Hellman.
ms.assetid: 623a8c9e-3f6a-470b-be30-dec13342bb90
title: Claves de Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00eaddd580ac74e18e26498175f87b5d81b8e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361628"
---
# <a name="diffie-hellman-keys"></a>Claves de Diffie-Hellman

-   [Generar claves de Diffie-Hellman](#generating-diffie-hellman-keys)
-   [Intercambio de claves de Diffie-Hellman](#exchanging-diffie-hellman-keys)
-   [Exportar una clave privada Diffie-Hellman](#exporting-a-diffie-hellman-private-key)
-   [Código de ejemplo](#example-code)

## <a name="generating-diffie-hellman-keys"></a>Generar claves de Diffie-Hellman

Para generar una clave de Diffie-Hellman, realice los pasos siguientes:

1.  Llame a la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor de servicios criptográficos de Microsoft Diffie-Hellman.
2.  Genere la nueva clave. Hay dos maneras de lograrlo: Si tiene CryptoAPI, debe generar todos los valores nuevos para G, P y X, o bien usar los valores existentes para G y P, y generar un nuevo valor para X.

    **Para generar la clave generando todos los valores nuevos**

    1.  Llame a la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) , pasando **CALG \_ DH \_ SF** (almacenar y reenviar) o **CALG \_ DH \_ EPHEM** (efímero) en el parámetro *algid* . La clave se generará con nuevos valores aleatorios para G y P, un valor calculado recientemente para X y su identificador se devolverá en el parámetro *phKey* .
    2.  La nueva clave ya está lista para su uso. Los valores de G y P deben enviarse al destinatario junto con la clave (o enviados por algún otro método) al realizar un [*intercambio de claves*](../secgloss/e-gly.md).

    **Para generar la clave con valores predefinidos para G y P**

    1.  Llame [**a CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) pasando **CALG \_ DH \_ SF** (almacenar y reenviar) o **CALG \_ DH \_ EPHEM** (efímero) en el parámetro *algid* y **CRYPT \_ PREGEN** para el parámetro *dwFlags* . Se generará un identificador de clave y se devolverá en el parámetro *phKey* .
    2.  Inicialice una estructura de [**\_ \_ BLOB de datos de cifrado**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) con el miembro **PbData** establecido en el valor P. El [*BLOB*](../secgloss/b-gly.md) no contiene información de encabezado y el miembro **pbData** está en formato [*Little-Endian*](../secgloss/l-gly.md) .
    3.  El valor de P se establece mediante una llamada a la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , pasando el identificador de clave recuperado en el paso a en el parámetro *hKey* , la marca de **KP \_ P** en el parámetro *dwParam* y un puntero a la estructura que contiene el valor de P en el parámetro *pbData* .
    4.  Inicialice una estructura de [**\_ \_ BLOB de datos de cifrado**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) con el miembro **PbData** establecido en el valor G. El BLOB no contiene información de encabezado y el miembro **pbData** está en formato Little-Endian.
    5.  El valor de G se establece mediante una llamada a la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , pasando el identificador de clave recuperado en el paso a en el parámetro *hKey* , la marca de **KP \_ G** en el parámetro *dwParam* y un puntero a la estructura que contiene el valor de G en el parámetro *pbData* .
    6.  El valor de X se genera mediante una llamada a la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , pasando el identificador de clave recuperado en el paso a en el parámetro *hKey* , la marca de **KP \_ X** en el parámetro *dwParam* y **null** en el parámetro *pbData* .
    7.  Si todas las llamadas de función se realizaron correctamente, la clave pública Diffie-Hellman está lista para su uso.

3.  Cuando ya no se necesite la clave, debe destruirla pasando el identificador de la clave a la función [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .

Si se especificó **CALG \_ DH \_ SF** en los procedimientos anteriores, los valores de clave se conservan en el almacenamiento con cada llamada a [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam). Los valores G y P se pueden recuperar mediante la función [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) . Algunos CSP pueden tener valores G y P codificados de forma rígida. En este caso, se devolverá un error de **NTE \_ FIXEDPARAMETER** si se llama a **CryptSetKeyParam** con **KP \_ G** o **KP \_ P** especificados en el parámetro *dwParam* . Si se llama a **CryptDestroyKey** , se destruye el identificador de la clave, pero los valores de clave se conservan en el CSP. Sin embargo, si se especificó **CALG \_ DH \_ EPHEM** , se destruye el identificador de la clave y se borran todos los valores del CSP.

## <a name="exchanging-diffie-hellman-keys"></a>Intercambio de claves de Diffie-Hellman

El propósito del algoritmo Diffie-Hellman es hacer posible que dos o más entidades creen y compartan una clave de sesión secreta idéntica compartiendo información a través de una red que no es segura. La información que se comparte a través de la red está en forma de un par de valores constantes y una Diffie-Hellman clave pública. El proceso que usan dos entidades de intercambio de claves es el siguiente:

-   Ambas partes aceptan el Diffie-Hellman parámetros, que son un número primo (P) y un número de generador (G).
-   La entidad 1 envía su clave pública Diffie-Hellman a la entidad 2.
-   La entidad 2 calcula la clave de sesión secreta usando la información contenida en la clave privada y la clave pública de la entidad 1.
-   La entidad 2 envía su clave pública Diffie-Hellman a la entidad 1.
-   La entidad 1 calcula la clave de sesión secreta mediante la información contenida en su clave privada y la clave pública de la entidad 2.
-   Ambas partes tienen ahora la misma clave de sesión, que se puede usar para cifrar y descifrar los datos. Los pasos necesarios para ello se muestran en el procedimiento siguiente.

**Para preparar una clave pública de Diffie-Hellman para la transmisión**

1.  Llame a la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor de servicios criptográficos de Microsoft Diffie-Hellman.
2.  Cree una clave de Diffie-Hellman llamando a la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para crear una nueva clave o llamando a la función [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) para recuperar una clave existente.
3.  Obtiene el tamaño necesario para contener el BLOB de clave Diffie-Hellman llamando a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), pasando **null** para el parámetro *pbData* . El tamaño necesario se devolverá en *pdwDataLen*.
4.  Asigne memoria para el BLOB de clave.
5.  Cree un [*BLOB de clave pública*](../secgloss/p-gly.md) Diffie-Hellman llamando a la función [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , pasando **PUBLICKEYBLOB** en el parámetro *dwBlobType* y el identificador a la clave de Diffie-Hellman en el parámetro *hKey* . Esta llamada de función provoca el cálculo del valor de clave pública (G ^ X) mod P.
6.  Si todas las llamadas de función anteriores se realizaron correctamente, el BLOB de clave pública de Diffie-Hellman ya está listo para su codificación y transmisión.

**Para importar una clave pública Diffie-Hellman y calcular la clave de sesión secreta**

1.  Llame a la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor de servicios criptográficos de Microsoft Diffie-Hellman.
2.  Cree una clave de Diffie-Hellman llamando a la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para crear una nueva clave o llamando a la función [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) para recuperar una clave existente.
3.  Para importar la clave pública de Diffie-Hellman en el CSP, llame a la función [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) , pasando un puntero al BLOB de clave pública en el parámetro *pbData* , la longitud del BLOB en el parámetro *dwDataLen* y el identificador de la clave de Diffie-Hellman en el parámetro *hPubKey* . Esto hace que se realice el cálculo (Y ^ X) mod P, con lo que se crea la clave secreta compartida y se completa el [*intercambio de claves*](../secgloss/e-gly.md). Esta llamada de función devuelve un identificador para la nueva clave de sesión secreta en el parámetro *hKey* .
4.  En este punto, la Diffie-Hellman importada es de tipo **CALG \_ AGREEDKEY \_ any**. Antes de que se pueda usar la clave, debe convertirse en un tipo de clave de sesión. Esto se logra mediante una llamada a la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con *DwParam* establecida en **KP \_ ALGID** y con *pbData* establecido en un puntero a un valor de [**\_ identificador de alg**](alg-id.md) que representa una clave de sesión, como **CALG \_ RC4**. La clave se debe convertir antes de usar la clave compartida en la función [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) o [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) . Se producirá un error en las llamadas realizadas a cualquiera de estas funciones antes de convertir el tipo de clave.
5.  La clave de sesión secreta ahora está lista para usarse para el cifrado o el descifrado.
6.  Cuando la clave ya no sea necesaria, destruya el identificador de clave mediante una llamada a la función [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .

## <a name="exporting-a-diffie-hellman-private-key"></a>Exportar una clave privada Diffie-Hellman

Para exportar una clave privada Diffie-Hellman, realice los pasos siguientes:

1.  Llame a la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor de servicios criptográficos de Microsoft Diffie-Hellman.
2.  Cree una clave de Diffie-Hellman llamando a la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para crear una nueva clave o llamando a la función [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) para recuperar una clave existente.
3.  Cree un [*BLOB de clave privada*](../secgloss/p-gly.md) Diffie-Hellman llamando a la función [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , pasando **PRIVATEKEYBLOB** en el parámetro *dwBlobType* y el identificador a la clave de Diffie-Hellman en el parámetro *hKey* .
4.  Cuando el identificador de clave ya no sea necesario, llame a la función [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) para destruir el identificador de clave.

## <a name="example-code"></a>Código de ejemplo

En el ejemplo siguiente se muestra cómo crear, exportar, importar y usar una clave de Diffie-Hellman para realizar un intercambio de claves.


```C++
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// The key size, in bits.
#define DHKEYSIZE 512

// Prime in little-endian format.
static const BYTE g_rgbPrime[] = 
{
    0x91, 0x02, 0xc8, 0x31, 0xee, 0x36, 0x07, 0xec, 
    0xc2, 0x24, 0x37, 0xf8, 0xfb, 0x3d, 0x69, 0x49, 
    0xac, 0x7a, 0xab, 0x32, 0xac, 0xad, 0xe9, 0xc2, 
    0xaf, 0x0e, 0x21, 0xb7, 0xc5, 0x2f, 0x76, 0xd0, 
    0xe5, 0x82, 0x78, 0x0d, 0x4f, 0x32, 0xb8, 0xcb,
    0xf7, 0x0c, 0x8d, 0xfb, 0x3a, 0xd8, 0xc0, 0xea, 
    0xcb, 0x69, 0x68, 0xb0, 0x9b, 0x75, 0x25, 0x3d,
    0xaa, 0x76, 0x22, 0x49, 0x94, 0xa4, 0xf2, 0x8d 
};

// Generator in little-endian format.
static BYTE g_rgbGenerator[] = 
{
    0x02, 0x88, 0xd7, 0xe6, 0x53, 0xaf, 0x72, 0xc5,
    0x8c, 0x08, 0x4b, 0x46, 0x6f, 0x9f, 0x2e, 0xc4,
    0x9c, 0x5c, 0x92, 0x21, 0x95, 0xb7, 0xe5, 0x58, 
    0xbf, 0xba, 0x24, 0xfa, 0xe5, 0x9d, 0xcb, 0x71, 
    0x2e, 0x2c, 0xce, 0x99, 0xf3, 0x10, 0xff, 0x3b,
    0xcb, 0xef, 0x6c, 0x95, 0x22, 0x55, 0x9d, 0x29,
    0x00, 0xb5, 0x4c, 0x5b, 0xa5, 0x63, 0x31, 0x41,
    0x13, 0x0a, 0xea, 0x39, 0x78, 0x02, 0x6d, 0x62
};

BYTE g_rgbData[] = {0x01, 0x02, 0x03, 0x04,    0x05, 0x06, 0x07, 0x08};

int _tmain(int argc, _TCHAR* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    BOOL fReturn;
    HCRYPTPROV hProvParty1 = NULL; 
    HCRYPTPROV hProvParty2 = NULL; 
    DATA_BLOB P;
    DATA_BLOB G;
    HCRYPTKEY hPrivateKey1 = NULL;
    HCRYPTKEY hPrivateKey2 = NULL;
    PBYTE pbKeyBlob1 = NULL;
    PBYTE pbKeyBlob2 = NULL;
    HCRYPTKEY hSessionKey1 = NULL;
    HCRYPTKEY hSessionKey2 = NULL;
    PBYTE pbData = NULL;

    /************************
    Construct data BLOBs for the prime and generator. The P and G 
    values, represented by the g_rgbPrime and g_rgbGenerator arrays 
    respectively, are shared values that have been agreed to by both 
    parties.
    ************************/
    P.cbData = DHKEYSIZE/8;
    P.pbData = (BYTE*)(g_rgbPrime);

    G.cbData = DHKEYSIZE/8;
    G.pbData = (BYTE*)(g_rgbGenerator);

    /************************
    Create the private Diffie-Hellman key for party 1. 
    ************************/
    // Acquire a provider handle for party 1.
    fReturn = CryptAcquireContext(
        &hProvParty1, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 1.
    fReturn = CryptGenKey(
        hProvParty1, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Create the private Diffie-Hellman key for party 2. 
    ************************/
    // Acquire a provider handle for party 2.
    fReturn = CryptAcquireContext(
        &hProvParty2, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 2.
    fReturn = CryptGenKey(
        hProvParty2, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 1's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen1;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob1 = (PBYTE)malloc(dwDataLen1)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob1,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 2's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen2;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob2 = (PBYTE)malloc(dwDataLen2)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob2,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Party 1 imports party 2's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty1,
        pbKeyBlob2,
        dwDataLen2,
        hPrivateKey1,
        0,
        &hSessionKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }
    
    /************************
    Party 2 imports party 1's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty2,
        pbKeyBlob1,
        dwDataLen1,
        hPrivateKey2,
        0,
        &hSessionKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Convert the agreed keys to symmetric keys. They are currently of 
    the form CALG_AGREEDKEY_ANY. Convert them to CALG_RC4.
    ************************/
    ALG_ID Algid = CALG_RC4;

    // Enable the party 1 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey1,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Enable the party 2 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey2,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Encrypt some data with party 1's session key. 
    ************************/
    // Get the size.
    DWORD dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        NULL, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate a buffer to hold the encrypted data.
    pbData = (PBYTE)malloc(dwLength);
    if(!pbData)
    {
        goto ErrorExit;
    }

    // Copy the unencrypted data to the buffer. The data will be 
    // encrypted in place.
    memcpy(pbData, g_rgbData, sizeof(g_rgbData)); 

    // Encrypt the data.
    dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        pbData, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }
  
    /************************
    Decrypt the data with party 2's session key. 
    ************************/
    dwLength = sizeof(g_rgbData);
    fReturn = CryptDecrypt(
        hSessionKey2,
        0,
        TRUE,
        0,
        pbData,
        &dwLength);
    if(!fReturn)
    {
        goto ErrorExit;
    }


ErrorExit:
    if(pbData)
    {
        free(pbData);
        pbData = NULL;
    }

    if(hSessionKey2)
    {
        CryptDestroyKey(hSessionKey2);
        hSessionKey2 = NULL;
    }

    if(hSessionKey1)
    {
        CryptDestroyKey(hSessionKey1);
        hSessionKey1 = NULL;
    }

    if(pbKeyBlob2)
    {
        free(pbKeyBlob2);
        pbKeyBlob2 = NULL;
    }

    if(pbKeyBlob1)
    {
        free(pbKeyBlob1);
        pbKeyBlob1 = NULL;
    }

    if(hPrivateKey2)
    {
        CryptDestroyKey(hPrivateKey2);
        hPrivateKey2 = NULL;
    }

    if(hPrivateKey1)
    {
        CryptDestroyKey(hPrivateKey1);
        hPrivateKey1 = NULL;
    }

    if(hProvParty2)
    {
        CryptReleaseContext(hProvParty2, 0);
        hProvParty2 = NULL;
    }

    if(hProvParty1)
    {
        CryptReleaseContext(hProvParty1, 0);
        hProvParty1 = NULL;
    }

    return 0;
}
```



 

 
