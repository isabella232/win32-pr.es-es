---
title: Enumeraciones ADSI
description: Active Directory interfaces de servicio (ADSI) definen y usan las enumeraciones enumeradas en la tabla siguiente.
ms.assetid: f0ad5ce5-742d-40dc-ac5a-31d779e40bfd
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Referencia, Enumeraciones
- ENUMERACIONES ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10d5aed5688e7128a64a32dee2f83efa22ab5bf292231517026299ccb592886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023913"
---
# <a name="adsi-enumerations"></a>Enumeraciones ADSI

Active Directory interfaces de servicio (ADSI) definen y usan las enumeraciones enumeradas en la tabla siguiente.



| Enumeración                                                           | Descripción                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ADS \_ ACEFLAG \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum)                        | Especifica cómo se propaga la seguridad para las entradas de control de acceso (ACE) heredadas y los tipos de auditoría para una ACE del sistema.                                                                                                                                             |
| [**ADS \_ ACETYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_acetype_enum)                        | Especifica el tipo ACE.                                                                                                                                                                                                                                           |
| [**ENUMERACIÓN \_ DE \_ AUTENTICACIÓN DE ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum)          | Especifica el nivel de seguridad utilizado para autenticar un cliente.                                                                                                                                                                                                     |
| [**ENUMERACIÓN \_ ADS \_ REFERRALS \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)       | Especifica el comportamiento de la búsqueda de referencias.                                                                                                                                                                                                                       |
| [**ADS \_ DEREFENUM**](/windows/win32/api/iads/ne-iads-ads_derefenum)                               | Especifica el comportamiento de la desreferenciación de alias.                                                                                                                                                                                                                    |
| [**ENUMERACIÓN \_ DE \_ VISUALIZACIÓN DE ANUNCIOS**](/windows/win32/api/iads/ne-iads-ads_display_enum)                        | Especifica cómo se muestra una ruta de acceso.                                                                                                                                                                                                                                |
| [**ENUMERACIÓN \_ DEL MODO DE ESCAPE DE \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)               | Especifica si los caracteres especiales tienen caracteres de escape, sin escape o sin tocar.                                                                                                                                                                                        |
| [**ADS \_ FLAGTYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum)                      | Especifica la presencia de los campos **ObjectType** o **InheritedObjectType** en una ACE.                                                                                                                                                                         |
| [**ENUMERACIÓN \_ DE FORMATO \_ DE ANUNCIOS**](/windows/win32/api/iads/ne-iads-ads_format_enum)                          | Especifica el tipo de valores de un objeto pathname.                                                                                                                                                                                                                |
| [**ADS \_ GROUP \_ TYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum)                 | Especifica el tipo de grupo del miembro.                                                                                                                                                                                                                           |
| [**ADS \_ NAME \_ INITTYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_name_inittype_enum)           | Especifica el tipo de inicialización que se va a realizar en un objeto de traducción de nombre.                                                                                                                                                                                  |
| [**ADS \_ NAME \_ TYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_name_type_enum)                   | Especifica el formato utilizado para representar nombres distintivos.                                                                                                                                                                                                       |
| [**ENUMERACIÓN \_ DE OPCIÓN \_ DE ANUNCIOS**](/windows/win32/api/iads/ne-iads-ads_option_enum)                          | Especifica las opciones disponibles que usa la [**interfaz IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) para manipular objetos de directorio.                                                                                                                        |
| [**ENUMERACIÓN \_ DE \_ CODIFICACIÓN \_ DE CONTRASEÑAS DE ADS**](/windows/win32/api/iads/ne-iads-ads_password_encoding_enum)   | Se usa para identificar el tipo de codificación de contraseña usado con la opción **\_ ADS OPTION PASSWORD \_ \_ METHOD** en los [**métodos IADsObjectOptions::GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) e [**IADsObjectOptions::SetOption.**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) |
| [**ADS \_ PATHTYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_pathtype_enum)                      | Especifica el tipo de objeto en el que se modifica el descriptor de seguridad.                                                                                                                                                                                        |
| [**ENUMERACIÓN \_ DE \_ PREFERENCIAS DE ANUNCIOS**](/windows/win32/api/iads/ne-iads-ads_preferences_enum)                | Especifica las preferencias de consulta del OLE DB para ADSI.                                                                                                                                                                                                           |
| [**ENUMERACIÓN \_ DE OPERACIÓN DE PROPIEDAD DE \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) | Especifica las formas de actualizar los valores de propiedad en la caché de propiedades.                                                                                                                                                                                               |
| [**ADS \_ RIGHTS \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum)                          | Especifica los derechos de acceso a un objeto de servicio de directorio.                                                                                                                                                                                                        |
| [**ADS \_ SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum)                               | Especifica el ámbito de una búsqueda de directorios.                                                                                                                                                                                                                        |
| [**ADS \_ SD \_ CONTROL \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum)                 | Especifica que se debe proteger una lista de control de acceso (ACL) cuando se apliquen nuevos permisos de forma recursiva a un árbol de directorios.                                                                                                                                  |
| [**ADS \_ SD \_ FORMAT \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_format_enum)                   | Especifica el formato para convertir el descriptor de seguridad.                                                                                                                                                                                                      |
| [**ADS \_ SD \_ REVISION \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_revision_enum)               | Especifica el número de revisión de una ACE o ACL.                                                                                                                                                                                                                   |
| [**ADS \_ SEARCHPREF \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_searchpref_enum)                  | Especifica las preferencias de la búsqueda.                                                                                                                                                                                                                              |
| [**ENUMERACIÓN \_ DE INFORMACIÓN DE SEGURIDAD DE \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_security_info_enum)           | Especifica las opciones para examinar los datos de seguridad.                                                                                                                                                                                                                |
| [**ADS \_ SETTYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_settype_enum)                        | Especifica el formato de ruta de acceso [**en IADsPathname::Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set).                                                                                                                                                                                       |
| [**ADS \_ STATUSENUM**](/windows/win32/api/iads/ne-iads-ads_statusenum)                             | Especifica el estado de las preferencias de búsqueda.                                                                                                                                                                                                                       |
| [**ADS \_ SYSTEMFLAG \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)                  | Especifica los tipos de atributos representados por un **objeto attributeSchema.**                                                                                                                                                                                   |
| [**ENUMERACIÓN \_ DE MARCA DE USUARIO DE \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)                   | Especifica las marcas usadas para manipular las propiedades del usuario.                                                                                                                                                                                                            |
| [**ENUMERACIÓN \_ DE \_ DIALECTO ADSI**](/windows/win32/api/iads/ne-iads-adsi_dialect_enum)                      | Especifica los dialectos de consulta ADSI disponibles.                                                                                                                                                                                                                          |
| [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)                                    | Especifica los tipos de datos usados para interpretar una cadena de sintaxis extendida adsi.                                                                                                                                                                                            |



 

## <a name="remarks"></a>Comentarios

Dado Visual Basic scripting Edition no pueden leer datos de una biblioteca de tipos, las aplicaciones VBScript no pueden reconocer constantes simbólicas como se define en estas enumeraciones. Use las constantes numéricas en su lugar para establecer las marcas adecuadas en una aplicación VBScript. Para usar las constantes simbólicas como una buena práctica de programación, escriba declaraciones explícitas de tales constantes, como se hace aquí, en aplicaciones VBScript.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
</dt> <dt>

[**IADsPathname::Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)
</dt> </dl>

 

 




