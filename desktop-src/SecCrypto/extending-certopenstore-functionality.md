---
description: El almacén de certificados es fundamental para todas las operaciones de administración de certificados.
ms.assetid: e5c7c882-cbfc-4343-952c-b13c67326756
title: Extensión de la funcionalidad CertOpenStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce198578cc482ba0488bd97ae0f1d7f923511b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171030"
---
# <a name="extending-certopenstore-functionality"></a>Extensión de la funcionalidad CertOpenStore

El [*almacén de certificados*](../secgloss/c-gly.md) es fundamental para todas las operaciones de administración de certificados. La funcionalidad de la [**función CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) se puede ampliar mediante el uso de una función de proveedor de almacén de certificados instalable (o registrada). Para obtener información general sobre cómo instalar o registrar funciones para su uso con CryptoAPI, vea [Información general de OID.](oid-overview.md)

> [!Note]  
> Los almacenes de certificados personalizados no se migran automáticamente al realizar implementaciones automatizadas. Para migrar almacenes de certificados personalizados, debe crear un manifiesto para migrar los almacenes personalizados y usar el Windows Herramienta de migración de estado de usuario (USMT). El USMT está disponible para su descarga desde el Centro de descarga de Microsoft en <https://www.microsoft.com/download/details.aspx?id=10837> .

 

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) abre un almacén vacío en memoria y llama a la función del [](../secgloss/o-gly.md) proveedor de almacén (si está registrada o instalada) mediante el identificador de objeto (OID) que se pasó en el parámetro *lpszStoreProvider.* Para obtener una lista de los tipos de proveedor predefinidos que se proporcionan con CryptoAPI, vea **CertOpenStore**.

La función de proveedor de almacén copia sus certificados y listas de [*revocación*](../secgloss/c-gly.md) de certificados (CRL) en el almacén en memoria especificado por el *identificador hCertStore* que se le pasa. La nueva función de proveedor de almacén puede usar cualquiera de las funciones de almacén de certificados CryptoAPI, como [**CertAddCertificateContextToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore) o [**CertAddSerializedElementToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore), para agregar sus certificados y CRL al almacén en memoria. Además, la función store-provider devuelve opcionalmente valores para todos los miembros de datos de la [**estructura CERT \_ STORE \_ PROV \_ INFO.**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) La función solo necesita actualizar esta estructura si admite funciones de devolución de llamada adicionales. Por ejemplo, si el almacén fuera a ser un almacén de solo lectura, probablemente no sería necesaria la compatibilidad con otras funciones de devolución de llamada. Para obtener detalles y prototipos de las posibles funciones de devolución de llamada, vea Funciones de devolución de llamada del [proveedor de almacén de certificados](cryptography-functions.md).

El almacén TrustedPeople por usuario está restringido a almacenes físicos predefinidos. No se puede extender el almacén TrustedPeople por usuario. Sin embargo, puede ampliar el almacén TrustedPeople de la máquina local.

**Windows XP y Windows Server 2003:** El almacén TrustedPeople por usuario no está restringido a almacenes físicos predefinidos.

Uno de los miembros de datos de la [**estructura CERT \_ STORE \_ PROV \_ INFO**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) es *la matriz rgpvStoreProvFunc.* Si la función de proveedor de almacén necesita admitir una o varias de las funciones de devolución de llamada, debe proporcionar punteros para esta matriz. Estos punteros deben apuntar a las funciones de devolución de llamada que se van a usar para otras actividades de almacén de certificados (como cerrar el almacén). En la ilustración siguiente se muestra el flujo de este proceso.

![Funcionalidad certopenstore](images/openstor.png)

Como se muestra en la siguiente ilustración, una vez abierto el almacén, otras funciones CryptoAPI (como [**CertCloseStore)**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)usan la matriz de punteros para acceder a las funciones de devolución de llamada que realizan la tarea prevista. La definición de la estructura [**CERT \_ STORE \_ PROV \_ INFO**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) y los prototipos de las funciones de devolución de llamada predeterminadas que se proporcionan con CryptoAPI se muestran en Funciones de devolución de llamada del proveedor de almacén [de certificados](cryptography-functions.md).

![Funcionalidad certclosestore](images/closstor.png)

Las API de almacén permiten a un proveedor de [](../secgloss/c-gly.md) almacén mantener los certificados, las CRL y las listas de confianza de certificados (CTL) fuera de la memoria caché del almacén (por ejemplo, una base de datos externa de certificados, como la proporcionada por la base de datos del servidor de certificados de Microsoft).

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) envía a través del *parámetro pszStoreProvider* a la función de proveedor [**instalable CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) adecuada. El proveedor devuelve información en el *parámetro pStoreProvInfo* que apunta a una [**estructura CERT STORE \_ \_ PROV \_ INFO.**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) La **estructura CERT STORE \_ \_ PROV \_ INFO** contiene un **miembro dwStoreProvFlags.** Se ha agregado la marca CERT STORE PROV EXTERNAL FLAG para permitir que el proveedor indique que los certificados, las CRL y las CL son externos a la memoria caché \_ \_ del \_ \_ almacén.

[**CertDllOpenStoreProv devuelve**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) una matriz de funciones de devolución de llamada. Un proveedor puede implementar las siguientes funciones de devolución de llamada:

-   CERT \_ STORE \_ PROV \_ CLOSE \_ FUNC
-   CERT \_ STORE \_ PROV \_ READ \_ CERT \_ FUNC
-   CERT \_ STORE \_ PROV WRITE CERT \_ FUNC (FUNC DE CERTIFICADO DE ESCRITURA DE \_ \_ PROV DEL ALMACÉN DE CERTIFICADOS)
-   CERT \_ STORE \_ PROV \_ DELETE \_ CERT \_ FUNC
-   CERT \_ STORE \_ PROV \_ SET \_ CERT \_ PROPERTY \_ FUNC
-   CERT \_ STORE \_ PROV \_ READ \_ CRL \_ FUNC
-   FUNC DE CRL DE ESCRITURA \_ \_ DE \_ \_ PROV DEL ALMACÉN DE \_ CERTIFICADOS
-   CERT \_ STORE \_ PROV \_ DELETE \_ CRL \_ FUNC
-   FUNC DE LA PROPIEDAD CRL DE CERT \_ STORE \_ PROV \_ SET \_ \_ \_
-   CERT \_ STORE \_ PROV \_ READ \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ WRITE \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ DELETE \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ SET \_ CTL \_ PROPERTY \_ FUNC

En las llamadas a las funciones de devolución de llamada WRITE CERT, WRITE CRL y WRITE CTL cuando se establece CERT STORE PROV WRITE ADD FLAG, los 16 bits superiores del parámetro dwFlags contienen el valor \_ \_ \_ \_ \_ \_ \_ \_ *dwAddDisposition.*  Para admitir almacenes externos, un proveedor puede implementar las siguientes funciones de devolución de llamada:

-   CERT \_ STORE \_ PROV \_ FIND \_ CERT \_ FUNC
-   CERT \_ STORE \_ PROV \_ FREE \_ FIND \_ CERT \_ FUNC
-   CERT \_ STORE \_ PROV \_ GET \_ CERT \_ PROPERTY \_ FUNC
-   CERT \_ STORE \_ PROV \_ FIND \_ CRL \_ FUNC
-   CERT \_ STORE \_ PROV \_ FREE \_ FIND \_ CRL \_ FUNC
-   FUNC DE LA PROPIEDAD \_ \_ GET \_ \_ CRL \_ \_ DE CERT STORE PROV
-   CERT \_ STORE \_ PROV \_ FIND \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ FREE \_ FIND \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ GET \_ CTL \_ PROPERTY \_ FUNC

Las funciones de devolución de llamada de certificado tienen las firmas siguientes:

``` syntax
typedef struct _CERT_STORE_PROV_FIND_INFO {
    DWORD               cbSize;
    DWORD               dwMsgAndCertEncodingType;
    DWORD               dwFindFlags;
    DWORD               dwFindType;
    const void          *pvFindPara;
} CERT_STORE_PROV_FIND_INFO, *PCERT_STORE_PROV_FIND_INFO;
typedef const CERT_STORE_PROV_FIND_INFO CCERT_STORE_PROV_FIND_INFO,
    *PCCERT_STORE_PROV_FIND_INFO;

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_FIND_CERT)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_STORE_PROV_FIND_INFO pFindInfo,
        IN PCCERT_CONTEXT pPrevCertContext,
        IN DWORD dwFlags,
        IN OUT void **ppvStoreProvFindInfo,
        OUT PCCERT_CONTEXT *ppProvCertContext
        );

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_FREE_FIND_CERT)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_CONTEXT pCertContext,
        IN void *pvStoreProvFindInfo,
        IN DWORD dwFlags
        );

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_GET_CERT_PROPERTY)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_CONTEXT pCertContext,
        IN DWORD dwPropId,
        IN DWORD dwFlags,
        OUT void *pvData,
        IN OUT DWORD *pcbData
        );
```

Las firmas de las funciones de devolución de llamada CRL y CTL son idénticas a las anteriores, con el puntero a [**CERT \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) reemplazado por un puntero a UN CONTEXTO [**DE CRL \_**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) o [**CTL \_ CONTEXT.**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context)

Se llama a la devolución de llamada FIND CERT cuando las API de \_ almacén enumeran, encuentran o agregan certificados. *pPrevCertContext* y *ppvStoreProvFindInfo* se establecen en **NULL** para iniciar una nueva instrucción FIND. El valor *ppvStoreProvFindInfo* devuelto se devuelve en la siguiente búsqueda, momento en el que el proveedor puede liberarlo. El proveedor puede establecer todas, algunas o ninguna de las propiedades del certificado. El proveedor tiene la opción de aplazar hasta que se llame a la devolución de llamada GET \_ CERT \_ PROPERTY. Se recomienda que los proveedores establezcan tantas propiedades como sea posible para permitir la copia en otro almacén.

Los siguientes tipos de búsqueda de certificados se admiten [**en CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore):

-   CERT \_ FIND \_ ANY
-   HASH \_ SHA1 DE CERT FIND \_ \_
-   CERT \_ FIND \_ MD5 \_ HASH
-   CERT \_ FIND \_ (PROPIEDAD)
-   CERT \_ FIND \_ PUBLIC \_ KEY
-   CERT \_ FIND \_ SUBJECT \_ NAME
-   CERT \_ FIND \_ SUBJECT \_ ATTR
-   CERT \_ FIND \_ ISSUER \_ NAME
-   CERT \_ FIND \_ ISSUER \_ ATTR
-   CERT \_ FIND \_ SUBJECT \_ STR \_ A
-   CERT \_ FIND \_ SUBJECT \_ STR \_ W
-   CERT \_ FIND \_ ISSUER \_ STR \_ A
-   CERT \_ FIND \_ ISSUER \_ STR \_ W
-   CERT \_ FIND \_ KEY \_ SPEC
-   CERT \_ FIND \_ ENHKEY \_ USAGE

Se llama \_ a la devolución de llamada FIND CERT para cada uno de los tipos de buscar anteriores. Los parámetros pasados [**a CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) se copian directamente en la estructura CERT STORE PROV FIND INFO antes de llamar a la devolución de \_ llamada FIND \_ \_ \_ \_ CERT. Para obtener más información sobre los valores de campo para los distintos tipos de búsqueda de la estructura CERT \_ STORE \_ PROV \_ FIND \_ INFO, vea **CertFindCertificateInStore**.

Los siguientes tipos de buscar certificados admiten las API [**CertGetSubjectCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) y [**CertGetIssuerCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore) y ayudan a determinar si el certificado ya existe en el almacén antes de agregar:

-   CERT \_ FIND \_ SUBJECT \_ CERT
-   CERT \_ FIND \_ ISSUER \_ OF
-   CERT \_ FIND \_ EXISTING

Para CERT FIND SUBJECT CERT, el parámetro \_ \_ \_ *pvFindPara* [**\_**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_info) apunta a una estructura CERT INFO que contiene los valores Issuer y SerialNumber del asunto. Para CERT \_ FIND \_ ISSUER \_ OF, *pvFindPara* apunta a una [**estructura CERT \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) del asunto. Para CERT \_ FIND \_ EXISTING, *pvFindPara* apunta a un **CONTEXTO \_ CERT** del certificado para comprobar su existencia en el almacén.

Se llama a la devolución de llamada FREE FIND CERT cuando el certificado devuelto por la devolución de llamada FIND CERT no se publicó al usarse en un siguiente FIND CERT posterior, lo que hace que su recuento de referencias se decrete a cero o se libera mediante una llamada \_ \_ a \_ \_ [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore). [](../secgloss/r-gly.md) Antes de llamar a la devolución de llamada CLOSE, todos los certificados devueltos por la devolución de llamada FIND CERT deben liberarse al proveedor al pasarse a una llamada a la devolución de llamada FIND CERT o a una llamada a la devolución de llamada \_ \_ FREE FIND \_ \_ CERT. Lo mismo se aplica a las devoluciones de llamada CRL y CTL.

CertGetCertificateContextProperty llama a la devolución de llamada GET CERT PROPERTY si no encuentra la propiedad especificada \_ \_ para el parámetro *pCertContext.* [](/windows/win32/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) Lo mismo se aplica a GET \_ CRL \_ PROPERTY y GET \_ CTL \_ PROPERTY.

Se llama a la devolución de llamada FIND CRL cuando las API de almacén enumeran u \_ obtienen CRL y antes de agregar una CRL. Se definirán los siguientes tipos de find de CRL:

Para CRL \_ FIND \_ ISSUED \_ BY, *pvFindPara* es un puntero a [**un CONTEXTO \_ DE CERT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) del emisor de CRL. Para CRL \_ FIND \_ EXISTING, *pvFindPara* [**\_**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) es un puntero a un CONTEXTO DE CRL de la CRL para determinar si ya existe en el almacén.

Se llama a \_ la devolución de llamada FIND CTL cuando las API de almacén enumeran o encuentran CTL. Los siguientes tipos de búsqueda de CTL se admiten [**en CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore):

-   CTL \_ FIND \_ ANY
-   CTL \_ FIND \_ SHA1 \_ HASH
-   CTL \_ FIND \_ MD5 \_ HASH
-   CTL \_ FIND \_ USAGE
-   CTL \_ FIND \_ SUBJECT
-   CTL \_ FIND \_ EXISTING

Se llama a \_ la devolución de llamada FIND CTL para cada uno de los tipos de buscar anteriores. Los parámetros pasados [**a CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore) se copian directamente en la estructura CERT STORE PROV FIND INFO antes de llamar a la devolución de \_ llamada \_ \_ \_ \_ CTL de FIND. Para obtener más información sobre los valores de campo para los distintos tipos de búsqueda de la estructura CERT \_ STORE \_ PROV \_ FIND \_ INFO, vea **CertFindCTLInStore**.

El tipo de buscar CTL FIND EXISTING de CTL ayuda a determinar si la CTL ya existe en el almacén antes de \_ \_ realizar una adición de CTL.

Para CTL \_ FIND \_ EXISTING, *pvFindPara* es un puntero a la estructura [**CTL \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context) de la CTL para determinar si ya existe en el almacén.

 

 
