---
description: Enumera las interfaces proporcionadas por CryptoAPI.
ms.assetid: f94f0264-78b8-4a28-9d3a-dda55db29897
title: Interfaces criptográficas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccf5284f5c2107e741fd91e2936ff3dea0853e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360225"
---
# <a name="cryptography-interfaces"></a>Interfaces criptográficas

Las interfaces criptográficas se clasifican en función del uso como se indica a continuación:

-   [Interfaces de exportación del motor de servidor](#server-engine-export-interfaces)
-   [Interfaces de importación de motor de servidor](#server-engine-import-interfaces)
-   [Interfaces de codificación](#encoding-interfaces)
-   [Interfaces de inscripción de certificados](#certificate-enrollment-interfaces)
-   [Interfaces de interoperabilidad de CAPICOM](#capicom-interoperability-interfaces)

## <a name="server-engine-export-interfaces"></a>Interfaces de exportación del motor de servidor

En el siguiente tema de referencia se describen las interfaces exportadas por el motor del servidor y llamadas por objetos externos.



| Interfaz                                                                | Descripción                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin)                                         | Lo usan los programas de administración para administrar solicitudes, certificados y revocación.                                                                                                                                                              |
| [**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2)                                       | Lo usan los programas de administración para administrar solicitudes, certificados y revocación. Reemplaza [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin).                                                                                                                 |
| [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)                                       | Lo usan los clientes para obtener información acerca de los servidores disponibles.                                                                                                                                                                                 |
| [**ICertConfig2**](/windows/desktop/api/Certcli/nn-certcli-icertconfig2)                                     | Lo usan los clientes para obtener información acerca de los servidores disponibles. Reemplaza [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig).                                                                                                                                  |
| [**ICertGetConfig**](/windows/desktop/api/Certcli/nn-certcli-icertgetconfig)                                 | Proporciona funcionalidad para recuperar los datos de configuración públicos (especificados durante la instalación del cliente) para un servidor de servicios de servidor de [*certificados*](../secgloss/c-gly.md) .                |
| [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest)                                     | Se usa para enviar una solicitud al servidor y obtener los resultados de la solicitud.                                                                                                                                                                        |
| [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2)                                   | Se usa para enviar una solicitud al servidor y obtener los resultados de la solicitud. Reemplaza la [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest).                                                                                                                       |
| [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit)                               | Lo usan los [módulos de salida](exit-modules.md) para obtener las propiedades del certificado y de la solicitud.                                                                                                                                                             |
| [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy)                           | Lo usa el [módulo de directivas](policy-modules.md) para obtener y establecer propiedades de certificado y solicitud.                                                                                                                                              |
| [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview)                                           | Lo usan los clientes para [ver la base de datos de servicios de certificados](viewing-the-certificate-services-database.md).                                                                                                                                 |
| [**ICertView2**](/windows/desktop/api/Certview/nn-certview-icertview2)                                         | Lo usan los clientes para ver la base de datos de servicios de certificados. Reemplaza [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview).                                                                                                                                       |
| [**IEnumCERTVIEWATTRIBUTE**](/windows/desktop/api/Certview/nn-certview-ienumcertviewattribute)                 | Lo usan los clientes para tener acceso a los atributos de certificado de una fila en la vista servicios de Certificate Server.                                                                                                                                                |
| [**IEnumCERTVIEWCOLUMN**](/windows/desktop/api/Certview/nn-certview-ienumcertviewcolumn)                       | Lo usan los clientes para tener acceso a las columnas de datos de una fila en la vista servicios de Certificate Server.                                                                                                                                                           |
| [**IEnumCERTVIEWEXTENSION**](/windows/desktop/api/Certview/nn-certview-ienumcertviewextension)                 | Lo usan los clientes para tener acceso a los datos de la extensión de certificado de una fila en la vista servicios de Certificate Server.                                                                                                                                            |
| [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow)                             | Lo usan los clientes para enumerar las filas de la vista de servicios de certificados.                                                                                                                                                                         |
| [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin)                                         | Lo usan los programas de administración para configurar los servidores de respuesta del Protocolo de estado de certificados en línea (OCSP).                                                                                                                                       |
| [**IOCSPCAConfiguration**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfiguration)                     | Proporciona funcionalidad para configurar un servicio de respuesta de OCSP para controlar las solicitudes de estado de una [*entidad de certificación*](../secgloss/c-gly.md) (CA) específica.<br/> |
| [**IOCSPCAConfigurationCollection**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfigurationcollection) | Proporciona funcionalidad para administrar las configuraciones de CA para las que un servicio de respuesta de OCSP puede controlar las solicitudes.                                                                                                                                 |
| [**IOCSPProperty**](/windows/desktop/api/Certadm/nn-certadm-iocspproperty)                                   | Proporciona funcionalidad para configurar un atributo de servidor de respuesta de OCSP.                                                                                                                                                                         |
| [**IOCSPPropertyCollection**](/windows/desktop/api/Certadm/nn-certadm-iocsppropertycollection)               | Lo usan los programas de administración para administrar los atributos del servidor de respuesta de OCSP.                                                                                                                                                                     |



 

## <a name="server-engine-import-interfaces"></a>Interfaces de importación de motor de servidor

En los temas de referencia siguientes se describen las interfaces que importa el motor del servidor.



| Interfaz                                      | Descripción                                                                                                                            |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit)                 | Exportados por los módulos de salida. Lo usa el motor del servidor para proporcionar los certificados terminados y la información de revocación.                       |
| [**ICertExit2**](/windows/desktop/api/Certexit/nn-certexit-icertexit2)               | Agrega el método [**GetManageModule**](/windows/desktop/api/Certexit/nf-certexit-icertexit2-getmanagemodule) a [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit).                               |
| [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) | Exportados por los módulos de directivas o de salida. Se usa para mostrar información del módulo o para mostrar una interfaz de usuario para la configuración del módulo. |
| [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy)             | Exportado por el módulo de directivas. Lo usa el motor del servidor para comprobar las solicitudes y obtener las propiedades de los certificados.                        |
| [**ICertPolicy2**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy2)           | Agrega el método [**GetManageModule**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy2-getmanagemodule) a [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy).                         |



 

## <a name="encoding-interfaces"></a>Interfaces de codificación

En los temas de referencia siguientes se describen las interfaces que los [controladores de extensión](writing-custom-extension-handlers.md) pueden exportar y que el módulo de directivas importa.



| Interfaz                                                | Descripción                                                                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname)         | Lo usa el [módulo de directivas](policy-modules.md) para administrar extensiones de nombre alternativas.                                                                                                                                                          |
| [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring)     | Lo usa el módulo de directivas para controlar las cadenas de bits usadas en las extensiones de certificado.                                                                                                                                                               |
| [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo) | Lo usa el módulo de directivas para controlar las matrices de información de distribución de [*lista de revocación de certificados*](../secgloss/c-gly.md) (CRL) utilizadas en las extensiones de certificado. |
| [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray)     | Lo usa el módulo de directivas para controlar las matrices de **fechas** usadas en las extensiones de certificado.                                                                                                                                                           |
| [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)     | Lo usa el módulo de directivas para controlar las matrices **largas** usadas en las extensiones de certificado.                                                                                                                                                           |
| [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray) | Lo usa el módulo de directivas para controlar las matrices de **cadenas** usadas en las extensiones de certificado.                                                                                                                                                         |



 

## <a name="certificate-enrollment-interfaces"></a>Interfaces de inscripción de certificados

En esta sección se describen los objetos, los métodos y las propiedades del control de inscripción de certificados y el objeto, los métodos y las propiedades disponibles en el control de inscripción de tarjetas inteligentes. Entre ellas se incluyen las siguientes interfaces.



| Interfaz                                                                                  | Descripción                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll)                                                               | Una de varias interfaces que representan el control de inscripción de certificados. Es principalmente interesante si no está utilizando la automatización.                                                                        |
| [**ICEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll2)                                                             | Una de varias interfaces que representan el control de inscripción de certificados. Es principalmente interesante si no está utilizando la automatización.                                                                        |
| [**ICEnroll3**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll3)                                                             | Una de varias interfaces que representan el control de inscripción de certificados. Es principalmente interesante si no está utilizando la automatización.                                                                        |
| [**ICertificateEnrollmentPolicyServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentpolicyserversetup) | Representa el servicio Web de directiva de inscripción de certificados (CEP) en Active Directory servicios de Certificate Server (ADCS). El servicio permite a los usuarios y equipos obtener información sobre directivas de inscripción de certificados. |
| [**ICertificateEnrollmentServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentserversetup)             | Representa el Servicio web de inscripción de certificados (CES) en ADCS. El servicio permite a los usuarios y equipos inscribir y renovar certificados.                                                               |
| [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4)                                                             | Una de varias interfaces que representan el control de inscripción de certificados. Es principalmente interesante si no está utilizando la automatización.                                                                        |
| [**IEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll)                                                                 | Una de varias interfaces que representan el control de inscripción de certificados. La interfaz es principalmente interesante si no está utilizando la automatización.                                                             |
| [**IEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll2)                                                               | Una de varias interfaces que representan el control de inscripción de certificados. La interfaz es principalmente interesante si no está utilizando la automatización.                                                             |
| [**IEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll4)                                                               | Una de varias interfaces que representan el control de inscripción de certificados. La interfaz es principalmente interesante si no está utilizando la automatización.                                                             |
| [**ISCrdEnr**](iscrdenr.md)                                                               | Representa el control de inscripción de tarjetas inteligentes. Es principalmente interesante si no está utilizando la automatización.                                                                                                       |



 

## <a name="capicom-interoperability-interfaces"></a>Interfaces de interoperabilidad de CAPICOM

En los temas de referencia siguientes se describen las interfaces que permiten que las derivaciones de CryptoAPI funcionen conjuntamente con CAPICOM 2,0.



| Interfaz                              | Descripción                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Proporciona acceso al contexto de un objeto de [**certificado**](certificate.md) de CAPICOM X. 509v3. Este contexto permite usar el certificado de CAPICOM en otras derivaciones de CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Proporciona acceso al contexto de un objeto de [**almacén**](store.md) de CAPICOM. Este contexto permite usar el almacén de certificados de CAPICOM en otras derivaciones de CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Proporciona acceso al contexto de un objeto de [**cadena**](chain.md) CAPICOM. Este contexto permite usar la cadena de confianza de certificados de CAPICOM en otras derivaciones de CryptoAPI.         |



 

 

 
