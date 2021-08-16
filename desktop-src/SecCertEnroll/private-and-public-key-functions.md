---
description: Implementa las interfaces IX509PrivateKey y IX509PublicKey.
ms.assetid: 1358053e-ed4e-4482-b160-5b9b1024c771
title: Funciones de clave privada y pública
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6f210393ffaeb676e0190d391692225f25e0cfb4bc3acbcd2c3c188bf40a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774428"
---
# <a name="private-and-public-key-functions"></a>Funciones de clave privada y pública

CertEnroll.dll implementa las interfaces [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) y [**IX509PublicKey.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) Por ejemplo, puede usar la interfaz [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) para realizar las siguientes acciones en una [*clave privada:*](/windows/desktop/SecGloss/p-gly)

-   Cree, abra, cierre, importe, exporte y elimine la clave.
-   Especifique o recupere el [*algoritmo de clave pública*](/windows/desktop/SecGloss/p-gly).
-   Especifique o recupere información sobre el proveedor de [*servicios criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP) disponible que admite el algoritmo de clave pública.
-   Especifique o recupere el [*certificado*](/windows/desktop/SecGloss/c-gly) asociado a la [*clave privada*](/windows/desktop/SecGloss/p-gly).
-   Especifique o recupere el nombre del contenedor [*de claves.*](/windows/desktop/SecGloss/k-gly)
-   Especifique o recupere una descripción de y un nombre para mostrar para la clave.
-   Especifique o recupere las restricciones de exportación en una clave privada.
-   Especifique o recupere un valor booleano que indique si la clave existe.
-   Especifique o recupere un valor que indique cómo se protege la clave antes de su uso.
-   Especifique o recupere un valor que indique si la clave se puede usar para la firma, el cifrado o ambos.
-   Especifique o recupere un valor que identifique el propósito específico para el que se puede usar la clave.
-   Especifique o recupere la longitud de la clave.
-   Especifique o recupere un valor que indique si la clave se usa o se guarda en el contexto de un equipo o usuario.
-   Recupera un valor booleano que especifica si se ha abierto la clave.
-   Especifique un número de identificación personal para acceder a una clave privada en una [*tarjeta inteligente.*](/windows/desktop/SecGloss/s-gly)
-   Especifique o recupere el nombre del CSP asociado a la clave.
-   Especifique o recupere el [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) de la clave.

Cada una de las secciones siguientes identifica una función exportada por Xenroll.dll que se puede usar para administrar una [*clave criptográfica*](/windows/desktop/SecGloss/c-gly). En cada tema también se describe cómo usar CertEnroll.dll para reemplazar la función o indica que no existe ninguna asignación entre las dos bibliotecas:

-   [ContainerNameWStr](#containernamewstr)
-   [GenKeyFlags](#genkeyflags)
-   [GetKeyLen](#getkeylenex)
-   [GetKeyLenEx](#getkeylenex)
-   [GetSupportedKeySpec](#getsupportedkeyspec)
-   [KeySpec](#getsupportedkeyspec)
-   [LimitExchangeKeyToEncipherment](#limitexchangekeytoencipherment)
-   [PVKFileNameWStr](#pvkfilenamewstr)
-   [ReuseHardwareKeyIfUnableToGenNew](#reusehardwarekeyifunabletogennew)
-   [UseExistingKeySet](#useexistingkeyset)
-   [Temas relacionados](#related-topics)

## <a name="containernamewstr"></a>ContainerNameWStr

La [**función ContainerNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_containernamewstr) Xenroll.dll especifica o recupera el nombre del contenedor [*de claves*](/windows/desktop/SecGloss/k-gly).

Al usar CertEnroll.dll, puede realizar las siguientes acciones para recuperar el nombre de un contenedor de claves:

1.  Llame a [**la propiedad Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) en un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existente.
2.  Llame al [**método GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) en la solicitud devuelta en el paso 1 para recuperar la solicitud más interna.
3.  Llame **a QueryInterface** en el [**objeto IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) devuelto desde el paso 2 para convertir a un objeto [**IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
4.  Llame a [**la propiedad PrivateKey**](/windows/desktop/SecCrypto/privatekey) en la solicitud PKCS \# 10.
5.  Llame a [**la propiedad ContainerName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_containername) en [**el objeto IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperado del paso 4.

## <a name="genkeyflags"></a>GenKeyFlags

La [**función GenKeyFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags) definida en Xenroll.dll especifica o recupera las marcas usadas para generar una clave privada o un par de claves pública [*y privada.*](/windows/desktop/SecGloss/p-gly)

Al usar CertEnroll.dll, puede especificar una serie de propiedades diferentes que determinarán cómo se crea una clave privada. Para obtener más información, vea [**Crear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create).

## <a name="getkeylen"></a>GetKeyLen

La [**función GetKeyLen**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getkeylen) definida en Xenroll.dll recupera el tamaño de clave máximo o mínimo de una clave de cifrado.

Al usar CertEnroll.dll, puede llamar a la propiedad [**Length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) en un objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) o [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) para recuperar el tamaño de clave, en bits.

## <a name="getkeylenex"></a>GetKeyLenEx

La [**función GetKeyLenEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getkeylenex) definida en Xenroll.dll recupera el tamaño máximo o mínimo de la clave o la longitud de incremento de una clave de cifrado.

Al usar CertEnroll.dll, puede llamar a la propiedad [**Length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) en un objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) o [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) para recuperar el tamaño de clave, en bits. Si un algoritmo admite longitudes de clave incrementales, puede llamar a la propiedad [**IncrementLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_incrementlength) en el objeto [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm) para recuperar el valor de incremento. También puede llamar a las [**propiedades MinLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_minlength) y [**MaxLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_maxlength) para recuperar los tamaños de clave mínimo y máximo.

## <a name="getsupportedkeyspec"></a>GetSupportedKeySpec

La [**función GetSupportedKeySpec**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getsupportedkeyspec) definida en Xenroll.dll recupera un valor que indica si un CSP admite claves de intercambio, claves de firma o ambas.

Al usar CertEnroll.dll, puede llamar a la propiedad [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) en los objetos [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) o [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) para recuperar las operaciones admitidas por la clave.

## <a name="keyspec"></a>KeySpec

La [**función KeySpec**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_keyspec) definida en Xenroll.dll especifica o recupera el tipo de clave.

Al usar CertEnroll.dll, puede llamar a la [**propiedad KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) en un [**objeto IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) para recuperar las operaciones admitidas por la clave.

## <a name="limitexchangekeytoencipherment"></a>LimitExchangeKeyToEncipherment

La función [**LimitExchangeKeyToEncipherment**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_limitexchangekeytoencipherment) definida en Xenroll.dll especifica o recupera un valor booleano que indica si una clave de cifrado solo se puede usar para los datos o el cifrado de claves.

CertEnroll.dll no contiene un equivalente directo para esta función. Sin embargo, puede lograr un resultado casi equivalente si especifica un objeto [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage) y lo agrega a la solicitud de certificado.

## <a name="pvkfilenamewstr"></a>PVKFileNameWStr

La [**función PVKFileNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr) definida en Xenroll.dll especifica o recupera el nombre de un archivo que contiene claves exportadas.

Al usar CertEnroll.dll, puede llamar al método [**Export**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-export) en un objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) para exportar una clave a **un BSTR**. Puede llamar al método [**ExportPublicKey para**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-exportpublickey) exportar la [*parte de clave pública*](/windows/desktop/SecGloss/p-gly) de un par de claves asimétricas.

## <a name="reusehardwarekeyifunabletogennew"></a>ReuseHardwareKeyIfUnableToGenNew

La [**función ReuseHardwareKeyIfUnableToGenNew**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_reusehardwarekeyifunabletogennew) definida en Xenroll.dll especifica o recupera un valor booleano que indica si se reutiliza una clave existente cuando se encuentra un error al generar una clave nueva.

Al usar CertEnroll.dll, puede llamar al método [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) en un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y especificar un valor del tipo de enumeración [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) para reutilizar una clave privada existente.

## <a name="useexistingkeyset"></a>UseExistingKeySet

La [**función UseExistingKeySet**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset) definida en Xenroll.dll especifica o recupera un valor booleano que indica si se deben usar las claves existentes.

Al usar CertEnroll.dll, puede llamar al método [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) en un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y especificar un valor del tipo de enumeración [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) para reutilizar las claves públicas y privadas existentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
