---
description: El almacén de certificados es fundamental para todas las operaciones de administración de certificados.
ms.assetid: e5c7c882-cbfc-4343-952c-b13c67326756
title: Extensión de la funcionalidad de CertOpenStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce198578cc482ba0488bd97ae0f1d7f923511b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565020"
---
# <a name="extending-certopenstore-functionality"></a>Extensión de la funcionalidad de CertOpenStore

El [*almacén de certificados*](../secgloss/c-gly.md) es fundamental para todas las operaciones de administración de certificados. La funcionalidad de la función [**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) se puede extender mediante el uso de una función de proveedor de almacén de certificados instalable (o registrada). Para obtener información general sobre cómo instalar o registrar funciones para su uso con CryptoAPI, consulte [información general sobre OID](oid-overview.md).

> [!Note]  
> Los almacenes de certificados personalizados no se migran automáticamente al realizar implementaciones automatizadas. Para migrar almacenes de certificados personalizados, debe crear un manifiesto para migrar los almacenes personalizados y usar el Herramienta de migración de estado de usuario de Windows (USMT). La herramienta USMT está disponible para su descarga desde el centro de descarga de Microsoft en <https://www.microsoft.com/download/details.aspx?id=10837> .

 

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) abre un almacén vacío en la memoria y llama a la función de proveedor de almacén (si está registrado o instalado) mediante el [*identificador de objeto*](../secgloss/o-gly.md) (OID) que se pasó en el parámetro *lpszStoreProvider* . Para obtener una lista de los tipos de proveedores predefinidos que se proporcionan con CryptoAPI, consulte **CertOpenStore**.

La función de proveedor de almacén copia sus certificados y [*listas de revocación de certificados*](../secgloss/c-gly.md) (CRL) en el almacén en memoria especificado por el identificador de *hCertStore* que se le ha pasado. La nueva función de proveedor de almacén puede usar cualquiera de las funciones del almacén de certificados CryptoAPI, como, [**CertAddCertificateContextToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore) o [**CertAddSerializedElementToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore), para agregar sus certificados y CRL al almacén en memoria. Además, la función de proveedor de almacenamiento devuelve opcionalmente valores para todos los miembros de datos de la estructura de [**información de Prov del almacén de certificados \_ \_ \_**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) . La función solo necesita actualizar esta estructura si admite funciones de devolución de llamada adicionales. Por ejemplo, si el almacén debía ser un almacén de solo lectura, es probable que la compatibilidad con otras funciones de devolución de llamada no fuera necesaria. Para obtener más información y los prototipos de las funciones de devolución de llamada posibles, vea [funciones de devolución de llamada del proveedor del almacén de certificados](cryptography-functions.md).

El almacén TrustedPeople por usuario está restringido a los almacenes físicos predefinidos. No se puede extender el almacén de TrustedPeople por usuario. Sin embargo, puede extender el almacén TrustedPeople del equipo local.

**Windows XP y Windows Server 2003:** El almacén TrustedPeople por usuario no está restringido a los almacenes físicos predefinidos.

Uno de los miembros de datos de la estructura de [**\_ \_ \_ información del almacén de certificados**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) es la matriz *rgpvStoreProvFunc* . Si la función de proveedor de almacén necesita admitir una o varias de las funciones de devolución de llamada, debe proporcionar punteros para esta matriz. Estos punteros deben apuntar a las funciones de devolución de llamada que se van a usar para otras actividades del almacén de certificados (por ejemplo, cerrar el almacén). En la ilustración siguiente se muestra el flujo de este proceso.

![funcionalidad de CertOpenStore](images/openstor.png)

Como se muestra en la siguiente ilustración, una vez abierto el almacén, otras funciones CryptoAPI (como [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)) utilizan la matriz de punteros para tener acceso a las funciones de devolución de llamada que realizan la tarea deseada. La definición de la estructura de [**\_ \_ \_ información del almacén de certificados**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) y los prototipos de las funciones de devolución de llamada predeterminadas que se proporcionan con CryptoAPI se muestran en funciones de devolución de llamada del proveedor del almacén de [certificados](cryptography-functions.md).

![funcionalidad de certclosestore](images/closstor.png)

Las API de almacenamiento permiten que un proveedor de almacén Mantenga los certificados, las CRL y [*las listas*](../secgloss/c-gly.md) de certificados de confianza (CTL) fuera de la caché del almacén (por ejemplo, una base de datos externa de certificados, como la proporcionada por la base de datos del servidor de certificados de Microsoft).

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) envía a través del parámetro *pszStoreProvider* a la función de proveedor instalable [**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) adecuada. El proveedor devuelve información en el parámetro *pStoreProvInfo* que apunta a una estructura de información de Prov del almacén de [**certificados \_ \_ \_**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) . La estructura de **\_ \_ \_ información del almacén de certificados** contiene un miembro **dwStoreProvFlags** . La \_ marca de marca external del almacén de certificados se ha \_ \_ \_ agregado para permitir que el proveedor indique que los certificados, las CRL y las CTL son externos a la memoria caché del almacén.

[**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) devuelve una matriz de funciones de devolución de llamada. Un proveedor puede implementar las siguientes funciones de devolución de llamada:

-   función \_ de \_ cierre de Prov de almacén de \_ certificados \_
-   función \_ de \_ \_ certificado de lectura Prov del almacén \_ \_ de certificados
-   función \_ de \_ \_ certificado de escritura de Prov de almacén \_ \_ de certificados
-   el \_ almacén de certificados \_ eliminar el \_ \_ certificado \_ FUNC
-   propiedad de certificado de conjunto de certificados del almacén de certificados \_ \_ \_ \_ \_ \_ FUNC
-   el \_ almacén de certificados \_ Prov \_ Read \_ CRL \_ FUNC
-   el almacén de certificados de la \_ \_ escritura de \_ \_ CRL \_ FUNC
-   \_FUNC. \_ eliminación \_ de \_ CRL \_ del almacén de certificados
-   \_propiedad de \_ conjunto \_ de \_ \_ propiedades CRL \_ del almacén de certificados
-   almacén de certificados \_ \_ Prov \_ Read \_ CTL \_ FUNC
-   almacén de certificados de la \_ \_ escritura de \_ \_ CTL \_ FUNC
-   el almacén de certificados de la \_ \_ eliminación de \_ \_ CTL \_ FUNC
-   función \_ de \_ \_ \_ propiedad CTL del \_ conjunto \_ de certificados del almacén de certificados

En las llamadas a las funciones de devolución de llamada de escritura de \_ certificado, escritura \_ CRL y escritura \_ CTL cuando \_ se establece la marca Add de la escritura del almacén de certificados \_ \_ \_ \_ , los 16 bits superiores del parámetro *dwFlags* contienen el valor *dwAddDisposition* . Para admitir almacenes externos, un proveedor puede implementar las siguientes funciones de devolución de llamada:

-   el \_ Prov del almacén de certificados \_ encontrar el \_ \_ certificado \_ FUNC
-   el almacén de certificados no se \_ \_ encuentra disponible en la búsqueda de \_ \_ \_ CERT \_
-   propiedad del certificado de obtención del almacén de certificados \_ \_ \_ \_ \_ \_ FUNC
-   función de CRL de la \_ \_ \_ búsqueda de \_ almacén de certificados \_
-   el almacén de certificados de la \_ \_ búsqueda de \_ \_ \_ CRL Free \_
-   función \_ de \_ \_ propiedad de \_ CRL de obtención \_ \_ de almacén de certificados
-   función \_ de \_ \_ \_ CTL \_ de aprovisionamiento de almacén de certificados
-   almacén de certificados de la \_ \_ búsqueda de \_ \_ CTL Free \_ \_ FUNC
-   función de la \_ \_ \_ propiedad de \_ CTL obtener CTL \_ \_ del almacén de certificados

Las funciones de devolución de llamada de certificado tienen las siguientes firmas:

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

Las firmas de las funciones de devolución de llamada de CTL y CTL son idénticas a las anteriores con el puntero al [**\_ contexto de certificado**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) reemplazado con un puntero a un [**\_ contexto de CRL**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) o de [**CTL \_**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context).

\_Se llama a la devolución de llamada de búsqueda de certificado cuando las API de almacenamiento enumeran, buscan o agregan certificados. *pPrevCertContext* y *ppvStoreProvFindInfo* se establecen en **null** para iniciar una nueva búsqueda. La *ppvStoreProvFindInfo* devuelta se vuelve a pasar en la siguiente búsqueda en el momento en el que el proveedor puede liberarla. El proveedor puede establecer todas las propiedades del certificado, algunas o ninguna de ellas. El proveedor tiene la opción de diferir hasta que \_ \_ se llame a la devolución de llamada de la propiedad Get cert. Se recomienda que los proveedores establezcan tantas propiedades como sea posible para permitir la copia en otro almacén.

Los siguientes tipos de búsqueda de certificado se admiten en [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore):

-   CERT \_ Buscar \_ any
-   CERTIFICADO de \_ búsqueda de \_ \_ hash SHA1
-   CERTIFICADO de \_ búsqueda \_ MD5 \_ hash
-   \_propiedad de búsqueda de certificado \_
-   CERTIFICADO de \_ búsqueda de \_ \_ clave pública
-   \_nombre del \_ firmante de búsqueda de certificado \_
-   CERTIFICADO \_ Buscar \_ atributo de asunto \_
-   \_nombre de \_ emisor de búsqueda de certificado \_
-   CERT \_ Buscar el \_ atributo issuer \_
-   CERT \_ Buscar \_ asunto \_ Str \_ A
-   CERT \_ Buscar \_ asunto \_ Str \_ W
-   CERTIFICADO \_ \_ de búsqueda de emisores \_ Str \_ A
-   CERTIFICADO de \_ búsqueda de \_ emisores en \_ Str \_ W
-   \_especificación de \_ clave de búsqueda de certificado \_
-   uso del certificado de \_ búsqueda de \_ ENHKEY \_

\_Se llama a la devolución de llamada de buscar certificado para cada uno de los tipos de búsqueda anteriores. Los parámetros que se pasan a [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) se copian directamente en la \_ estructura del Prov. buscar información del almacén de certificados \_ \_ \_ antes de que se llame a la devolución de llamada de búsqueda de \_ certificado. Para obtener más información acerca de los valores de campo de los diferentes tipos de búsqueda de la estructura de información de la búsqueda del almacén de certificados \_ \_ \_ \_ , vea **CertFindCertificateInStore**.

Los siguientes tipos de búsqueda de certificado admiten las API [**CertGetSubjectCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) y [**CertGetIssuerCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore) y ayudan a determinar si el certificado ya existe en el almacén antes de agregar:

-   certificado de \_ búsqueda \_ de certificado \_
-   \_ \_ emisor \_ de búsqueda de certificado de
-   CERTIFICADO \_ encontrar \_ existente

En el caso de CERT \_ \_ \_ , busque CERT, el parámetro *pvFindPara* apunta a una estructura de [**\_ información de certificado**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_info) que contiene el emisor y la SerialNumber del sujeto. En el caso del \_ \_ emisor \_ de la búsqueda de certificados, *pvFindPara* apunta a una estructura de [**\_ contexto de certificado**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) del sujeto. En el caso de CERT \_ Find \_ Existing, *pvFindPara* apunta a un **\_ contexto** de certificado del certificado para comprobar su existencia en el almacén.

\_ \_ Se llama a la devolución de llamada de búsqueda de certificado gratuita cuando el certificado devuelto por la devolución de llamada de búsqueda \_ de certificado no se liberó por su uso en un siguiente certificado de búsqueda posterior \_ , por lo que su [*recuento de referencias*](../secgloss/r-gly.md) se ha reducido a cero o porque se ha liberado mediante una llamada a [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore). Antes de que se llame a la devolución de llamada de cierre, todos los certificados devueltos por la devolución de llamada de FIND \_ CERT deben liberarse en el proveedor pasando a una llamada a la devolución de llamada de búsqueda de certificado \_ o una llamada a la \_ devolución de llamada de búsqueda de certificado gratuita \_ . Lo mismo se aplica a las devoluciones de llamada CRL y CTL.

\_ \_ [**CertGetCertificateContextProperty**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) llama a la devolución de llamada de la propiedad Get CERT si no encuentra la propiedad especificada para el parámetro *pCertContext* . Lo mismo se aplica a la \_ propiedad Get CRL \_ y a la \_ propiedad Get CTL \_ .

\_Se llama a la devolución de llamada de la CRL de búsqueda cuando las API de almacén enumeran u obtienen CRL y antes de agregar una CRL. Se definirán los siguientes tipos de búsqueda de CRL:

En el caso de \_ la búsqueda de CRL \_ emitida \_ por, *pvFindPara* es un puntero a un [**\_ contexto de certificado**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) del emisor de CRL. En el caso de \_ la CRL buscar \_ existente, *pvFindPara* es un puntero a un [**\_ contexto de CRL**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) de la CRL para determinar si ya existe en el almacén.

\_Se llama a la devolución de llamada de búsqueda CTL cuando las API de almacenamiento enumeran o buscan CTL. Los siguientes tipos de búsqueda de CTL se admiten en [**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore):

-   CTL \_ Buscar \_ cualquiera
-   CTL \_ Buscar \_ \_ hash SHA1
-   CTL \_ Buscar \_ \_ hash MD5
-   CTL \_ Buscar \_ uso
-   CTL \_ Buscar \_ asunto
-   CTL \_ Buscar \_ existente

\_Se llama a la devolución de llamada de búsqueda CTL para cada uno de los tipos de búsqueda anteriores. Los parámetros que se pasan a [**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore) se copian directamente en la \_ estructura del Prov. buscar información del almacén de certificados \_ \_ \_ antes de que se llame a la devolución de llamada de búsqueda \_ CTL. Para obtener más información acerca de los valores de campo de los diferentes tipos de búsqueda de la estructura de información de la búsqueda del almacén de certificados \_ \_ \_ \_ , vea **CertFindCTLInStore**.

El \_ tipo de \_ búsqueda CTL existente buscar CTL ayuda a determinar si la CTL ya existe en el almacén antes de realizar una operación de agregar CTL.

En la \_ búsqueda de CTL \_ existente, *pvFindPara* es un puntero a la estructura de [**\_ contexto CTL**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context) de la CTL para determinar si ya existe en el almacén.

 

 
