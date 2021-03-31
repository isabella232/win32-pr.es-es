---
description: Explica las cadenas usadas en una entrada de control de acceso.
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: Cadenas ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a35bde18a1ca3ac416faa42e3b693e26305beb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813291"
---
# <a name="ace-strings"></a>Cadenas ACE

El [lenguaje de definición de descriptores de seguridad](security-descriptor-definition-language.md) (SDDL) utiliza cadenas ACE en los componentes DACL y SACL de una cadena de [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) .

Como se muestra en los ejemplos de [formato de cadena de descriptor de seguridad](security-descriptor-string-format.md) , cada ACE de una cadena de descriptor de seguridad se incluye entre paréntesis. Los campos de la ACE están en el siguiente orden y se separan mediante signos de punto y coma (;).

> [!Note]  
> Hay un formato diferente para [*las entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) condicionales que otros tipos ACE. Para las ACE condicionales, consulte [lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md).

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a>Campos

<dl> <dt>

<span id="ace_type"></span><span id="ACE_TYPE"></span>**tipo de ACE \_**
</dt> <dd>

Cadena que indica el valor del miembro **AceType** de la estructura del [**\_ encabezado ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . La cadena de tipo ACE puede ser una de las siguientes cadenas definidas en SDDL. h.



| Cadena de tipo ACE | Constante en SDDL. h                      | Valor AceType                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "A"             | acceso de SDDL \_ \_ permitido                   | \_tipo de \_ ACE \_ permitido de acceso                                                                                                                                         |
| "D"             | acceso de SDDL \_ \_ denegado                    | tipo de ACE de acceso \_ denegado \_ \_                                                                                                                                          |
| OA            | \_ \_ acceso a objeto SDDL \_ permitido           | \_tipo de \_ ACE de objeto permitido \_ de acceso \_                                                                                                                                 |
| DP            | \_ \_ acceso \_ denegado a objetos SDDL            | tipo de ACE de objeto de acceso \_ denegado \_ \_ \_                                                                                                                                  |
| ESTÉ            | auditoría de SDDL \_                             | \_tipo de \_ ACE de auditoría del sistema \_                                                                                                                                           |
| "AL"            | \_alarma SDDL                             | \_tipo de \_ ACE de alarma del sistema \_                                                                                                                                           |
| ORGANIZA            | \_Auditoría de objeto SDDL \_                     | \_tipo de \_ ACE del objeto de auditoría del sistema \_ \_                                                                                                                                   |
| OL            | \_alarma de objeto SDDL \_                     | \_tipo de \_ ACE del objeto Alarm \_ del sistema \_                                                                                                                                   |
| APROXIMADAMENTE            | \_etiqueta obligatoria de SDDL \_                  | \_tipo de \_ ACE de etiqueta obligatoria \_ del sistema \_                                                                                                                                |
| XA            | acceso de devolución de llamada de SDDL \_ \_ \_ permitido         | \_ \_ \_ \_ Tipo de ACE de devolución **de llamada permitido de acceso windows vista y Windows Server 2003:** no disponible.<br/>                                                           |
| XD            | \_ \_ acceso denegado de devolución de llamada SDDL \_          | \_ \_ \_ Tipo de ACE de devolución de llamada de acceso denegado \_ **, windows vista y Windows Server 2003:** no disponible.<br/>                                                            |
| REMOTA            | \_atributo de recurso SDDL \_               | \_Tipo de \_ ACE de atributo de recurso del sistema \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista y Windows Server 2003:** no disponible.<br/> |
| DAÑADO            | identificador de directiva de ámbito de SDDL \_ \_ \_                | \_ID. de directiva de ámbito del sistema \_ tipo de \_ \_ ACE \_ **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista y Windows Server 2003:** no disponible.<br/>  |
| "XU"            | auditoría de devolución de llamada de SDDL \_ \_                   | \_Tipo de ACE de devolución de llamada de auditoría del sistema de \_ \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista y Windows Server 2003:** no disponible.<br/>     |
| ZA            | \_acceso a objetos de devolución de llamada de SDDL \_ \_ \_ permitido | \_Tipo de \_ ACE de devolución de llamada permitido de acceso a \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista y Windows Server 2003:** no disponible.<br/>   |



 

> [!Note]  
> Si **el \_ tipo ACE** es \_ el tipo de ACE de objeto permitido de acceso y ninguno de los GUID del objeto o el GUID del objeto \_ \_ \_ **heredado \_ \_** tiene un [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) especificado, [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) convierte el **\_ tipo de ACE** en el tipo de **\_** \_ ACE permitido de acceso \_ \_ .

 

</dd> <dt>

<span id="ace_flags"></span><span id="ACE_FLAGS"></span>**\_marcas ACE**
</dt> <dd>

Cadena que indica el valor del miembro **AceFlags** de la estructura del [**\_ encabezado ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . La cadena de marcas ACE puede ser una concatenación de las siguientes cadenas definidas en SDDL. h.



| Cadena de marcas ACE | Constante en SDDL. h       | Valor AceFlag                 |
|------------------|--------------------------|-------------------------------|
| IA             | \_herencia de contenedor de SDDL \_ | \_ACE de herencia de contenedor \_       |
| OI             | \_herencia de objeto SDDL \_    | \_ACE de herencia de objeto \_          |
| PAGINA             | SDDL \_ no \_ Propagate      | NO \_ propagar \_ ACE de herencia \_   |
| IO             | \_solo herencia de SDDL \_      | solo HEREDAr \_ \_ ACE            |
| "ID"             | SDDL \_ heredado          | ACE HEREDAda \_                |
| VALIDA             | auditoría de SDDL \_ \_ correcta     | \_ \_ marca ACE de acceso correcta \_ |
| REG             | \_error de auditoría de SDDL \_     | \_ \_ marca ACE de acceso con error \_     |



 

</dd> <dt>

<span id="rights"></span><span id="RIGHTS"></span>**necesarios**
</dt> <dd>

Cadena que indica los [derechos de acceso](access-rights-and-access-masks.md) controlados por la ACE. Esta cadena puede ser una representación de cadena hexadecimal de los derechos de acceso, como "0x7800003F", o puede ser una concatenación de las siguientes cadenas.



### <a name="generic-access-rights"></a>Derechos de acceso genéricos

| Cadena de derechos de acceso | Constante en SDDL. h | Valor derecho de acceso |
|----------------------|--------------------|--------------------|
| General                 | SDDL \_ genéricos \_ | todos GENÉRICOs \_       |
| GR                 | \_lectura genérica de SDDL \_ | \_lectura genérica     |
| GW                 | \_escritura genérica \_ SDDL | \_escritura genérica |
| GX                 | \_ejecución genérica de SDDL \_ | \_ejecución genérica |


### <a name="standard-access-rights"></a>Derechos de acceso estándar

| Cadena de derechos de acceso | Constante en SDDL. h | Valor derecho de acceso |
|----------------------|--------------------|--------------------|
| CR                 | \_control de lectura de SDDL \_ | CONTROL de lectura \_      |
| DT                 | SDDL \_ estándar de \_ eliminación | Delete          |
| WD                 | \_DAC de escritura de SDDL \_ | ESCRIBIR \_ DAC            |
| SEM                 | \_propietario de escritura de SDDL \_ | propietario de escritura \_        |

### <a name="directory-service-object-access-rights"></a>Derechos de acceso a objetos de servicio de directorio

| Cadena de derechos de acceso | Constante en SDDL. h | Valor derecho de acceso |
|----------------------|--------------------|--------------------|
| RP                 | \_propiedad de lectura de SDDL \_ | \_right \_ DS \_ leer \_ prop. |
| WP                 | \_propiedad de escritura de SDDL \_ | \_prop de \_ \_ escritura DS right de \_ ADS |
| CORREOS                 | \_crear \_ elemento secundario de SDDL | AD \_ derecho \_ DS \_ crear \_ secundario |
| CD                 | SDDL \_ eliminar \_ secundario | ADS \_ derecho \_ DS \_ eliminar \_ secundario |
| Live                 | \_ \_ elementos secundarios de la lista SDDL | AD \_ derecho \_ ACTRL \_ lista de DS \_ |
| SW                 | \_escritura automática de SDDL \_    | AD \_ right \_ DS \_ Self |
| LO                  | \_objeto de lista SDDL \_ | \_objeto de \_ lista de DS derecho \_ ADS \_ |
| DT                 | \_árbol de eliminación de SDDL \_ | \_árbol de \_ eliminación de DS derecho \_ de ADS \_ |
| COMPRA                  | \_acceso de control de SDDL \_ | \_acceso de \_ \_ control DS derecho de \_ ADS |

### <a name="file-access-rights"></a>Derechos de acceso a archivos

| Cadena de derechos de acceso | Constante en SDDL. h | Valor derecho de acceso |
|----------------------|--------------------|--------------------|
| REG                 | \_ \_ todos los archivos SDDL    | \_acceso a todos los archivos \_   |
| DIRECCIONA                 | \_lectura de archivo SDDL \_   | lectura de archivo \_ genérico \_ |
| RV                 | \_escritura de archivos SDDL \_  | escritura de archivo \_ genérico \_ |
| EFECTOS                 | \_ejecución de archivo SDDL \_ | ARCHIVO \_ genérico \_ Execute |


### <a name="registry-key-access-rights"></a>Derechos de acceso de la clave del registro

| Cadena de derechos de acceso | Constante en SDDL. h | Valor derecho de acceso |
|----------------------|--------------------|--------------------|
| Ka                 | \_ \_ todas las claves SDDL     | acceso de clave \_ \_ a todo   |
| Corea                 | \_lectura de clave SDDL \_    | lectura de clave \_          |
| KW                 | \_escritura de claves SDDL \_   | escritura de claves \_         |
| KX                 | \_ejecución de clave SDDL \_ | ejecución de clave \_       |

### <a name="mandatory-label-rights"></a>Derechos de etiqueta obligatorios

| Cadena de derechos de acceso | Constante en SDDL. h | Valor derecho de acceso |
|----------------------|--------------------|--------------------|
| Nr                 | SDDL \_ no \_ lectura \_ | NO se ha leído la \_ etiqueta obligatoria del sistema \_ \_ \_ \_ |
| NOROESTE                 | \_no \_ escribir SDDL \_ | \_no se \_ ha \_ \_ configurado ninguna \_ etiqueta obligatoria del sistema |
| NX                 | SDDL \_ no \_ ejecutar \_ | NO se ha ejecutado la \_ etiqueta obligatoria del sistema \_ \_ \_ \_ |
</dd> <dt>

<span id="object_guid"></span><span id="OBJECT_GUID"></span>**GUID del objeto \_**
</dt> <dd>

Representación de cadena de un GUID que indica el valor del miembro **objecttype** de una estructura ACE específica del objeto, como [**acceso a la \_ \_ \_ ACE del objeto permitido**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace). La cadena GUID usa el formato devuelto por la función [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .

En la tabla siguiente se enumeran algunos GUID de objetos de uso frecuente.



| Derechos y GUID                         | Permiso      |
|-----------------------------------------|-----------------|
| CR; ab721a53-1e2f-11d0-9819-00aa0040529b | Cambiar contraseña |
| CR; 00299570-246d-11d0-A768-00aa006e0529 | Restablecimiento de contraseña  |



 

</dd> <dt>

<span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**heredar \_ GUID del objeto \_**
</dt> <dd>

Representación de cadena de un GUID que indica el valor del miembro **InheritedObjectType** de una estructura ACE específica del objeto. La cadena GUID usa el formato [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .

</dd> <dt>

<span id="account_sid"></span><span id="ACCOUNT_SID"></span>**SID de cuenta \_**
</dt> <dd>

[Cadena SID](sid-strings.md) que identifica el [Administrador de confianza](trustees.md) de la ACE.

</dd> <dt>

<span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**atributo de recurso \_**
</dt> <dd>

\[OPCIONAL \] el \_ atributo de recurso es solo para las ACE de recursos y es opcional. Cadena que indica el tipo de datos. El tipo de datos ACE del atributo de recurso puede ser uno de los siguientes tipos de datos definidos en SDDL. h.

El \# signo "" es sinónimo de "0" en los atributos de recursos. Por ejemplo, D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) es equivalente a e interpretado como D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 01020300)).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista y Windows server 2003:** Los atributos de recursos no están disponibles.



| Cadena de tipo de datos ACE de atributo de recurso | Constante en SDDL. h | Tipo de datos        |
|-----------------------------------------|--------------------|------------------|
| TI                                    | SDDL \_ int          | Entero con signo   |
| TU                                    | SDDL ( \_ uint)         | Entero sin signo |
| TS                                    | \_WSTRING SDDL      | Cadena ancha      |
| TD                                    | SID de SDDL \_          | SID              |
| TX                                    | BLOB de SDDL \_         | Cadena de octeto     |
| TB                                    | SDDL \_ booleano      | Boolean          |



 

</dd> </dl>

En el ejemplo siguiente se muestra una cadena ACE para una ACE con acceso permitido. No es una ACE específica del objeto, por lo que no tiene información en los **campos \_ GUID** del objeto y **heredar \_ \_ GUID del objeto** . El **campo \_ marcas ACE** también está vacío, lo que indica que no se ha establecido ninguna de las marcas ACE.


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



En el ejemplo siguiente se muestra un archivo clasificado con notificaciones de recursos para Windows y Lenguaje de consulta estructurado (SQL) con la confidencialidad establecida en alto impacto empresarial.


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



Para obtener más información, vea [formato de cadena de descriptor de seguridad](security-descriptor-string-format.md) y cadenas de [SID](sid-strings.md). Para las ACE condicionales, consulte [lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\[MS-DTYP \] : lenguaje de descripción de descriptores de seguridad](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

