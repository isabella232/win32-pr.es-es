---
description: Las propiedades de nombre son propiedades de certificados y solicitudes de certificado que representan datos sobre el sujeto, es decir, el propietario del certificado o la persona para la que se solicita un certificado.
ms.assetid: c32756f7-4431-410e-ab3a-c7b748a43829
title: Propiedades de nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28765f0c278678ed5bdca9ef8547c1c6dc85ca7b6b343b229441b4b777eac688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425315"
---
# <a name="name-properties"></a>Propiedades de nombre

Las propiedades de nombre son propiedades de certificados y solicitudes de certificado que representan datos sobre el sujeto, es decir, el propietario del certificado o la persona para la que se solicita un certificado. Cada propiedad name se identifica mediante un nombre de propiedad. Estos nombres no son localizables; Sin embargo, las propiedades de nombre normalmente corresponden a una columna de base de datos de Servicios de certificados y puede usar el complemento MMC de la entidad de certificación, la herramienta de línea de comandos "certutil -schema" o el método [**IEnumCERTVIEWCOLUMN::GetDisplayName**](/windows/desktop/api/Certview/nf-certview-ienumcertviewcolumn-getdisplayname) para mostrar versiones localizadas de los nombres de columna de base de datos.

El nombre de propiedad (pero no los alias) puede tener "Subject". como prefijo opcional. Por ejemplo, para hacer referencia al nombre común del sujeto, puede usar "CommonName" o "Subject.CommonName".

Además de su nombre, cada propiedad tiene algún número de alias que Certificate Services reconoce como nombres alternativos para la propiedad. Tenga en [*cuenta que los identificadores*](../secgloss/o-gly.md) de objeto (OID) son alias aceptables, al igual que las **constantes \_ \* *szOID_. Estas constantes son definiciones (en Wincrypt.h) que representan los OD. Por ejemplo, _* szOID \_ COMMON \_ NAME** se define como "2.5.4.3". Por lo tanto, puede usar las **constantes szOID \_ \*** como alias en lugar de los OID que representan.



| Nombre de propiedad                 | Alias                                                                                                                                                        | Tipo de datos                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Subject.CommonName"          | "CommonName" "CN"<br/> "2.5.4.3"<br/> **szOID \_ COMMON \_ NAME**<br/>                                                                           | **Cadena** (máximo 64 caracteres)  | Para los certificados de usuario, el nombre completo de la persona. Para los certificados de equipo, la ruta de acceso completa hostName* usada en las búsquedas del Sistema de nombres de dominio ***/**  (DNS) (por ejemplo, *HostName*). _Ejemplo_* _.com_*).<br/>                                                                                                                                                                                                                                                                        |
| "Subject.Country"             | "Country" "C"<br/> "2.5.4.6"<br/> **szOID \_ COUNTRY \_ NAME**<br/>                                                                              | **Cadena** (máximo 2 caracteres)    | País o región del sujeto. Se trata de un [*código X.500*](../secgloss/x-gly.md) de país o región de dos caracteres (por ejemplo, EE. UU. para Estados Unidos o CA para Canadá).<br/> Muchos de estos códigos de dos caracteres se definen en el estándar ISO 3166. Además, el código de la configuración regional actual está disponible mediante una llamada a la función Windows [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) (especificando un *LCType* de LOCALE \_ SISO3166CTRYNAME).<br/> |
| "Subject.DeviceSerialNumber"  | "DeviceSerialNumber" "2.5.4.5"<br/> **szOID \_ DEVICE \_ SERIAL \_ NUMBER**<br/>                                                                         | **Cadena** (máximo 1024 caracteres) | Número de serie del dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject.DomainComponent"     | "DomainComponent" "DC"<br/> "0.9.2342.19200300.100.1.25"<br/> **szOID \_ DOMAIN \_ COMPONENT**<br/>                                              | **Cadena** (máximo 128 caracteres)  | Componente de un nombre de sistema de nombres de dominio (DNS).                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject.EMail"               | "EMail" "E"<br/> "1.2.840.113549.1.9.1"<br/> **szOID \_ RSA \_ emailAddr**<br/>                                                                  | **Cadena** (máximo 128 caracteres)  | Dirección de correo electrónico (por ejemplo, someone@example.com "").                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject.GivenName"           | "GivenName" "G"<br/> "2.5.4.42"<br/> **szOID \_ GIVEN \_ NAME**<br/>                                                                             | **Cadena** (máximo 16 caracteres)   | Nombre del asunto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| "Subject.Initials"            | "Initials" "I"<br/> "2.5.4.43"<br/> **szOID \_ INITIALS**<br/>                                                                                 | **Cadena** (máximo 5 caracteres)    | Iniciales del asunto (opcional).                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject.Locality"            | "Locality" "L"<br/> "2.5.4.7"<br/> **szOID \_ LOCALITY \_ NAME**<br/>                                                                            | **Cadena** (máximo 128 caracteres)  | Nombre de la ciudad del sujeto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| "Subject.Organization"        | "Organización" "Org"<br/> "O"<br/> "2.5.4.10"<br/> **szOID \_ ORGANIZATION \_ NAME**<br/>                                                  | **Cadena** (máximo 64 caracteres)   | Nombre legal de la organización del sujeto.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Subject.OrgUnit"             | "OrgUnit" "OrganizationUnit"<br/> "OrganizationalUnit"<br/> "OU"<br/> "2.5.4.11"<br/> **szOID \_ ORGANIZATIONAL \_ UNIT \_ NAME**<br/> | **Cadena** (máximo 64 caracteres)   | Nombre de la sub organización o departamento del sujeto.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject.State"               | "State" "ST"<br/> "S"<br/> "2.5.4.8"<br/> **szOID \_ STATE OR PROVINCE \_ \_ \_ NAME**<br/>                                                    | **Cadena** (máximo 128 caracteres)  | Nombre completo del estado o provincia del sujeto (por ejemplo, California).                                                                                                                                                                                                                                                                                                                                                                                                                         |
| "Subject.StreetAddress"       | "StreetAddress" "Street"<br/> "2.5.4.9"<br/> **szOID \_ STREET \_ ADDRESS**<br/>                                                                 | **Cadena** (máximo 30 caracteres)   | Dirección postal del sujeto o cuadro de pedido de compra.                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject.SurName"             | "SurName" "SN"<br/> "2.5.4.4"<br/> **szOID \_ SUR \_ NAME**<br/>                                                                                 | **Cadena** (máximo 40 caracteres)   | Apellidos del sujeto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Subject.Title"               | "Title" "T"<br/> "2.5.4.12"<br/> **szOID \_ TITLE**<br/>                                                                                       | **Cadena** (máximo 64 caracteres)   | Título de la persona que solicitó el certificado (opcional).                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject.UnstructuredAddress" | "UnstructuredAddress" "1.2.840.113549.1.9.8"<br/> **szOID \_ RSA \_ unstructAddr**<br/>                                                                | **Cadena** (máximo 1024 caracteres) | Dirección no estructurada.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject.UnstructuredName"    | "UnstructuredName" "1.2.840.113549.1.9.2"<br/> **szOID \_ RSA \_ unstructName**<br/>                                                                   | **Cadena** (máximo 1024 caracteres) | Nombre no estructurado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

Las siguientes propiedades están relacionadas con el asunto, aunque no son propiedades de nombre. El módulo de directivas no puede establecer estas propiedades directamente.



| Propiedad                    | Tipo de datos                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Request.DistinguishedName" | **Cadena** (máximo 8192 caracteres) | Nombre [*distintivo relativo de la*](../secgloss/r-gly.md) solicitud, una representación textual del asunto en la solicitud. Esta representación consta de propiedades de nombre, por ejemplo, "CN=MyName, OU=MyOrgUnit, C=US". La aplicación Servicios de certificados establece esta propiedad antes de llamar al módulo de directivas mediante una llamada [**a CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) mediante el asunto de RawRequest. |
| "Request.RawName"           | **Binario** (máximo 4096 bytes) | [*Notación de sintaxis abstracta 1*](../secgloss/a-gly.md) (ASN.1) [*blob*](../secgloss/b-gly.md) de asunto binario extraído de la solicitud. La aplicación Servicios de certificados establece esta propiedad antes de llamar al módulo de directivas; Su valor viene determinado por el asunto de RawRequest.                                                                                     |
| "DistinguishedName"         | **Cadena** (máximo 8192 caracteres) | Nombre distintivo relativo del certificado, una representación textual del asunto en el certificado. Esta representación consta de propiedades de nombre, por ejemplo, "CN=MyName, OU=MyOrgUnit, C=US". La aplicación Servicios de certificados establece esta propiedad después de llamar al módulo de directivas, llamando [**a CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) mediante RawName.                                                                                                               |
| "RawName"                   | **Binario** (máximo 4096 bytes) | [*BLOB*](../secgloss/b-gly.md) de asunto binario de ASN.1 usado para construir el certificado. La aplicación Servicios de certificados establece esta propiedad después de llamar al módulo de directivas; Su valor viene determinado por los valores de propiedades de nombre específicas (Subject.CommonName, entre otras) según lo indicado por SubjectTemplate.                                                                                                                                        |



 

Los [*componentes de*](../secgloss/r-gly.md) nombre distintivo relativos que aparecen en la propiedad DistinguishedName y el orden en que aparecen se controlan mediante el valor del Registro "SubjectTemplate" incluido en la siguiente clave del Registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            CertSvc
               Configuration
                  CaName
```

Cuando Servicios de certificados analiza los nombres [*de*](../secgloss/a-gly.md) atributo, omite los espacios, los guiones (signos menos) y las mayúsculas y minúsculas. Por ejemplo, "AttributeName1", "Attribute Name1" y "Attribute-name1" son equivalentes. Para los valores de atributo, Certificate Services omite los espacios en blanco iniciales y finales.

Todas las propiedades anteriores, excepto DistinguishedName, RawName y Subject.Country, admiten la sintaxis de varios valores mediante un carácter de nueva línea. El separador de nueva línea no se puede deshabilitar ni cambiar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del certificado](certificate-properties.md)
</dt> <dt>

[**ICertServerExit::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> <dt>

[**ICertServerExit::GetRequestProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getrequestproperty)
</dt> <dt>

[**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**ICertServerPolicy::GetRequestProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getrequestproperty)
</dt> <dt>

[**ICertServerPolicy::SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty)
</dt> </dl>

 

 
