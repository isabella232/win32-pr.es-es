---
description: Representa un único certificado digital.
ms.assetid: da95312b-cc9f-44f0-9517-0b28c5fcfb61
title: Objeto de certificado
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1360b197f0d7f5e0579a5378a37047e6a117a9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690394"
---
# <a name="certificate-object"></a>Objeto de certificado

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El objeto de **certificado** representa un único [*certificado digital*](../secgloss/d-gly.md).

El objeto de **certificado** expone las siguientes interfaces:

-   **ICertificate** : introducido en CAPICOM 1,0.
-   **ICertificate2** : introducido en CAPICOM 2,0.

## <a name="when-to-use"></a>Cuándo se usa

El objeto de **certificado** se usa para realizar las siguientes tareas:

-   Cargue los datos del certificado, incluida la clave privada, de un archivo.
-   Obtiene información del certificado.
-   Devolver restricciones básicas, EKU, propiedades extendidas, extensiones, uso de claves, clave pública y objetos de plantilla asociados al certificado.
-   Determine si el certificado es válido y Compruebe la disponibilidad de acceso de la clave privada del sujeto del certificado.
-   Mostrar el certificado.
-   Importe y exporte el certificado.
-   Guarde el certificado en un archivo.
-   Recupera o establece las propiedades que describen el certificado.

## <a name="members"></a>Miembros

El objeto de **certificado** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto de **certificado** tiene estos métodos.



| Método                                                       | Descripción                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BasicConstraints**](certificate-basicconstraints.md)     | Devuelve un objeto [**BasicConstraints**](basicconstraints.md) que representa la extensión de restricciones básicas del certificado.<br/> (Se hereda de **CertificateICertificate2ICertificate**)                                                   |
| [**Muestra**](certificate-display.md)                       | Muestra un certificado.<br/> (Se hereda de **CertificateICertificate2ICertificate**)                                                                                                                                                             |
| [**Exportación**](certificate-export.md)                         | Copia un certificado en una cadena codificada. La cadena codificada puede escribirse en un archivo o importarse en un nuevo objeto de **certificado** .<br/> (Se hereda de **CertificateICertificate2ICertificate**)                                               |
| [**ExtendedKeyUsage**](certificate-extendedkeyusage.md)     | Devuelve un objeto [**ExtendedKeyUsage**](extendedkeyusage.md) que indica los usos de clave extendida válidos del certificado.<br/> (Se hereda de **CertificateICertificate2ICertificate**)                                                       |
| [**ExtendedProperties**](certificate-extendedproperties.md) | Devuelve una colección de las propiedades extendidas del certificado.<br/> (Se hereda de **CertificateICertificate2**)                                                                                                                             |
| [**Extensiones**](certificate-extensions.md)                 | Devuelve una colección de las extensiones asociadas al certificado.<br/> (Se hereda de **CertificateICertificate2**)                                                                                                                         |
| [**GetInfo**](certificate-getinfo.md)                       | Recupera información del certificado.<br/> (Se hereda de **CertificateICertificate2ICertificate**)                                                                                                                                         |
| [**HasPrivateKey**](certificate-hasprivatekey.md)           | Determina si el certificado tiene una [*clave privada*](../secgloss/p-gly.md) asociada.<br/> (Se hereda de **CertificateICertificate2ICertificate**)                                    |
| [**Importar**](certificate-import.md)                         | Importa un certificado previamente codificado de una cadena en el objeto de **certificado** .<br/> (Se hereda de **CertificateICertificate2ICertificate**)                                                                                             |
| [**IsValid**](certificate-isvalid.md)                       | Crea una cadena de comprobación de certificados para un certificado y devuelve un objeto [**CertificateStatus**](certificatestatus.md) que contiene el estado de validez del certificado.<br/> (Se hereda de **CertificateICertificate2ICertificate**) |
| [**KeyUsage**](certificate-keyusage.md)                     | Devuelve un objeto [**KeyUsage**](keyusage.md) que indica el uso de clave válido del certificado.<br/> (Se hereda de **CertificateICertificate2ICertificate**)                                                                                |
| [**Cargar**](certificate-load.md)                             | Importa un certificado de un archivo.<br/> (Se hereda de **CertificateICertificate2**)                                                                                                                                                              |
| [**PublicKey**](certificate-publickey.md)                   | Devuelve un objeto [**publicKey**](publickey.md) .<br/> (Se hereda de **CertificateICertificate2**)                                                                                                                                                |
| [**Guardar**](certificate-save.md)                             | Guarda el certificado en un archivo.<br/> (Se hereda de **CertificateICertificate2**)                                                                                                                                                                |
| [**Plantilla**](certificate-template.md)                     | Devuelve la plantilla asociada al certificado.<br/> (Se hereda de **CertificateICertificate2**)                                                                                                                                           |



 

### <a name="properties"></a>Propiedades

El objeto de **certificado** tiene estas propiedades.



| Propiedad                                                      | Tipo de acceso           | Descripción                                                                                                                                          |
|:--------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Archivado**](certificate-archived.md)<br/>           | Lectura/escritura<br/> | Establece o recupera un valor booleano que indica si el certificado se ha archivado.<br/> (Se hereda de **CertificateICertificate2**)       |
| [**IssuerName**](certificate-issuername.md)<br/>       | Solo lectura<br/>  | Recupera una cadena que contiene el nombre del emisor del certificado.<br/> (Se hereda de **CertificateICertificate2ICertificate**)            |
| [**PrivateKey**](certificate-privatekey.md)<br/>       | Lectura/escritura<br/> | Establece o recupera la clave privada asociada al certificado.<br/> (Se hereda de **CertificateICertificate2**)                          |
| [**SerialNumber**](certificate-serialnumber.md)<br/>   | Solo lectura<br/>  | Recupera una cadena que contiene el número de serie del certificado.<br/> (Se hereda de **CertificateICertificate2ICertificate**)                 |
| [**SubjectName**](certificate-subjectname.md)<br/>     | Solo lectura<br/>  | Recupera una cadena que contiene el nombre del sujeto del certificado.<br/> (Se hereda de **CertificateICertificate2ICertificate**)           |
| [**Huella**](certificate-thumbprint.md)<br/>       | Solo lectura<br/>  | Recupera una cadena hexadecimal que contiene el hash SHA-1 del certificado.<br/> (Se hereda de **CertificateICertificate2ICertificate**) |
| [**ValidFromDate**](certificate-validfromdate.md)<br/> | Solo lectura<br/>  | Recupera la fecha de inicio de la validez del certificado.<br/> (Se hereda de **CertificateICertificate2ICertificate**)               |
| [**ValidToDate**](certificate-validtodate.md)<br/>     | Solo lectura<br/>  | Recupera la fecha de finalización de la validez del certificado.<br/> (Se hereda de **CertificateICertificate2ICertificate**)                  |
| [**Versión**](certificate-version.md)<br/>             | Solo lectura<br/>  | Recupera el número de versión del certificado.<br/> (Se hereda de **CertificateICertificate2ICertificate**)                                |



 

## <a name="remarks"></a>Observaciones

Se puede crear el objeto de **certificado** y es seguro para el scripting. El ProgID del objeto de **certificado** es "CAPICOM. Certificate. 2 ".

**CAPICOM 1. *x*:** el ProgID del objeto de **certificado** es "CAPICOM. Certificate. 1 ".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
