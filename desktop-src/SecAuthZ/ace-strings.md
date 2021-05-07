---
description: Explica las cadenas usadas en una entrada de control de acceso.
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: Cadenas ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed8f9aad8696bd3d3c251170f2ff79ea493ce57
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644187"
---
# <a name="ace-strings"></a>Cadenas ACE

El [lenguaje de definición de descriptores](security-descriptor-definition-language.md) de seguridad (SDDL) usa cadenas ACE en los componentes DACL y SACL de una cadena [*de descriptor de*](/windows/desktop/SecGloss/s-gly) seguridad.

Como se muestra en los ejemplos de formato de [cadena del descriptor](security-descriptor-string-format.md) de seguridad, cada ACE de una cadena de descriptor de seguridad se incluye entre paréntesis. Los campos de la ACE están en el orden siguiente y están separados por punto y coma (;).

> [!Note]  
> Hay un formato diferente para las entradas de [*control de*](/windows/desktop/SecGloss/a-gly) acceso condicional (ACE) que otros tipos ace. Para las ACE condicionales, vea [Lenguaje de definición de descriptores de seguridad para ACE condicionales.](security-descriptor-definition-language-for-conditional-aces-.md)

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a>Campos

<dl> <dt>

<span id="ace_type"></span><span id="ACE_TYPE"></span>**tipo \_ ace**
</dt> <dd>

Cadena que indica el valor del miembro **AceType** de la [**estructura ACE \_ HEADER.**](/windows/desktop/api/Winnt/ns-winnt-ace_header) La cadena de tipo ACE puede ser una de las cadenas siguientes definidas en Sddl.h.



| Cadena de tipo ACE | Constante en Sddl.h                      | Valor AceType                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "A"             | ACCESO DE SDDL \_ \_ PERMITIDO                   | ACCESO \_ AL TIPO ACE \_ \_ PERMITIDO                                                                                                                                         |
| "D"             | ACCESO DE SDDL \_ \_ DENEGADO                    | TIPO \_ ACE DE ACCESO \_ \_ DENEGADO                                                                                                                                          |
| "OA"            | SE PERMITE \_ EL ACCESO A \_ OBJETOS SDDL \_           | TIPO \_ ACE DE OBJETO PERMITIDO DE \_ \_ \_ ACCESO                                                                                                                                 |
| "OD"            | ACCESO DENEGADO A OBJETOS SDDL \_ \_ \_            | TIPO \_ ACE DE OBJETO DE ACCESO \_ \_ \_ DENEGADO                                                                                                                                  |
| "AU"            | SDDL \_ AUDIT                             | TIPO ACE \_ DE \_ AUDITORÍA DEL \_ SISTEMA                                                                                                                                           |
| "AL"            | SDDL \_ ALARM                             | TIPO \_ ACE DE ALARMA DEL \_ \_ SISTEMA                                                                                                                                           |
| "OU"            | SDDL \_ OBJECT \_ AUDIT                     | TIPO ACE \_ DE OBJETO DE AUDITORÍA DEL \_ \_ \_ SISTEMA                                                                                                                                   |
| "OL"            | SDDL \_ OBJECT \_ ALARM                     | TIPO ACE \_ DE OBJETO ALARMA DEL \_ \_ \_ SISTEMA                                                                                                                                   |
| "ML"            | ETIQUETA OBLIGATORIA \_ DE \_ SDDL                  | SYSTEM \_ MANDATORY \_ LABEL ACE TYPE Windows Server \_ \_ **2003:** No disponible.                                                                                        |
| "XA"            | SE PERMITE EL ACCESO \_ DE DEVOLUCIÓN DE \_ LLAMADA DE SDDL \_         | ACCESS \_ ALLOWED \_ CALLBACK ACE TYPE Windows Server \_ \_ **2008, Windows Vista and Windows Server 2003:** No disponible.                                                |
| "XD"            | ACCESO DENEGADO DE \_ DEVOLUCIÓN DE \_ LLAMADA DE SDDL \_          | ACCESS \_ DENIED \_ CALLBACK ACE TYPE Windows Server \_ \_ **2008, Windows Vista and Windows Server 2003:** No disponible.                                                 |
| "RA"            | ATRIBUTO DE \_ RECURSO \_ SDDL               | ATRIBUTO DE RECURSO DEL SISTEMA TIPO ACE \_ \_ Windows Server \_ \_ **2008 R2, Windows 7, Windows Server 2008, Windows Vista y Windows Server 2003:** No disponible.<br/> |
| "SP"            | ID. DE \_ DIRECTIVA CON ÁMBITO DE \_ \_ SDDL                | ID. DE DIRECTIVA DE ÁMBITO DEL SISTEMA TIPO ACE \_ \_ Windows Server \_ \_ \_ **2008 R2, Windows 7, Windows Server 2008, Windows Vista y Windows Server 2003:** No disponible.<br/>  |
| "XU"            | AUDITORÍA DE DEVOLUCIÓN DE LLAMADA DE SDDL \_ \_                   | SYSTEM \_ AUDIT \_ CALLBACK ACE TYPE Windows Server \_ \_ **2008 R2, Windows 7, Windows Server 2008, Windows Vista y Windows Server 2003:** No disponible.<br/>     |
| "ZA"            | ACCESO AL OBJETO DE DEVOLUCIÓN DE LLAMADA DE SDDL \_ \_ \_ \_ PERMITIDO | ACCESS \_ ALLOWED \_ CALLBACK ACE TYPE Windows Server \_ \_ **2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** No disponible.<br/>   |
| "TL"            | ETIQUETA DE \_ CONFIANZA DEL PROCESO \_ \_ SDDL             | SYSTEM \_ PROCESS TRUST LABEL ACE TYPE Windows Server \_ \_ \_ \_ **2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista y Windows Server 2003:** No disponible. |
| "FL"            | FILTRO DE \_ ACCESO \_ SDDL                    | SYSTEM \_ ACCESS FILTER ACE TYPE Windows Server \_ \_ \_ **2016, Windows 10 versión 1607, Windows 10 versión 1511, Windows 10 versión 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista y Windows Server 2003:** no disponible. |
 

> [!Note]  
> Si **ace \_ type** es ACCESS ALLOWED OBJECT ACE TYPE y ni guid de objeto ni GUID de objeto heredado tienen un \_ \_ \_ \_ [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) especificado, [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) **\_ \_** **\_** **\_** \_ \_ \_ convierte el tipo ace en ACCESS ALLOWED ACE TYPE.

 

</dd> <dt>

<span id="ace_flags"></span><span id="ACE_FLAGS"></span>**marcas \_ ace**
</dt> <dd>

Cadena que indica el valor del miembro **AceFlags** de la [**estructura ACE \_ HEADER.**](/windows/desktop/api/Winnt/ns-winnt-ace_header) La cadena de marcas ACE puede ser una concatenación de las cadenas siguientes definidas en Sddl.h.



| Cadena de marcas ACE | Constante en Sddl.h       | Valor aceFlag                 |
|------------------|--------------------------|-------------------------------|
| "CI"             | SDDL \_ CONTAINER \_ INHERIT | ACE \_ DE HERENCIA DE \_ CONTENEDOR       |
| "OI"             | SDDL \_ OBJECT \_ INHERIT    | ACE \_ DE HERENCIA DE \_ OBJETO          |
| "NP"             | SDDL \_ NO \_ PROPAGATE      | NO \_ PROPAGATE \_ INHERIT \_ ACE   |
| "E/S"             | SOLO HERENCIA \_ DE \_ SDDL      | HEREDAR \_ SOLO \_ ACE            |
| "ID"             | SDDL \_ HEREDADO          | ACE \_ HEREDADA                |
| "SA"             | SDDL \_ AUDIT \_ SUCCESS     | MARCA \_ ACE DE ACCESO \_ \_ CORRECTO |
| "FA"             | ERROR DE \_ AUDITORÍA DE \_ SDDL     | MARCA \_ ACE DE ACCESO CON \_ \_ ERROR     |
| "TP"             | FILTRO PROTEGIDO \_ DE CONFIANZA \_ DE \_ SDDL | TRUST \_ PROTECTED FILTER ACE FLAG Windows Server \_ \_ \_ **2016, Windows 10 versión 1607, Windows 10 versión 1511, Windows 10 versión 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista y Windows Server 2003:** no disponible. |
| "CR"             | SDDL \_ CRITICAL           | CRITICAL \_ ACE FLAG Windows Server version \_ **1803, Windows 10 Version 1803, Windows Server Version 1709, Windows 10 Version 1709, Windows 10 Version 1703, Windows Server 2016, Windows 10 versión 1607, Windows 10 versión 1511, Windows 10 versión 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista y Windows Server 2003:** No disponible. |
 

</dd> <dt>

<span id="rights"></span><span id="RIGHTS"></span>**Derechos**
</dt> <dd>

Cadena que indica los derechos [de acceso controlados](access-rights-and-access-masks.md) por la ACE. Esta cadena puede ser una representación de cadena hexadecimal de los derechos de acceso, como "0x7800003F", o puede ser una concatenación de las cadenas siguientes.



### <a name="generic-access-rights"></a>Derechos de acceso genéricos

| Cadena de derechos de acceso | Constante en Sddl.h | Valor derecho de acceso |
|----------------------|--------------------|--------------------|
| "GA"                 | SDDL \_ GENERIC \_ ALL | GENERIC \_ ALL       |
| "GR"                 | LECTURA GENÉRICA DE SDDL \_ \_ | LECTURA \_ GENÉRICA     |
| "GW"                 | ESCRITURA \_ GENÉRICA DE \_ SDDL | ESCRITURA \_ GENÉRICA |
| "GX"                 | EJECUCIÓN GENÉRICA DE SDDL \_ \_ | GENERIC \_ EXECUTE |


### <a name="standard-access-rights"></a>Derechos de acceso estándar

| Cadena de derechos de acceso | Constante en Sddl.h | Valor derecho de acceso |
|----------------------|--------------------|--------------------|
| "RC"                 | CONTROL DE LECTURA \_ DE \_ SDDL | CONTROL DE \_ LECTURA      |
| "SD"                 | SDDL \_ STANDARD \_ DELETE | DELETE          |
| "WD"                 | SDDL \_ WRITE \_ DAC | ESCRIBIR \_ DAC            |
| "WO"                 | PROPIETARIO DE ESCRITURA DE SDDL \_ \_ | PROPIETARIO \_ DE ESCRITURA        |

### <a name="directory-service-object-access-rights"></a>Derechos de acceso a objetos del servicio de directorio

| Cadena de derechos de acceso | Constante en Sddl.h | Valor derecho de acceso |
|----------------------|--------------------|--------------------|
| "RP"                 | PROPIEDAD \_ READ de \_ SDDL | ADS \_ RIGHT \_ DS \_ READ \_ PROP |
| "WP"                 | PROPIEDAD \_ DE ESCRITURA DE \_ SDDL | ADS \_ RIGHT \_ DS \_ WRITE \_ PROP |
| "CC"                 | SDDL \_ CREATE \_ CHILD | ADS \_ RIGHT \_ DS \_ CREATE \_ CHILD |
| "DC"                 | SDDL \_ DELETE \_ CHILD | ADS \_ RIGHT \_ DS \_ DELETE \_ CHILD |
| "LC"                 | SDDL \_ LIST \_ CHILDREN | ADS \_ RIGHT \_ ACTRL \_ DS \_ LIST |
| "SW"                 | AUTOES \_ ESCRITURA DE \_ SDDL    | ADS \_ RIGHT \_ DS \_ SELF |
| "LO"                  | OBJETO DE \_ LISTA DE \_ SDDL | OBJETO \_ DE LISTA DE \_ DS DE LA DERECHA DE \_ \_ ADS |
| "DT"                 | ÁRBOL DE \_ ELIMINACIÓN DE \_ SDDL | ÁRBOL \_ DE \_ ELIMINACIÓN DE DS DE LA DERECHA \_ DE \_ ADS |
| "CR"                  | ACCESO DE CONTROL DE SDDL \_ \_ | ADS \_ RIGHT \_ DS \_ CONTROL \_ ACCESS |

### <a name="file-access-rights"></a>Derechos de acceso a archivos

| Cadena de derechos de acceso | Constante en Sddl.h | Valor derecho de acceso |
|----------------------|--------------------|--------------------|
| "FA"                 | ARCHIVO SDDL \_ \_ ALL    | ACCESO A \_ TODOS LOS \_ ARCHIVOS   |
| "FR"                 | LECTURA DE ARCHIVOS SDDL \_ \_   | LECTURA \_ GENÉRICA DE \_ ARCHIVO |
| "FW"                 | ESCRITURA DE \_ ARCHIVOS \_ SDDL  | ESCRITURA \_ GENÉRICA DE \_ ARCHIVOS |
| "FX"                 | SDDL \_ FILE \_ EXECUTE | FILE \_ GENERIC \_ EXECUTE |


### <a name="registry-key-access-rights"></a>Derechos de acceso a la clave del Registro

| Cadena de derechos de acceso | Constante en Sddl.h | Valor derecho de acceso |
|----------------------|--------------------|--------------------|
| "KA"                 | SDDL \_ KEY \_ ALL     | ACCESO \_ A KEY \_ ALL   |
| "KR"                 | SDDL \_ KEY \_ READ    | KEY \_ READ          |
| "KW"                 | SDDL \_ KEY \_ WRITE   | KEY \_ WRITE         |
| "KX"                 | SDDL \_ KEY \_ EXECUTE | KEY \_ EXECUTE       |

### <a name="mandatory-label-rights"></a>Derechos de etiqueta obligatorios

| Cadena de derechos de acceso | Constante en Sddl.h | Valor derecho de acceso |
|----------------------|--------------------|--------------------|
| "NR"                 | SDDL \_ NO \_ READ \_ UP | ETIQUETA \_ OBLIGATORIA DEL SISTEMA NO READ UP Windows Server \_ \_ \_ \_ **2008, Windows Vista y Windows Server 2003:** No disponible. |
| "NW"                 | SDDL \_ NO \_ WRITE \_ UP | SYSTEM \_ MANDATORY \_ LABEL NO WRITE UP Windows Server \_ \_ \_ **2008, Windows Vista and Windows Server 2003:** No disponible. |
| "NX"                 | SDDL \_ NO \_ EXECUTE \_ UP | ETIQUETA \_ OBLIGATORIA DEL SISTEMA NO EXECUTE UP Windows Server \_ \_ \_ \_ **2008, Windows Vista y Windows Server 2003:** No disponible. |
</dd> <dt>

<span id="object_guid"></span><span id="OBJECT_GUID"></span>**GUID de \_ objeto**
</dt> <dd>

Representación de cadena de un GUID que indica el valor del **miembro ObjectType** de una estructura ACE específica del objeto, como [**ACCESS ALLOWED OBJECT \_ \_ \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace). La cadena GUID usa el formato devuelto por la [**función UuidToString.**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring)

En la tabla siguiente se enumeran algunos GUID de objeto usados habitualmente.



| Derechos y GUID                         | Permiso      |
|-----------------------------------------|-----------------|
| CR;ab721a53-1e2f-11d0-9819-00aa0040529b | Cambiar contraseña |
| CR;00299570-246d-11d0-a768-00aa006e0529 | Restablecimiento de contraseña  |



 

</dd> <dt>

<span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**guid \_ de \_ objeto inherit**
</dt> <dd>

Representación de cadena de un GUID que indica el valor del **miembro InheritedObjectType** de una estructura ACE específica del objeto. La cadena GUID usa el [**formato UuidToString.**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring)

</dd> <dt>

<span id="account_sid"></span><span id="ACCOUNT_SID"></span>**sid \_ de cuenta**
</dt> <dd>

[Cadena de SID](sid-strings.md) que identifica al [administrador de confianza](trustees.md) de la ACE.

</dd> <dt>

<span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**atributo \_ resource**
</dt> <dd>

\[OPCIONAL \] El atributo de recurso es solo para las ACE de recursos y es \_ opcional. Cadena que indica el tipo de datos. El tipo de datos ace del atributo de recurso puede ser uno de los siguientes tipos de datos definidos en Sddl.h.

El signo \# " es sinónimo de "0" en los atributos de recursos. Por ejemplo, D:AI(XA;OICI;FA;;; WD;(OctetStringType== 1 2 3 )) es equivalente e interpretado como \# \# \# \# \# D:AI(XA;OICI;FA;;; WD;(OctetStringType== \# 01020300)).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista y Windows Server 2003:** Los atributos de recursos no están disponibles.



| Cadena de tipo de datos ace de atributo de recurso | Constante en Sddl.h | Tipo de datos        |
|-----------------------------------------|--------------------|------------------|
| "TI"                                    | SDDL \_ INT          | Entero con signo   |
| "TU"                                    | SDDL \_ UINT         | Entero sin signo |
| "TS"                                    | SDDL \_ WSTRING      | Cadena ancha      |
| "TD"                                    | SID \_ de SDDL          | SID              |
| "TX"                                    | BLOB \_ DE SDDL         | Cadena de octeto     |
| "TB"                                    | VALOR BOOLEANO de SDDL \_      | Boolean          |



 

</dd> </dl>

En el ejemplo siguiente se muestra una cadena ACE para una ACE con acceso permitido. No es una ACE específica del objeto, por lo que no tiene información en el **\_ GUID** del objeto y **hereda los \_ campos guid \_ del** objeto. El **campo \_ de marcas** ace también está vacío, lo que indica que no se ha establecido ninguna de las marcas ACE.


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



La cadena ACE mostrada anteriormente describe la siguiente información de ACE.


```C++
AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
AceFlags:      0x00
Access Mask:   0x100e003f
                    READ_CONTROL
                    WRITE_DAC
                    WRITE_OWNER
                    GENERIC_ALL
                    Other access rights(0x0000003f)
Ace Sid      : (S-1-1-0)
```



En el ejemplo siguiente se muestra un archivo clasificado con notificaciones de recursos para Windows y Lenguaje de consulta estructurado (SQL) con secreto establecido en Alto impacto empresarial.


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



La cadena ACE mostrada anteriormente describe la siguiente información de ACE.


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



Para obtener más información, vea [Formato de cadena de descriptor de seguridad](security-descriptor-string-format.md) y [Cadenas SID](sid-strings.md). Para las ACE condicionales, vea [Lenguaje de definición de descriptores de seguridad para ACE condicionales.](security-descriptor-definition-language-for-conditional-aces-.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\[MS-DTYP: \] lenguaje de descripción del descriptor de seguridad](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

