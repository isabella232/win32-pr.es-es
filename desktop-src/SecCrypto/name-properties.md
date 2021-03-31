---
description: Las propiedades de nombre son propiedades de certificados y solicitudes de certificado que representan datos sobre el asunto, es decir, el propietario del certificado o la persona para la que se solicita un certificado.
ms.assetid: c32756f7-4431-410e-ab3a-c7b748a43829
title: Propiedades de nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c5978b3fe5ab7c6ead39840dfb1793372c5feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278800"
---
# <a name="name-properties"></a>Propiedades de nombre

Las propiedades de nombre son propiedades de certificados y solicitudes de certificado que representan datos sobre el asunto, es decir, el propietario del certificado o la persona para la que se solicita un certificado. Cada propiedad de nombre se identifica mediante un nombre de propiedad. Estos nombres no son localizables; sin embargo, las propiedades de nombre suelen corresponder a una columna de base de datos de servicios de certificados, y se puede usar el complemento MMC entidad de certificación, la herramienta de línea de comandos "certutil-Schema" o el método [**IEnumCERTVIEWCOLUMN:: getDisplayName**](/windows/desktop/api/Certview/nf-certview-ienumcertviewcolumn-getdisplayname) para mostrar versiones localizadas de los nombres de columna de la base de datos.

El nombre de la propiedad (pero no los alias) puede tener "asunto". como prefijo opcional. Por ejemplo, para hacer referencia al nombre común del sujeto, puede usar "CommonName" o "Subject. CommonName".

Además de su nombre, cada propiedad tiene un número de alias que los servicios de Certificate Server reconocen como nombres alternativos para la propiedad. Tenga en cuenta que los [*identificadores de objeto*](../secgloss/o-gly.md) (OID) son alias aceptables, como las **\_ \* *constantes szOID _. Estas constantes son definiciones (en Wincrypt. h) que representan los OID. Por ejemplo, _* szOID \_ Common \_ Name** se define como "2.5.4.3". Por consiguiente, puede usar las constantes **szOID \_ \** _ como alias en lugar de los OID que representan.



| Nombre de propiedad                 | Alias                                                                                                                                                        | Tipo de datos                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Asunto. CommonName"          | "CommonName" "CN"<br/> "2.5.4.3"<br/> _ * \_ nombre común de szOID \_ * *<br/>                                                                           | **String** (max. 64 caracteres)  | En el caso de los certificados de usuario, el nombre completo de la persona. En el caso de los certificados de equipo, *ruta de **/** _acceso_ completa de nombre de host * usada en búsquedas del sistema de nombres de dominio (DNS) (por ejemplo, *nombre de host ***.** _Ejemplo_* de _. com_*).<br/>                                                                                                                                                                                                                                                                        |
| "Asunto. país"             | "País" "C"<br/> "2.5.4.6"<br/> **szOID \_ nombre del país \_**<br/>                                                                              | **Cadena** (máximo 2 caracteres)    | País o región del sujeto. Este es un código de país o región de dos caracteres [*X. 500*](../secgloss/x-gly.md) (por ejemplo, para Estados Unidos o CA para Canadá).<br/> Muchos de estos códigos de dos caracteres se definen en el estándar ISO 3166. Además, el código de la configuración regional actual está disponible a través de una llamada a la función de Windows [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) (mediante la especificación de un *LCTYPE* de configuración regional \_ SISO3166CTRYNAME).<br/> |
| "Asunto. DeviceSerialNumber"  | "DeviceSerialNumber" "2.5.4.5"<br/> **\_número de \_ serie del dispositivo szOID \_**<br/>                                                                         | **Cadena** (máximo 1024 caracteres) | Número de serie del dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Asunto. DomainComponent"     | "DomainComponent" "DC"<br/> "0.9.2342.19200300.100.1.25"<br/> **\_componente de dominio szOID \_**<br/>                                              | **Cadena** (máximo 128 caracteres)  | Componente de un nombre de sistema de nombres de dominio (DNS).                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject.EMail"               | "Correo electrónico" "E"<br/> "1.2.840.113549.1.9.1"<br/> **szOID \_ RSA \_ emailAddr**<br/>                                                                  | **Cadena** (máximo 128 caracteres)  | Dirección de correo electrónico (por ejemplo, " someone@example.com ").                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Asunto. GivenName"           | "GivenName" "G"<br/> "2.5.4.42"<br/> **szOID \_ nombre de pila \_**<br/>                                                                             | **Cadena** (16 caracteres como máximo)   | Nombre del sujeto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| "Subject.Initials"            | "Iniciales" "I"<br/> "2.5.4.43"<br/> **iniciales de szOID \_**<br/>                                                                                 | **Cadena** (5 caracteres como máximo)    | Iniciales del asunto (opcional).                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Asunto. localidad"            | "Localidad" "L"<br/> "2.5.4.7"<br/> **szOID \_ nombre de localidad \_**<br/>                                                                            | **Cadena** (máximo 128 caracteres)  | Nombre de la ciudad del sujeto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| "Asunto. organización"        | "Organización" "org"<br/> Aceptar<br/> "2.5.4.10"<br/> **nombre de la organización de szOID \_ \_**<br/>                                                  | **Cadena** (máximo 64 caracteres)   | Nombre legal de la organización del firmante.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Asunto. unidad organizativa"             | "Unidad organizativa" "OrganizationUnit"<br/> OrganizationalUnit<br/> ORGANIZA<br/> 2.5.4.11<br/> **\_nombre de \_ unidad \_ organizativa de szOID**<br/> | **Cadena** (máximo 64 caracteres)   | Nombre de la suborganización o departamento del sujeto.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Asunto. estado"               | "Estado" "ST"<br/> Seg<br/> "2.5.4.8"<br/> **\_ \_ nombre de estado o \_ provincia de \_ szOID**<br/>                                                    | **Cadena** (máximo 128 caracteres)  | Nombre completo del estado o provincia del sujeto (por ejemplo, California).                                                                                                                                                                                                                                                                                                                                                                                                                         |
| "Asunto. StreetAddress"       | "StreetAddress" "calle"<br/> "2.5.4.9"<br/> **szOID \_ \_ dirección postal**<br/>                                                                 | **Cadena** (máx. 30 caracteres)   | Dirección postal del asunto o el cuadro PO.                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Asunto. apellido"             | "Apellido" "SN"<br/> "2.5.4.4"<br/> **nombre de szOID \_ sur \_**<br/>                                                                                 | **Cadena** (máximo 40 caracteres)   | Apellido del asunto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Asunto. título"               | "Title" "T"<br/> "2.5.4.12"<br/> **título de szOID \_**<br/>                                                                                       | **Cadena** (máximo 64 caracteres)   | Título del individuo que solicitó el certificado (opcional).                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Asunto. UnstructuredAddress" | "UnstructuredAddress" "1.2.840.113549.1.9.8"<br/> **szOID \_ RSA \_ unstructAddr**<br/>                                                                | **Cadena** (máximo 1024 caracteres) | Dirección no estructurada.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Asunto. UnstructuredName"    | "UnstructuredName" "1.2.840.113549.1.9.2"<br/> **szOID \_ RSA \_ unstructName**<br/>                                                                   | **Cadena** (máximo 1024 caracteres) | Nombre no estructurado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

Las siguientes propiedades están relacionadas con el sujeto, aunque no son propiedades de nombre. El módulo de directivas no puede establecer estas propiedades directamente.



| Propiedad                    | Tipo de datos                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Request. DistinguishedName" | **Cadena** (máximo 8192 caracteres) | [*Nombre distintivo relativo*](../secgloss/r-gly.md) de la solicitud, una representación textual del sujeto en la solicitud. Esta representación consta de propiedades de nombre, por ejemplo, "CN = nombre, OU = Miunidadorg, C = US". La aplicación de servicios de certificados establece esta propiedad antes de llamar al módulo de directivas, llamando a [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) con el sujeto del RawRequest. |
| "Request. RawName"           | **Binario** (máximo 4096 bytes) | [*Objeto*](../secgloss/b-gly.md) binario de asunto binario de la [*notación de sintaxis abstracta uno*](../secgloss/a-gly.md) (ASN. 1) extraído de la solicitud. La aplicación de servicios de certificados establece esta propiedad antes de llamar al módulo de directivas; su valor viene determinado por el asunto del RawRequest.                                                                                     |
| Distintivo         | **Cadena** (máximo 8192 caracteres) | Nombre distintivo relativo del certificado, una representación textual del sujeto en el certificado. Esta representación consta de propiedades de nombre, por ejemplo, "CN = nombre, OU = Miunidadorg, C = US". La aplicación de servicios de certificados establece esta propiedad después de llamar al módulo de directivas, llamando a [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) mediante RawName.                                                                                                               |
| "RawName"                   | **Binario** (máximo 4096 bytes) | [*BLOB*](../secgloss/b-gly.md) de asunto binario ASN. 1 usado para construir el certificado. La aplicación de servicios de certificados establece esta propiedad después de llamar al módulo de directivas; su valor viene determinado por los valores de las propiedades de nombre específico (subject. CommonName y así sucesivamente) como indica el SubjectTemplate.                                                                                                                                        |



 

Los componentes de [*nombre distintivo relativo*](../secgloss/r-gly.md) aparecen en la propiedad DistinguishedName y el orden en que aparecen se controlan mediante el valor del registro "SubjectTemplate" contenido en la siguiente clave del registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            CertSvc
               Configuration
                  CaName
```

Cuando servicios de Certificate Server analiza los nombres de [*atributo*](../secgloss/a-gly.md) , omite los espacios, guiones (menos signos) y case. Por ejemplo, "AttributeName1", "atributo Nombre1" y "Attribute-nombre1" son equivalentes. En el caso de los valores de atributo, servicios de Certificate Server omite los espacios en blanco iniciales y finales.

Todas las propiedades anteriores, excepto DistinguishedName, RawName y Subject. Country, admiten la sintaxis de varios valores mediante el uso de un carácter de nueva línea. No se puede deshabilitar o cambiar el separador de nueva línea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de certificado](certificate-properties.md)
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

 

 
