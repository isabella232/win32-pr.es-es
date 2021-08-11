---
title: Enumeraciones ADSI
description: Active Directory interfaces de servicio (ADSI) definen y usan las enumeraciones que se muestran en la tabla siguiente.
ms.assetid: f0ad5ce5-742d-40dc-ac5a-31d779e40bfd
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, referencia, enumeraciones
- Enumeraciones ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459aa59bc0f7907f59a4cd5a7e5fcb4f1b2630d8
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/27/2020
ms.locfileid: "104077399"
---
# <a name="adsi-enumerations"></a>Enumeraciones ADSI

Active Directory interfaces de servicio (ADSI) definen y usan las enumeraciones que se muestran en la tabla siguiente.



| Enumeración                                                           | Descripción                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ enumeración ACEFLAG ADS**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum)                        | Especifica cómo se propaga la seguridad para las entradas de control de acceso (ACE) heredadas y los tipos de auditoría de una ACE del sistema.                                                                                                                                             |
| [**\_ \_ enumeración ACETYPE ADS**](/windows/win32/api/iads/ne-iads-ads_acetype_enum)                        | Especifica el tipo de ACE.                                                                                                                                                                                                                                           |
| [**\_enumeración de autenticación ADS \_**](/windows/win32/api/iads/ne-iads-ads_authentication_enum)          | Especifica el nivel de seguridad usado en la autenticación de un cliente.                                                                                                                                                                                                     |
| [**\_ \_ enumeración de referencias de seguimiento de ADS \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)       | Especifica el comportamiento del seguimiento de referencias.                                                                                                                                                                                                                       |
| [**\_DEREFENUM ADS**](/windows/win32/api/iads/ne-iads-ads_derefenum)                               | Especifica el comportamiento de desreferenciación de alias.                                                                                                                                                                                                                    |
| [**\_enumeración para mostrar de ADS \_**](/windows/win32/api/iads/ne-iads-ads_display_enum)                        | Especifica cómo se muestra una ruta de acceso.                                                                                                                                                                                                                                |
| [**\_ \_ enumeración de modo de escape de ADS \_**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)               | Especifica si los caracteres especiales son caracteres de escape, sin escape o no tocados.                                                                                                                                                                                        |
| [**\_ \_ enumeración FLAGTYPE ADS**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum)                      | Especifica la presencia de los campos **objecttype** o **INHERITEDOBJECTTYPE** en una ACE.                                                                                                                                                                         |
| [**\_enumeración de formato ADS \_**](/windows/win32/api/iads/ne-iads-ads_format_enum)                          | Especifica el tipo de valores de un objeto pathname.                                                                                                                                                                                                                |
| [**\_ \_ enumeración de tipo de grupo ADS \_**](/windows/win32/api/iads/ne-iads-ads_group_type_enum)                 | Especifica el tipo de grupo del miembro.                                                                                                                                                                                                                           |
| [**ADS \_ name \_ INITTYPE \_ enum**](/windows/win32/api/iads/ne-iads-ads_name_inittype_enum)           | Especifica el tipo de inicialización que se va a realizar en un objeto de traducción de nombre.                                                                                                                                                                                  |
| [**\_ \_ enumeración de tipo de nombre de ADS \_**](/windows/win32/api/iads/ne-iads-ads_name_type_enum)                   | Especifica el formato utilizado para representar nombres distintivos.                                                                                                                                                                                                       |
| [**\_enumeración de opciones de ADS \_**](/windows/win32/api/iads/ne-iads-ads_option_enum)                          | Especifica las opciones disponibles que la interfaz [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) utiliza para manipular los objetos de directorio.                                                                                                                        |
| [**\_ \_ enumeración de codificación de contraseña ADS \_**](/windows/win32/api/iads/ne-iads-ads_password_encoding_enum)   | Se usa para identificar el tipo de codificación de contraseña utilizada con la opción de método de contraseña de opción de ADS en los métodos [**IADsObjectOptions:: GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) y [**IADsObjectOptions:: SetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) . **\_ \_ \_** |
| [**\_ \_ enumeración PATHTYPE ADS**](/windows/win32/api/iads/ne-iads-ads_pathtype_enum)                      | Especifica el tipo de objeto en el que se modifica el descriptor de seguridad.                                                                                                                                                                                        |
| [**enumeración de las preferencias de ADS \_ \_**](/windows/win32/api/iads/ne-iads-ads_preferences_enum)                | Especifica las preferencias de consulta del OLE DB para ADSI.                                                                                                                                                                                                           |
| [**\_ \_ enumeración de operación de propiedad ADS \_**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) | Especifica las formas de actualizar los valores de propiedad en la caché de propiedades.                                                                                                                                                                                               |
| [**\_enumeración de derechos de ADS \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum)                          | Especifica los derechos de acceso a un objeto de servicio de directorio.                                                                                                                                                                                                        |
| [**\_SCOPEENUM ADS**](/windows/win32/api/iads/ne-iads-ads_scopeenum)                               | Especifica el ámbito de una búsqueda de directorio.                                                                                                                                                                                                                        |
| [**\_ \_ enumeración de control SD de ADS \_**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum)                 | Especifica que una lista de control de acceso (ACL) se protegerá cuando se apliquen nuevos permisos de forma recursiva a un árbol de directorios.                                                                                                                                  |
| [**\_ \_ enumeración de formato SD de ADS \_**](/windows/win32/api/iads/ne-iads-ads_sd_format_enum)                   | Especifica el formato para convertir el descriptor de seguridad.                                                                                                                                                                                                      |
| [**\_ \_ enumeración de revisión de ad SD \_**](/windows/win32/api/iads/ne-iads-ads_sd_revision_enum)               | Especifica el número de revisión de una ACE o ACL.                                                                                                                                                                                                                   |
| [**\_ \_ enumeración SEARCHPREF ADS**](/windows/win32/api/iads/ne-iads-ads_searchpref_enum)                  | Especifica las preferencias de la búsqueda.                                                                                                                                                                                                                              |
| [**\_ \_ enumeración de información de seguridad ADS \_**](/windows/win32/api/iads/ne-iads-ads_security_info_enum)           | Especifica las opciones para examinar los datos de seguridad.                                                                                                                                                                                                                |
| [**\_ \_ enumeración SETTYPE ADS**](/windows/win32/api/iads/ne-iads-ads_settype_enum)                        | Especifica el formato de la ruta de acceso en [**IADsPathname:: set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set).                                                                                                                                                                                       |
| [**\_STATUSENUM ADS**](/windows/win32/api/iads/ne-iads-ads_statusenum)                             | Especifica el estado de las preferencias de búsqueda.                                                                                                                                                                                                                       |
| [**\_ \_ enumeración SYSTEMFLAG ADS**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)                  | Especifica los tipos de atributos que representa un objeto **attributeSchema** .                                                                                                                                                                                   |
| [**\_ \_ enumeración de marca de usuario ADS \_**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)                   | Especifica las marcas que se usan para manipular las propiedades de usuario.                                                                                                                                                                                                            |
| [**\_enumeración de dialecto ADSI \_**](/windows/win32/api/iads/ne-iads-adsi_dialect_enum)                      | Especifica los dialectos de consulta ADSI disponibles.                                                                                                                                                                                                                          |
| [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)                                    | Especifica los tipos de datos utilizados para interpretar una cadena de sintaxis extendida de ADSI.                                                                                                                                                                                            |



 

## <a name="remarks"></a>Observaciones

Dado que Visual Basic Scripting Edition aplicaciones no pueden leer datos de una biblioteca de tipos, las aplicaciones de VBScript no pueden reconocer constantes simbólicas tal y como se definen en estas enumeraciones. En su lugar, use las constantes numéricas para establecer las marcas adecuadas en las aplicaciones de VBScript. Para usar las constantes simbólicas como una buena práctica de programación, escriba declaraciones explícitas de tales constantes, como se hace aquí, en aplicaciones de VBScript.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
</dt> <dt>

[**IADsPathname:: set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)
</dt> </dl>

 

 




