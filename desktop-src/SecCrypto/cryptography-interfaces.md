---
description: Enumera las interfaces proporcionadas por CryptoAPI.
ms.assetid: f94f0264-78b8-4a28-9d3a-dda55db29897
title: Interfaces de criptografía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5937dce6da8ffa3396c885d00c895b845de9889c2688c6daef4eba5db0beb90b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876105"
---
# <a name="cryptography-interfaces"></a>Interfaces de criptografía

Las interfaces de criptografía se clasifican según el uso como se muestra a continuación:

-   [Interfaces de exportación del motor de servidor](#server-engine-export-interfaces)
-   [Interfaces de importación del motor de servidor](#server-engine-import-interfaces)
-   [Interfaces de codificación](#encoding-interfaces)
-   [Interfaces de inscripción de certificados](#certificate-enrollment-interfaces)
-   [Interfaces de interoperabilidad capicom](#capicom-interoperability-interfaces)

## <a name="server-engine-export-interfaces"></a>Interfaces de exportación del motor de servidor

En el siguiente tema de referencia se describen las interfaces exportadas por el motor de servidor y a las que llaman los objetos externos.



| Interfaz                                                                | Descripción                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin)                                         | Lo usan los programas de administración para administrar solicitudes, certificados y revocaciones.                                                                                                                                                              |
| [**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2)                                       | Lo usan los programas de administración para administrar solicitudes, certificados y revocaciones. Reemplaza [**a ICertAdmin.**](/windows/desktop/api/Certadm/nn-certadm-icertadmin)                                                                                                                 |
| [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)                                       | Usado por los clientes para obtener información sobre los servidores disponibles.                                                                                                                                                                                 |
| [**ICertConfig2**](/windows/desktop/api/Certcli/nn-certcli-icertconfig2)                                     | Usado por los clientes para obtener información sobre los servidores disponibles. Reemplaza a [**ICertConfig.**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)                                                                                                                                  |
| [**ICertGetConfig**](/windows/desktop/api/Certcli/nn-certcli-icertgetconfig)                                 | Proporciona funcionalidad para recuperar los datos de configuración pública (especificados durante la instalación del cliente) para un [*servidor de Servicios de*](../secgloss/c-gly.md) certificados.                |
| [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest)                                     | Se usa para enviar una solicitud al servidor y obtener los resultados de la solicitud.                                                                                                                                                                        |
| [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2)                                   | Se usa para enviar una solicitud al servidor y obtener los resultados de la solicitud. Reemplaza a [**ICertRequest.**](/windows/desktop/api/Certcli/nn-certcli-icertrequest)                                                                                                                       |
| [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit)                               | Lo usan los [módulos de salida](exit-modules.md) para obtener las propiedades de certificado y solicitud.                                                                                                                                                             |
| [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy)                           | Lo usa el [módulo de directivas](policy-modules.md) para obtener y establecer las propiedades de certificado y solicitud.                                                                                                                                              |
| [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview)                                           | Usado por los clientes para [ver la base de datos de Servicios de certificados](viewing-the-certificate-services-database.md).                                                                                                                                 |
| [**ICertView2**](/windows/desktop/api/Certview/nn-certview-icertview2)                                         | Usado por los clientes para ver la base de datos de Servicios de certificados. Reemplaza [**a ICertView.**](/windows/desktop/api/Certview/nn-certview-icertview)                                                                                                                                       |
| [**IEnumCERTVIEWATTRIBUTE**](/windows/desktop/api/Certview/nn-certview-ienumcertviewattribute)                 | Usado por los clientes para tener acceso a los atributos de certificado de una fila en la vista Servicios de certificados.                                                                                                                                                |
| [**IEnumCERTVIEWCOLUMN**](/windows/desktop/api/Certview/nn-certview-ienumcertviewcolumn)                       | Usado por los clientes para tener acceso a las columnas de datos de una fila en la vista Servicios de certificados.                                                                                                                                                           |
| [**IEnumCERTVIEWEXTENSION**](/windows/desktop/api/Certview/nn-certview-ienumcertviewextension)                 | Usado por los clientes para acceder a los datos de extensión de certificado de una fila en la vista Servicios de certificados.                                                                                                                                            |
| [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow)                             | Usado por los clientes para enumerar las filas de la vista Servicios de certificados.                                                                                                                                                                         |
| [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin)                                         | Lo usan los programas de administración para configurar servidores de respondedor del Protocolo de estado de certificado en línea (OCSP).                                                                                                                                       |
| [**IOCSPCAConfiguration**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfiguration)                     | Proporciona funcionalidad para configurar un servicio de respondedor OCSP para controlar las solicitudes de estado de una entidad de [*certificación (CA)*](../secgloss/c-gly.md) específica.<br/> |
| [**IOCSPCAConfigurationCollection**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfigurationcollection) | Proporciona funcionalidad para administrar las configuraciones de CA para las que un servicio de respondedor OCSP puede controlar las solicitudes.                                                                                                                                 |
| [**IOCSPProperty**](/windows/desktop/api/Certadm/nn-certadm-iocspproperty)                                   | Proporciona funcionalidad para configurar un atributo de servidor del respondedor OCSP.                                                                                                                                                                         |
| [**IOCSPPropertyCollection**](/windows/desktop/api/Certadm/nn-certadm-iocsppropertycollection)               | Lo usan los programas de administración para administrar los atributos del servidor del respondedor OCSP.                                                                                                                                                                     |



 

## <a name="server-engine-import-interfaces"></a>Interfaces de importación del motor de servidor

En los temas de referencia siguientes se describen las interfaces importadas por el motor de servidor.



| Interfaz                                      | Descripción                                                                                                                            |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit)                 | Exportada por módulos de salida. Usado por el motor de servidor para entregar certificados terminados e información de revocación.                       |
| [**ICertExit2**](/windows/desktop/api/Certexit/nn-certexit-icertexit2)               | Agrega el [**método GetManageModule**](/windows/desktop/api/Certexit/nf-certexit-icertexit2-getmanagemodule) a [**ICertExit.**](/windows/desktop/api/Certexit/nn-certexit-icertexit)                               |
| [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) | Exportada por módulos de directiva o salida. Se usa para mostrar información del módulo o para mostrar una interfaz de usuario para la configuración del módulo. |
| [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy)             | Exportado por el módulo de directivas. Lo usa el motor de servidor para comprobar las solicitudes y obtener propiedades de los certificados.                        |
| [**ICertPolicy2**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy2)           | Agrega el [**método GetManageModule**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy2-getmanagemodule) a [**ICertPolicy.**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy)                         |



 

## <a name="encoding-interfaces"></a>Interfaces de codificación

En los temas de referencia siguientes se [](writing-custom-extension-handlers.md) describen las interfaces que pueden exportar los controladores de extensiones y que el módulo de directivas importa.



| Interfaz                                                | Descripción                                                                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname)         | Lo usa el [módulo de directivas](policy-modules.md) para controlar extensiones de nombre alternativas.                                                                                                                                                          |
| [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring)     | Lo usa el módulo de directivas para controlar las cadenas de bits usadas en las extensiones de certificado.                                                                                                                                                               |
| [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo) | Lo usa el módulo de directivas para controlar las matrices de información de distribución de lista de [*revocación*](../secgloss/c-gly.md) de certificados (CRL) usadas en las extensiones de certificado. |
| [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray)     | Lo usa el módulo de directivas para controlar las **matrices date** usadas en las extensiones de certificado.                                                                                                                                                           |
| [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)     | Lo usa el módulo de directivas para controlar **las matrices Long** que se usan en las extensiones de certificado.                                                                                                                                                           |
| [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray) | Lo usa el módulo de directivas para controlar las **matrices STRING** que se usan en las extensiones de certificado.                                                                                                                                                         |



 

## <a name="certificate-enrollment-interfaces"></a>Interfaces de inscripción de certificados

En esta sección se describen los objetos, métodos y propiedades del Control de inscripción de certificados y el objeto, los métodos y las propiedades disponibles en el Control de inscripción de tarjeta inteligente. Estas incluyen las interfaces siguientes.



| Interfaz                                                                                  | Descripción                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll)                                                               | Una de varias interfaces que representan el control de inscripción de certificados. Es principalmente de interés si no usa Automation.                                                                        |
| [**ICEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll2)                                                             | Una de varias interfaces que representan el control de inscripción de certificados. Es principalmente de interés si no usa Automation.                                                                        |
| [**ICEnroll3**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll3)                                                             | Una de varias interfaces que representan el control de inscripción de certificados. Es principalmente de interés si no usa Automation.                                                                        |
| [**ICertificateEnrollmentPolicyServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentpolicyserversetup) | Representa el servicio web de la directiva de inscripción de certificados (CEP) Servicios de certificados de Active Directory (ADCS). El servicio permite a los usuarios y equipos obtener información de la directiva de inscripción de certificados. |
| [**ICertificateEnrollmentServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentserversetup)             | Representa el Servicio web de inscripción de certificados (CES) dentro de ADCS. El servicio permite a los usuarios y equipos inscribirse y renovar certificados.                                                               |
| [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4)                                                             | Una de varias interfaces que representan el control de inscripción de certificados. Es principalmente de interés si no usa Automation.                                                                        |
| [**IEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll)                                                                 | Una de varias interfaces que representan el control de inscripción de certificados. La interfaz es principalmente de interés si no usa Automation.                                                             |
| [**IEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll2)                                                               | Una de varias interfaces que representan el control de inscripción de certificados. La interfaz es principalmente de interés si no usa Automation.                                                             |
| [**IEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll4)                                                               | Una de varias interfaces que representan el control de inscripción de certificados. La interfaz es principalmente de interés si no usa Automation.                                                             |
| [**ISCrdEnr**](iscrdenr.md)                                                               | Representa el control de inscripción de tarjeta inteligente. Es principalmente de interés si no usa Automation.                                                                                                       |



 

## <a name="capicom-interoperability-interfaces"></a>Interfaces de interoperabilidad capicom

En los temas de referencia siguientes se describen las interfaces que permiten que las derivaciones de CryptoAPI funcionen junto con CAPICOM 2.0.



| Interfaz                              | Descripción                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Proporciona acceso al contexto de un objeto de certificado [](certificate.md) CAPICOM X.509v3. Este contexto permite usar el certificado CAPICOM en otras derivaciones de CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Proporciona acceso al contexto de un objeto de [**almacén**](store.md) CAPICOM. Este contexto permite que el almacén de certificados CAPICOM se utilice en otras derivaciones de CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Proporciona acceso al contexto de [](chain.md) un objeto de cadena CAPICOM. Este contexto permite usar la cadena de confianza de certificados CAPICOM en otras derivaciones de CryptoAPI.         |



 

 

 
