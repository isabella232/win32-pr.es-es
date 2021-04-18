---
description: Identifica una entrada en la base de datos de correcciones de compatibilidad.
ms.assetid: c092592d-a4f4-4b2f-9b03-c07951ed214a
title: ETIQUETA (Exposeenums2managed. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacbd3c8d29e1f41d7aaabc989848c561415ae4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650093"
---
# <a name="tag"></a>ETIQUETA

Identifica una entrada en la base de datos de correcciones de compatibilidad.

Las siguientes entradas son del tipo **\_ \_ List (tipo de etiqueta** ) (0x7000).



| Constante o valor                                                                                                                                                                                                                                                             | Descripción                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span id="TAG_DATABASE"></span><span id="tag_database"></span><dl> <dt>**Etiqueta \_ de BASE de datos**</dt> <dt>(0x1, \| **\_ \_ lista de tipos de etiquetas**)</dt> </dl>                               | Entrada de base de datos.<br/>                                                |
| <span id="TAG_LIBRARY"></span><span id="tag_library"></span><dl> <dt>**Etiqueta \_ de Biblioteca**</dt> <dt>( \| **lista de \_ tipos \_ de etiqueta** 0X2)</dt> </dl>                                  | Entrada de la biblioteca.<br/>                                                 |
| <span id="TAG_INEXCLUDE"></span><span id="tag_inexclude"></span><dl> <dt>**Etiqueta \_ de Inexclude**</dt> <dt>(0X3, \| **\_ \_ lista de tipos de etiquetas**)</dt> </dl>                            | Entrada incluir y excluir.<br/>                                     |
| <span id="TAG_SHIM"></span><span id="tag_shim"></span><dl> <dt>**Etiqueta \_ de Corrección de compatibilidad**</dt> <dt>( \| **\_ \_ lista de tipos de etiquetas** 0x4)</dt> </dl>                                           | Entrada de correcciones de compatibilidad (shim) que contiene la información de nombre y propósito.<br/>     |
| <span id="TAG_PATCH"></span><span id="tag_patch"></span><dl> <dt>**Etiqueta \_ de PATCH**</dt> <dt>( \| **lista de \_ tipos \_ de etiquetas** 0X5)</dt> </dl>                                        | Entrada de revisión que contiene la información de la revisión en memoria.<br/>  |
| <span id="TAG_APP"></span><span id="tag_app"></span><dl> <dt>**Etiqueta \_ de APP**</dt> <dt>( \| **lista de \_ tipos \_ de etiqueta** 0x6)</dt> </dl>                                              | Entrada de la aplicación.<br/>                                             |
| <span id="TAG_EXE"></span><span id="tag_exe"></span><dl> <dt>**Etiqueta \_ de EXE**</dt> <dt>( \| **lista de \_ tipos \_ de etiquetas** 0X7)</dt> </dl>                                              | Entrada ejecutable.<br/>                                              |
| <span id="TAG_MATCHING_FILE"></span><span id="tag_matching_file"></span><dl> <dt>**Etiqueta \_ de \_Archivo coincidente**</dt> <dt>( \| **lista de \_ tipos \_ de etiqueta** 0x8)</dt> </dl>               | Entrada de archivo coincidente.<br/>                                           |
| <span id="TAG_SHIM_REF"></span><span id="tag_shim_ref"></span><dl> <dt>**Etiqueta \_ de \_Referencia de Shim**</dt> <dt>( \| lista de tipos de etiqueta 0x9 \_ \_ )</dt> </dl>                                   | Entrada de definición de corrección de compatibilidad.<br/>                                         |
| <span id="TAG_PATCH_REF"></span><span id="tag_patch_ref"></span><dl> <dt>**Etiqueta \_ de \_Referencia de revisión**</dt> <dt>( \| **\_ \_ lista de tipos de etiquetas** 0xA)</dt> </dl>                           | Entrada de definición de revisión.<br/>                                        |
| <span id="TAG_LAYER"></span><span id="tag_layer"></span><dl> <dt>**Etiqueta \_ de CAPA**</dt> <dt>( \| **lista de \_ tipos \_ de etiqueta** 0xB)</dt> </dl>                                        | Entrada de corrección de compatibilidad de capas.<br/>                                              |
| <span id="TAG_FILE"></span><span id="tag_file"></span><dl> <dt>**Etiqueta \_ de ARCHIVO**</dt> <dt>( \| **lista de \_ tipos \_ de etiqueta** 0xc)</dt> </dl>                                           | Atributo de archivo usado en una entrada de corrección de compatibilidad.<br/>                           |
| <span id="TAG_APPHELP"></span><span id="tag_apphelp"></span><dl> <dt>**Etiqueta \_ de APPHELP**</dt> <dt>(la \| **\_ \_ lista de tipos de etiqueta** 0xd)</dt> </dl>                                  | Entrada de información de apphelp.<br/>                                     |
| <span id="TAG_LINK"></span><span id="tag_link"></span><dl> <dt>**Etiqueta \_ de LINK**</dt> <dt>( \| **lista de \_ tipos \_ de etiqueta** 0xE)</dt> </dl>                                           | Entrada de información de vínculo en línea de apphelp.<br/>                         |
| <span id="TAG_DATA"></span><span id="tag_data"></span><dl> <dt>**Etiqueta \_ de DATOS**</dt> <dt>( \| **lista de \_ tipos \_ de etiqueta** 0xF)</dt> </dl>                                           | Entrada de asignación de nombre y valor.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM"></span><span id="tag_msi_transform"></span><dl> <dt>**Etiqueta \_ de \_Transformación MSI**</dt> <dt>( \| **lista de \_ tipo \_ de etiqueta** 0x10)</dt> </dl>              | Entrada de transformación MSI.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM_REF"></span><span id="tag_msi_transform_ref"></span><dl> <dt>**Etiqueta \_ de \_ \_ Referencia de transformación MSI**</dt> <dt>( \| **\_ \_ lista de tipos de etiqueta** 0x11)</dt> </dl> | Entrada de definición de transformación MSI.<br/>                           |
| <span id="TAG_MSI_PACKAGE"></span><span id="tag_msi_package"></span><dl> <dt>**Etiqueta \_ de \_Paquete MSI**</dt> <dt>( \| **lista de \_ tipos \_ de etiqueta** 0X12)</dt> </dl>                    | Entrada del paquete MSI.<br/>                                             |
| <span id="TAG_FLAG"></span><span id="tag_flag"></span><dl> <dt>**Etiqueta \_ de MARCA**</dt> <dt>( \| **lista de \_ tipos \_ de etiquetas** 0x13)</dt> </dl>                                          | Entrada de marca.<br/>                                                    |
| <span id="TAG_MSI_CUSTOM_ACTION"></span><span id="tag_msi_custom_action"></span><dl> <dt>**Etiqueta \_ de \_ \_ Acción personalizada MSI**</dt> <dt>( \| **lista de \_ tipos \_ de etiqueta** 0x14)</dt> </dl> | Entrada de acción personalizada MSI.<br/>                                       |
| <span id="TAG_FLAG_REF"></span><span id="tag_flag_ref"></span><dl> <dt>**Etiqueta \_ de MARCA \_ ref**</dt> <dt>( \| **lista de \_ tipos \_ de etiqueta** 0x15)</dt> </dl>                             | Entrada de definición de marca.<br/>                                         |
| <span id="TAG_ACTION"></span><span id="tag_action"></span><dl> <dt>**Etiqueta \_ de ACCIÓN**</dt> <dt>( \| **lista de \_ tipos \_ de etiqueta** 0x16)</dt> </dl>                                    | Sin usar.<br/>                                                        |
| <span id="TAG_LOOKUP"></span><span id="tag_lookup"></span><dl> <dt>**Etiqueta \_ de BÚSQUEDA**</dt> <dt>( \| **lista de \_ tipos \_ de etiqueta** 0x17)</dt> </dl>                                    | Entrada de búsqueda usada para la búsqueda en una base de datos de controladores.<br/>             |
| <span id="TAG_STRINGTABLE"></span><span id="tag_stringtable"></span><dl> <dt>**Etiqueta \_ de STRINGTABLE**</dt> <dt>( \| **lista de \_ tipos \_ de etiquetas** 0x801)</dt> </dl>                    | Entrada de la tabla de cadenas.<br/>                                            |
| <span id="TAG_INDEXES"></span><span id="tag_indexes"></span><dl> <dt>**Etiqueta \_ de ÍNDICES**</dt> <dt>( \| **\_ \_ lista de tipos de etiqueta** 0x802)</dt> </dl>                                | Entrada de índices que define todos los índices de una base de datos de correcciones de compatibilidad (shim).<br/> |
| <span id="TAG_INDEX"></span><span id="tag_index"></span><dl> <dt>**Etiqueta \_ de INDEX**</dt> <dt>( \| **lista de \_ tipos \_ de etiqueta** 0x803)</dt> </dl>                                      | Entrada de índice que define un índice en una base de datos de Shim.<br/>          |



Las siguientes entradas son de tipo **tag \_ Type \_ STRINGREF** (0x6000).



| Constante o valor                                                                                                                                                                                                                                                                     | Descripción                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="TAG_NAME"></span><span id="tag_name"></span><dl> <dt>**Etiqueta \_ de NOMBRE**</dt> <dt>(0x1, \| **tipo de etiqueta \_ \_ STRINGREF**)</dt> </dl>                                              | Atributo de nombre.<br/>                                                                    |
| <span id="TAG_DESCRIPTION"></span><span id="tag_description"></span><dl> <dt>**Etiqueta \_ de Descripción**</dt> <dt>( \| **tipo de etiqueta 0X2 \_ \_ STRINGREF**)</dt> </dl>                         | Entrada de descripción.<br/>                                                                 |
| <span id="TAG_MODULE"></span><span id="tag_module"></span><dl> <dt>**Etiqueta \_ de MODULE**</dt> <dt>(0X3 ( \| **tipo de etiqueta \_ \_ STRINGREF**)</dt> </dl>                                        | Atributo de módulo.<br/>                                                                  |
| <span id="TAG_API"></span><span id="tag_api"></span><dl> <dt>**Etiqueta \_ de API**</dt> <dt>(0x4 \| **tipo de etiqueta \_ \_ STRINGREF**)</dt> </dl>                                                 | Entrada de la API.<br/>                                                                         |
| <span id="TAG_VENDOR"></span><span id="tag_vendor"></span><dl> <dt>**Etiqueta \_ de VENDOR**</dt> <dt>( \| **tipo de etiqueta 0X5 \_ \_ STRINGREF**)</dt> </dl>                                        | Atributo Vendor Name.<br/>                                                             |
| <span id="TAG_APP_NAME"></span><span id="tag_app_name"></span><dl> <dt>**Etiqueta \_ de \_Nombre**</dt> de la aplicación <dt>( \| **tipo de etiqueta 0x6 \_ \_ STRINGREF**)</dt> </dl>                                 | Atributo de nombre de aplicación que describe una entrada de aplicación en una base de datos de corrección de compatibilidad.<br/> |
| <span id="TAG_COMMAND_LINE"></span><span id="tag_command_line"></span><dl> <dt>**Etiqueta \_ de \_Línea de comandos**</dt> <dt>( \| **tipo de etiqueta 0x8 \_ \_ STRINGREF**)</dt> </dl>                     | Atributo de línea de comandos que se usa al pasar argumentos a una corrección de compatibilidad, por ejemplo.<br/> |
| <span id="TAG_COMPANY_NAME"></span><span id="tag_company_name"></span><dl> <dt>**Etiqueta \_ de \_Nombre**</dt> de la compañía <dt>( \| **tipo de etiqueta 0x9 \_ \_ STRINGREF**)</dt> </dl>                     | Atributo de nombre de la compañía.<br/>                                                            |
| <span id="TAG_DLLFILE"></span><span id="tag_dllfile"></span><dl> <dt>**Etiqueta \_ de DLLFILE**</dt> <dt>( \| **tipo de etiqueta 0xA \_ \_ STRINGREF**)</dt> </dl>                                     | Atributo de archivo DLL para una entrada de corrección de compatibilidad.<br/>                                               |
| <span id="TAG_WILDCARD_NAME"></span><span id="tag_wildcard_name"></span><dl> <dt>**Etiqueta \_ de \_Nombre de comodín**</dt> <dt>( \| **tipo de etiqueta 0xB \_ \_ STRINGREF**)</dt> </dl>                  | Atributo de nombre comodín para una entrada ejecutable con un carácter comodín como nombre de archivo.<br/>  |
| <span id="TAG_PRODUCT_NAME"></span><span id="tag_product_name"></span><dl> <dt>**Etiqueta \_ de \_Nombre del producto**</dt> <dt>(0x10 ( \| **tipo de etiqueta \_ \_ STRINGREF**)</dt> </dl>                    | Atributo Product Name.<br/>                                                            |
| <span id="TAG_PRODUCT_VERSION"></span><span id="tag_product_version"></span><dl> <dt>**Etiqueta \_ de \_Versión del producto**</dt> <dt>( \| **tipo de etiqueta 0x11 \_ \_ STRINGREF**)</dt> </dl>           | Atributo de versión del producto.<br/>                                                         |
| <span id="TAG_FILE_DESCRIPTION"></span><span id="tag_file_description"></span><dl> <dt>**Etiqueta \_ de \_Descripción del archivo**</dt> <dt>( \| **tipo de etiqueta 0X12 \_ \_ STRINGREF**)</dt> </dl>        | Atributo de Descripción del archivo.<br/>                                                        |
| <span id="TAG_FILE_VERSION"></span><span id="tag_file_version"></span><dl> <dt>**Etiqueta \_ de \_Versión del archivo**</dt> <dt>( \| **tipo de etiqueta 0x13 \_ \_ STRINGREF**)</dt> </dl>                    | Atributo de versión de archivo.<br/>                                                            |
| <span id="TAG_ORIGINAL_FILENAME"></span><span id="tag_original_filename"></span><dl> <dt>**Etiqueta \_ de \_Nombre de archivo original**</dt> <dt>(tipo de \| **etiqueta 0x14 \_ \_ STRINGREF**)</dt> </dl>     | Atributo de nombre de archivo original.<br/>                                                      |
| <span id="TAG_INTERNAL_NAME"></span><span id="tag_internal_name"></span><dl> <dt>**Etiqueta \_ de \_Nombre interno**</dt> <dt>( \| **tipo de etiqueta 0x15 \_ \_ STRINGREF**)</dt> </dl>                 | Atributo de nombre de archivo interno.<br/>                                                      |
| <span id="TAG_LEGAL_COPYRIGHT"></span><span id="tag_legal_copyright"></span><dl> <dt>**Etiqueta \_ de \_Copyright legal**</dt> <dt>( \| **tipo de etiqueta 0x16 \_ \_ STRINGREF**)</dt> </dl>           | Atributo de copyright.<br/>                                                               |
| <span id="TAG_16BIT_DESCRIPTION"></span><span id="tag_16bit_description"></span><dl> <dt>**Etiqueta de \_ 16 bits \_ Descripción**</dt> <dt>(tipo de \| **etiqueta 0x17 \_ \_ STRINGREF**)</dt> </dl>     | atributo de descripción de 16 bits.<br/>                                                      |
| <span id="TAG_APPHELP_DETAILS"></span><span id="tag_apphelp_details"></span><dl> <dt>**Etiqueta \_ de \_Detalles de APPHELP**</dt> <dt>( \| **tipo de etiqueta 0x18 \_ \_ STRINGREF**)</dt> </dl>           | Atributo de información de mensaje de detalles de apphelp.<br/>                                     |
| <span id="TAG_LINK_URL"></span><span id="tag_link_url"></span><dl> <dt>**Etiqueta \_ de \_URL del vínculo**</dt> <dt>( \| **tipo de etiqueta 0x19 \_ \_ STRINGREF**)</dt> </dl>                                | Atributo URL de vínculo de apphelp en línea.<br/>                                                 |
| <span id="TAG_LINK_TEXT"></span><span id="tag_link_text"></span><dl> <dt>**Etiqueta \_ de \_Texto del vínculo**</dt> <dt>( \| **tipo de etiqueta 0x1A \_ \_ STRINGREF**)</dt> </dl>                             | Atributo de texto de vínculo en línea de apphelp.<br/>                                                |
| <span id="TAG_APPHELP_TITLE"></span><span id="tag_apphelp_title"></span><dl> <dt>**Etiqueta \_ de \_Título de APPHELP**</dt> <dt>( \| **tipo de etiqueta 0x1b \_ \_ STRINGREF**)</dt> </dl>                 | Atributo de título de apphelp.<br/>                                                           |
| <span id="TAG_APPHELP_CONTACT"></span><span id="tag_apphelp_contact"></span><dl> <dt>**Etiqueta \_ de \_Contacto de APPHELP**</dt> <dt>( \| **tipo de etiqueta 0x1c \_ \_ STRINGREF**)</dt> </dl>           | Atributo de contacto del proveedor de apphelp.<br/>                                                  |
| <span id="TAG_SXS_MANIFEST"></span><span id="tag_sxs_manifest"></span><dl> <dt>**Etiqueta \_ de \_Manifiesto SxS**</dt> <dt>( \| **tipo de etiqueta 0x1D \_ \_ STRINGREF**)</dt> </dl>                    | Entrada de manifiesto en paralelo.<br/>                                                       |
| <span id="TAG_DATA_STRING"></span><span id="tag_data_string"></span><dl> <dt>**Etiqueta \_ de \_Cadena de datos**</dt> <dt>( \| **tipo de etiqueta 0x1E \_ \_ STRINGREF**)</dt> </dl>                       | Atributo de cadena para una entrada de datos.<br/>                                                 |
| <span id="TAG_MSI_TRANSFORM_FILE"></span><span id="tag_msi_transform_file"></span><dl> <dt>**Etiqueta \_ de \_ \_ Archivo de transformación MSI**</dt> <dt>( \| **tipo de etiqueta 0x1F \_ \_ STRINGREF**)</dt> </dl> | Atributo de nombre de archivo de una entrada de transformación MSI.<br/>                                |
| <span id="TAG_16BIT_MODULE_NAME"></span><span id="tag_16bit_module_name"></span><dl> <dt>**\_ Nombre del \_ módulo \_ de 16 bits de etiquetas**</dt> <dt>(tipo de \| **etiqueta 0x20 \_ \_ STRINGREF**)</dt> </dl>    | atributo de nombre de módulo de 16 bits.<br/>                                                      |
| <span id="TAG_LAYER_DISPLAYNAME"></span><span id="tag_layer_displayname"></span><dl> <dt>**Etiqueta \_ de NIVEL \_ DISPLAYNAME**</dt> <dt>( \| **tipo de etiqueta 0x21 \_ \_ STRINGREF**)</dt> </dl>     | Sin usar.<br/>                                                                            |
| <span id="TAG_COMPILER_VERSION"></span><span id="tag_compiler_version"></span><dl> <dt>**Etiqueta \_ de \_Versión del COMpilador**</dt> <dt>( \| **tipo de etiqueta 0x22 \_ \_ STRINGREF**)</dt> </dl>        | Versión del compilador de base de datos Shim.<br/>                                                    |
| <span id="TAG_ACTION_TYPE"></span><span id="tag_action_type"></span><dl> <dt>**Etiqueta \_ de \_Tipo de acción**</dt> <dt>( \| **tipo de etiqueta 0x23 \_ \_ STRINGREF**)</dt> </dl>                       | Sin usar.<br/>                                                                            |
| <span id="TAG_EXPORT_NAME"></span><span id="tag_export_name"></span><dl> <dt>**Etiqueta \_ de EXPORT \_ Name**</dt> <dt>( \| **tipo de etiqueta 0x24 \_ \_ STRINGREF**)</dt> </dl>                       | Atributo de nombre de archivo de exportación.<br/>                                                        |



Las siguientes entradas son del tipo **de \_ etiqueta \_ DWORD** (0x4000).



| Constante o valor                                                                                                                                                                                                                                                                    | Descripción                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| <span id="TAG_SIZE"></span><span id="tag_size"></span><dl> <dt>**Etiqueta \_ de TAMAÑO**</dt> <dt>(0x1 \| **tipo de etiqueta \_ \_ DWORD**)</dt> </dl>                                                 | Atributo de tamaño de archivo.<br/>                                                                                  |
| <span id="TAG_OFFSET"></span><span id="tag_offset"></span><dl> <dt>**Etiqueta \_ de DESPLAZAMIENTO**</dt> <dt>( \| **tipo de etiqueta 0X2 \_ \_ DWORD**)</dt> </dl>                                           | Sin usar.<br/>                                                                                               |
| <span id="TAG_CHECKSUM"></span><span id="tag_checksum"></span><dl> <dt>**Etiqueta \_ de CHECKSUM**</dt> <dt>(0X3 ( \| **tipo de etiqueta \_ \_ DWORD**)</dt> </dl>                                     | Atributo checksum del archivo.<br/>                                                                              |
| <span id="TAG_SHIM_TAGID"></span><span id="tag_shim_tagid"></span><dl> <dt>**Etiqueta \_ de Corrección \_ de compatibilidad**</dt> <dt>( \| **\_ tipo de \_ etiqueta**)</dt> . </dl>                              | Atributo **de** corrección de compatibilidad.<br/>                                                                             |
| <span id="TAG_PATCH_TAGID"></span><span id="tag_patch_tagid"></span><dl> <dt>**Etiqueta \_ de PATCH \_ TAGID**</dt> <dt>( \| **tipo de etiqueta 0X5 \_ \_ DWORD**)</dt> </dl>                           | Atributo patch **TAGID** .<br/>                                                                            |
| <span id="TAG_MODULE_TYPE"></span><span id="tag_module_type"></span><dl> <dt>**Etiqueta \_ de \_Tipo de módulo**</dt> <dt>( \| **tipo de etiqueta 0x6 \_ \_ DWORD**)</dt> </dl>                           | Atributo de tipo de módulo.<br/>                                                                                |
| <span id="TAG_VERDATEHI"></span><span id="tag_verdatehi"></span><dl> <dt>**Etiqueta \_ de VERDATEHI**</dt> <dt>( \| **tipo de etiqueta 0X7 \_ \_ DWORD**)</dt> </dl>                                  | Parte de orden superior del atributo de fecha de versión de archivo.<br/>                                                |
| <span id="TAG_VERDATELO"></span><span id="tag_verdatelo"></span><dl> <dt>**Etiqueta \_ de VERDATELO**</dt> <dt>( \| **tipo de etiqueta 0x8 \_ \_ DWORD**)</dt> </dl>                                  | Parte de orden inferior del atributo de fecha de versión de archivo.<br/>                                                 |
| <span id="TAG_VERFILEOS"></span><span id="tag_verfileos"></span><dl> <dt>**Etiqueta \_ de VERFILEOS**</dt> <dt>( \| **tipo de etiqueta 0x9 \_ \_ DWORD**)</dt> </dl>                                  | Atributo de versión de archivo del sistema operativo.<br/>                                                              |
| <span id="TAG_VERFILETYPE"></span><span id="tag_verfiletype"></span><dl> <dt>**Etiqueta \_ de VERFILETYPE**</dt> <dt>( \| **tipo de etiqueta 0xA \_ \_ DWORD**)</dt> </dl>                            | Atributo de tipo de archivo.<br/>                                                                                  |
| <span id="TAG_PE_CHECKSUM"></span><span id="tag_pe_checksum"></span><dl> <dt>**Etiqueta \_ de \_Suma de comprobación de PE**</dt> <dt>(tipo de etiqueta 0xB \| **\_ \_ DWORD**)</dt> </dl>                           | Atributo de suma de comprobación del archivo PE.<br/>                                                                           |
| <span id="TAG_PREVOSMAJORVER"></span><span id="tag_prevosmajorver"></span><dl> <dt>**Etiqueta \_ de PREVOSMAJORVER**</dt> <dt>( \| **tipo de etiqueta 0xc \_ \_ DWORD**)</dt> </dl>                   | Atributo de versión principal del sistema operativo.<br/>                                                             |
| <span id="TAG_PREVOSMINORVER"></span><span id="tag_prevosminorver"></span><dl> <dt>**Etiqueta \_ de PREVOSMINORVER**</dt> <dt>(el \| **tipo de etiqueta 0xd \_ \_ DWORD**)</dt> </dl>                   | Atributo de versión secundaria del sistema operativo.<br/>                                                             |
| <span id="TAG_PREVOSPLATFORMID"></span><span id="tag_prevosplatformid"></span><dl> <dt>**Etiqueta \_ de PREVOSPLATFORMID**</dt> <dt>( \| **tipo de etiqueta 0xE \_ \_ DWORD**)</dt> </dl>             | Atributo de identificador de plataforma del sistema operativo.<br/>                                                       |
| <span id="TAG_PREVOSBUILDNO"></span><span id="tag_prevosbuildno"></span><dl> <dt>**Etiqueta \_ de PREVOSBUILDNO**</dt> <dt>( \| **tipo de etiqueta 0xF \_ \_ DWORD**)</dt> </dl>                      | Atributo de número de compilación del sistema operativo.<br/>                                                              |
| <span id="TAG_PROBLEMSEVERITY"></span><span id="tag_problemseverity"></span><dl> <dt>**Etiqueta \_ de PROBLEMSEVERITY**</dt> <dt>(0x10 ( \| **tipo de etiqueta \_ \_ DWORD**)</dt> </dl>               | Atributo de bloqueo de una entrada de apphelp. Esto determina si la aplicación está bloqueada de forma rígida o parcial.<br/> |
| <span id="TAG_LANGID"></span><span id="tag_langid"></span><dl> <dt>**Etiqueta \_ de LANGID**</dt> <dt>( \| **tipo de etiqueta 0x11 \_ \_ DWORD**)</dt> </dl>                                          | Identificador de idioma de una entrada de apphelp.<br/>                                                              |
| <span id="TAG_VER_LANGUAGE"></span><span id="tag_ver_language"></span><dl> <dt>**Etiqueta \_ de \_Idioma de ver**</dt> <dt>( \| **tipo de etiqueta 0X12 \_ \_ DWORD**)</dt> </dl>                       | Atributo de versión de idioma de un archivo.<br/>                                                                 |
| <span id="TAG_ENGINE"></span><span id="tag_engine"></span><dl> <dt>**Etiqueta \_ de ENGINE**</dt> <dt>( \| **tipo de etiqueta 0x14 \_ \_ DWORD**)</dt> </dl>                                          | Sin usar.<br/>                                                                                               |
| <span id="TAG_HTMLHELPID"></span><span id="tag_htmlhelpid"></span><dl> <dt>**Etiqueta \_ de HTMLHELPID**</dt> <dt>( \| **tipo de etiqueta 0x15 \_ \_ DWORD**)</dt> </dl>                              | Atributo de identificador de ayuda para una entrada de apphelp.<br/>                                                       |
| <span id="TAG_INDEX_FLAGS"></span><span id="tag_index_flags"></span><dl> <dt>**Etiqueta \_ de \_Marcas de índice**</dt> <dt>( \| **tipo de etiqueta 0x16 \_ \_ DWORD**)</dt> </dl>                          | Marca el atributo para una entrada de índice.<br/>                                                                   |
| <span id="TAG_FLAGS"></span><span id="tag_flags"></span><dl> <dt>**Etiqueta \_ de MARCAS**</dt> <dt>( \| **tipo de etiqueta 0x17 \_ \_ DWORD**)</dt> </dl>                                             | Marca el atributo para una entrada de apphelp.<br/>                                                                 |
| <span id="TAG_DATA_VALUETYPE"></span><span id="tag_data_valuetype"></span><dl> <dt>**Etiqueta \_ de \_VALUETYPE de datos**</dt> <dt>( \| **tipo de etiqueta 0x18 \_ \_ DWORD**)</dt> </dl>                 | Atributo de tipo de datos de una entrada de datos.<br/>                                                                 |
| <span id="TAG_DATA_DWORD"></span><span id="tag_data_dword"></span><dl> <dt>**Etiqueta \_ de Dato \_ DWORD**</dt> <dt>( \| **tipo de etiqueta 0x19 \_ \_ DWORD**)</dt> </dl>                             | Atributo de valor **DWORD** para una entrada de datos.<br/>                                                           |
| <span id="TAG_LAYER_TAGID"></span><span id="tag_layer_tagid"></span><dl> <dt>**Etiqueta \_ de CAPA \_ TAGID**</dt> <dt>( \| **tipo de etiqueta 0x1A \_ \_ DWORD**)</dt> </dl>                          | Atributo **TAGID** de Shim de capa.<br/>                                                                       |
| <span id="TAG_MSI_TRANSFORM_TAGID"></span><span id="tag_msi_transform_tagid"></span><dl> <dt>**Etiqueta \_ de \_Transformación MSI \_ TAGID**</dt> <dt>( \| **tipo de etiqueta 0x1b \_ \_ DWORD**)</dt> </dl> | Atributo **TAGID** de transformación MSI.<br/>                                                                    |
| <span id="TAG_LINKER_VERSION"></span><span id="tag_linker_version"></span><dl> <dt>**Etiqueta \_ de \_Versión del vinculador**</dt> <dt>( \| **tipo de etiqueta 0x1c \_ \_ DWORD**)</dt> </dl>                 | Atributo de versión del vinculador de un archivo.<br/>                                                                   |
| <span id="TAG_LINK_DATE"></span><span id="tag_link_date"></span><dl> <dt>**Etiqueta \_ de LINK \_ Date**</dt> <dt>( \| **tipo de etiqueta 0x1D \_ \_ DWORD**)</dt> </dl>                                | Atributo de fecha de vínculo de un archivo.<br/>                                                                        |
| <span id="TAG_UPTO_LINK_DATE"></span><span id="tag_upto_link_date"></span><dl> <dt>**Etiqueta \_ de \_ \_ Fecha de vínculo hasta la fecha**</dt> <dt>(tipo de \| **etiqueta 0x1E \_ \_ DWORD**)</dt> </dl>                | Atributo de fecha de vínculo de un archivo. La búsqueda de coincidencias se realiza hasta la fecha de este vínculo, incluida.<br/>                   |
| <span id="TAG_OS_SERVICE_PACK"></span><span id="tag_os_service_pack"></span><dl> <dt>**Etiqueta \_ de \_Service \_ Pack de sistema operativo**</dt> <dt>(tipo de \| **etiqueta 0x1F \_ \_ DWORD**)</dt> </dl>             | Atributo de Service Pack del sistema operativo para una entrada ejecutable.<br/>                                      |
| <span id="TAG_FLAG_TAGID"></span><span id="tag_flag_tagid"></span><dl> <dt>**Etiqueta \_ de MARCA \_ TAGID**</dt> <dt>( \| **tipo de etiqueta 0x20 \_ \_ DWORD**)</dt> </dl>                             | Atributo **TAGID** de Flags.<br/>                                                                            |
| <span id="TAG_RUNTIME_PLATFORM"></span><span id="tag_runtime_platform"></span><dl> <dt>**Etiqueta \_ de \_Plataforma en tiempo de ejecución**</dt> <dt>(tipo de \| **etiqueta 0x21 \_ \_ DWORD**)</dt> </dl>           | Atributo de plataforma en tiempo de ejecución de un archivo.<br/>                                                                |
| <span id="TAG_OS_SKU"></span><span id="tag_os_sku"></span><dl> <dt>**Etiqueta \_ de \_SKU de sistema operativo**</dt> <dt>( \| **tipo de etiqueta 0x22 \_ \_ DWORD**)</dt> </dl>                                         | Atributo SKU del sistema operativo para una entrada ejecutable.<br/>                                               |
| <span id="TAG_OS_PLATFORM"></span><span id="tag_os_platform"></span><dl> <dt>**Etiqueta \_ de \_Plataforma de sistema operativo**</dt> <dt>( \| **tipo de etiqueta 0x23 \_ \_ DWORD**)</dt> </dl>                          | Atributo de plataforma del sistema operativo.<br/>                                                                  |
| <span id="TAG_APP_NAME_RC_ID"></span><span id="tag_app_name_rc_id"></span><dl> <dt>**Etiqueta \_ de Nombre de la aplicación \_ \_ RC \_ ID**</dt> <dt>( \| **tipo de etiqueta 0x24 \_ \_ DWORD**)</dt> </dl>               | Atributo de identificador de recurso de nombre de aplicación para entradas de apphelp.<br/>                                   |
| <span id="TAG_VENDOR_NAME_RC_ID"></span><span id="tag_vendor_name_rc_id"></span><dl> <dt>**Etiqueta \_ de \_ \_ \_ Identificador de nombre de proveedor RC**</dt> <dt>( \| **tipo de etiqueta 0x25 \_ \_ DWORD**)</dt> </dl>      | Nombre del proveedor atributo Identificador de recurso para entradas de apphelp.<br/>                                        |
| <span id="TAG_SUMMARY_MSG_RC_ID"></span><span id="tag_summary_msg_rc_id"></span><dl> <dt>**Etiqueta \_ de Resumen \_ mens \_ \_ . RC**</dt> <dt>( \| **tipo de etiqueta 0x26 \_ \_ DWORD**)</dt> </dl>      | Atributo de identificador de recurso de Resumen de mensajes para entradas de apphelp.<br/>                                    |
| <span id="TAG_VISTA_SKU"></span><span id="tag_vista_sku"></span><dl> <dt>**Etiqueta \_ de \_SKU de vista**</dt> <dt>( \| **tipo de etiqueta 0x27 \_ \_ DWORD**)</dt> </dl>                                | Atributo SKU de Windows Vista.<br/>                                                                          |
| <span id="TAG_DESCRIPTION_RC_ID"></span><span id="tag_description_rc_id"></span><dl> <dt>**Etiqueta \_ de Descripción \_ RC \_ ID**</dt> <dt>( \| **tipo de etiqueta 0x28 \_ \_ DWORD**)</dt> </dl>       | Descripción atributo de identificador de recurso para entradas de apphelp.<br/>                                        |
| <span id="TAG_PARAMETER1_RC_ID"></span><span id="tag_parameter1_rc_id"></span><dl> <dt>**Etiqueta \_ de PARÁMETRO1 \_ RC \_ ID**</dt> <dt>( \| **tipo de etiqueta 0x29 \_ \_ DWORD**)</dt> </dl>          | Atributo de identificador de recurso parámetro1 para entradas de apphelp.<br/>                                         |
| <span id="TAG_TAGID"></span><span id="tag_tagid"></span><dl> <dt>**Etiqueta \_ de TAGID**</dt> <dt>( \| **tipo de etiqueta 0x801 \_ \_ DWORD**)</dt> </dl>                                            | **TAGID** (atributo).<br/>                                                                                  |



La entrada siguiente es de tipo **\_ \_ cadena de tipo de etiqueta** (0x8000).



| Constante o valor                                                                                                                                                                                                                                                            | Descripción                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------|
| <span id="TAG_STRINGTABLE_ITEM"></span><span id="tag_stringtable_item"></span><dl> <dt>**Etiqueta \_ de \_Elemento stringtable**</dt> <dt>( \| **cadena de \_ tipo \_ de etiqueta** 0x801)</dt> </dl> | Entrada de elemento de tabla de cadena.<br/> |



Las siguientes entradas son de tipo **etiqueta \_ \_ null** (0x1000).



| Constante o valor                                                                                                                                                                                                                                                                            | Descripción                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span id="TAG_INCLUDE"></span><span id="tag_include"></span><dl> <dt>**Etiqueta \_ de INCLUDE**</dt> <dt>(0x1 \| **tipo de etiqueta \_ \_ null**)</dt> </dl>                                                 | Incluir entrada de lista.<br/>                           |
| <span id="TAG_GENERAL"></span><span id="tag_general"></span><dl> <dt>**Etiqueta \_ de GENERAL**</dt> <dt>( \| **tipo de etiqueta 0X2 \_ \_ nulo**)</dt> </dl>                                                 | Entrada de corrección de compatibilidad de uso general.<br/>                   |
| <span id="TAG_MATCH_LOGIC_NOT"></span><span id="tag_match_logic_not"></span><dl> <dt>**Etiqueta \_ de La \_ lógica \_ de coincidencia no**</dt> <dt>(0X3 \| **tipo de etiqueta \_ \_ null**)</dt> </dl>                       | NO coincide con la entrada lógica.<br/>                  |
| <span id="TAG_APPLY_ALL_SHIMS"></span><span id="tag_apply_all_shims"></span><dl> <dt>**Etiqueta \_ de APLICAR \_ todas las \_ correcciones de compatibilidad**</dt> <dt>(tipo de \| **etiqueta 0x4 \_ \_ null**)</dt> </dl>                       | Sin usar.<br/>                                       |
| <span id="TAG_USE_SERVICE_PACK_FILES"></span><span id="tag_use_service_pack_files"></span><dl> <dt>**Etiqueta \_ de USAR \_ \_ \_ archivos de Service Pack**</dt> <dt>( \| **tipo de etiqueta 0X5 \_ \_ null**)</dt> </dl> | Información de Service Pack para entradas de apphelp.<br/> |
| <span id="TAG_MITIGATION_OS"></span><span id="tag_mitigation_os"></span><dl> <dt>**Etiqueta \_ de \_Sistema operativo de mitigación**</dt> <dt>( \| **tipo de etiqueta 0x6 \_ \_ nulo**)</dt> </dl>                              | Mitigación en la entrada de ámbito del sistema operativo.<br/>   |
| <span id="TAG_BLOCK_UPGRADE"></span><span id="tag_block_upgrade"></span><dl> <dt>**Etiqueta \_ de BLOQUEAR \_ actualización**</dt> <dt>( \| **tipo de etiqueta 0X7 \_ \_ null**)</dt> </dl>                              | Entrada de bloque de actualización.<br/>                          |
| <span id="TAG_INCLUDEEXCLUDEDLL"></span><span id="tag_includeexcludedll"></span><dl> <dt>**Etiqueta \_ de INCLUDEEXCLUDEDLL**</dt> <dt>( \| **tipo de etiqueta 0x8 \_ \_ null**)</dt> </dl>                   | Entrada de inclusión/exclusión de DLL.<br/>                    |



Las siguientes entradas son del tipo de etiqueta de tipo **\_ \_ QWord** (0x5000).



| Constante o valor                                                                                                                                                                                                                                                                                   | Descripción                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TAG_TIME"></span><span id="tag_time"></span><dl> <dt>**Etiqueta \_ de TIME**</dt> <dt>(0x1 \| **tipo de etiqueta \_ \_ QWord**)</dt> </dl>                                                                | Atributo de hora.<br/>                                                                                     |
| <span id="TAG_BIN_FILE_VERSION"></span><span id="tag_bin_file_version"></span><dl> <dt>**Etiqueta \_ de \_ \_ Versión del archivo bin**</dt> <dt>( \| **tipo de etiqueta 0X2 \_ \_ QWord**)</dt> </dl>                          | Atributo de versión del archivo bin para entradas de archivo.<br/>                                                        |
| <span id="TAG_BIN_PRODUCT_VERSION"></span><span id="tag_bin_product_version"></span><dl> <dt>**Etiqueta \_ de \_ \_ Versión del producto bin**</dt> <dt>(0X3 \| **tipo de etiqueta \_ \_ QWord**)</dt> </dl>                 | Atributo de versión del producto bin para entradas de archivo.<br/>                                                     |
| <span id="TAG_MODTIME"></span><span id="tag_modtime"></span><dl> <dt>**Etiqueta \_ de MODTIME**</dt> <dt>(0x4 \| **tipo de etiqueta \_ \_ QWord**)</dt> </dl>                                                       | Sin usar.<br/>                                                                                             |
| <span id="TAG_FLAG_MASK_KERNEL"></span><span id="tag_flag_mask_kernel"></span><dl> <dt>**Etiqueta \_ de \_ \_ Kernel de máscara de marca**</dt> <dt>(0X5 \| **tipo de etiqueta \_ \_ QWord**)</dt> </dl>                          | Atributo de máscara de marca de kernel.<br/>                                                                         |
| <span id="TAG_UPTO_BIN_PRODUCT_VERSION"></span><span id="tag_upto_bin_product_version"></span><dl> <dt>**Etiqueta \_ de \_Versión del \_ producto \_ bin**</dt> <dt>(tipo de \| **etiqueta 0x6 \_ \_ QWord**)</dt> </dl> | Atributo de versión del producto bin de un archivo. La búsqueda de coincidencias se realiza hasta e incluye esta versión del producto.<br/> |
| <span id="TAG_DATA_QWORD"></span><span id="tag_data_qword"></span><dl> <dt>**Etiqueta \_ de \_QWord de datos**</dt> <dt>( \| **tipo de etiqueta 0X7 \_ \_ QWord**)</dt> </dl>                                             | Atributo de valor **ULONGLONG** para una entrada de datos.<br/>                                                     |
| <span id="TAG_FLAG_MASK_USER"></span><span id="tag_flag_mask_user"></span><dl> <dt>**Etiqueta \_ de MARCAR \_ \_ usuario de máscara**</dt> <dt>( \| **\_ tipo de \_ etiqueta** 0x8)</dt> </dl>                                | Atributo de máscara de marca de usuario.<br/>                                                                           |
| <span id="TAG_FLAGS_NTVDM1"></span><span id="tag_flags_ntvdm1"></span><dl> <dt>**Etiqueta \_ de FLAGs \_ NTVDM1**</dt> <dt>( \| **tipo de etiqueta 0x9 \_ \_ QWord**)</dt> </dl>                                       | Atributo de máscara de marca NTVDM1.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM2"></span><span id="tag_flags_ntvdm2"></span><dl> <dt>**Etiqueta \_ de FLAGs \_ NTVDM2**</dt> <dt>( \| **tipo de etiqueta 0xA \_ \_ QWord**)</dt> </dl>                                       | Atributo de máscara de marca NTVDM2.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM3"></span><span id="tag_flags_ntvdm3"></span><dl> <dt>**Etiqueta \_ de FLAGs \_ NTVDM3**</dt> <dt>( \| **tipo de etiqueta 0xB \_ \_ QWord**)</dt> </dl>                                       | Atributo de máscara de marca NTVDM3.<br/>                                                                         |
| <span id="TAG_FLAG_MASK_SHELL"></span><span id="tag_flag_mask_shell"></span><dl> <dt>**Etiqueta \_ de \_ \_ Shell de máscara de marca**</dt> <dt>( \| **\_ tipo \_ de etiqueta** 0xc)</dt> </dl>                             | Atributo de máscara de marca de Shell.<br/>                                                                          |
| <span id="TAG_UPTO_BIN_FILE_VERSION"></span><span id="tag_upto_bin_file_version"></span><dl> <dt>**Etiqueta \_ de \_Versión del \_ archivo \_ bin**</dt> <dt>(0xd, \| **tipo de etiqueta \_ \_ QWord**)</dt> </dl>          | Atributo de versión del archivo bin de un archivo. La búsqueda de coincidencias se realiza hasta la versión de este archivo incluida.<br/>       |
| <span id="TAG_FLAG_MASK_FUSION"></span><span id="tag_flag_mask_fusion"></span><dl> <dt>**Etiqueta \_ de \_ \_ Fusión de máscara de marca**</dt> <dt>(tipo de \| **etiqueta 0xE \_ \_ QWord**)</dt> </dl>                          | Atributo de máscara de marca de fusión.<br/>                                                                         |
| <span id="TAG_FLAG_PROCESSPARAM"></span><span id="tag_flag_processparam"></span><dl> <dt>**Etiqueta \_ de FLAG \_ PROCESSPARAM**</dt> <dt>( \| **tipo de etiqueta 0xF \_ \_ QWord**)</dt> </dl>                        | Atributo de marcador de parámetro de proceso.<br/>                                                                       |
| <span id="TAG_FLAG_LUA"></span><span id="tag_flag_lua"></span><dl> <dt>**Etiqueta \_ de MARCA \_ Lua**</dt> <dt>(0x10 \| **tipo de etiqueta \_ \_ QWord**)</dt> </dl>                                                  | Atributo de marca LUA.<br/>                                                                                 |
| <span id="TAG_FLAG_INSTALL"></span><span id="tag_flag_install"></span><dl> <dt>**Etiqueta \_ de MARCA de \_ instalación**</dt> <dt>( \| **tipo de etiqueta 0x11 \_ \_ QWord**)</dt> </dl>                                      | Atributo de marca de instalación.<br/>                                                                             |



Las siguientes entradas son de tipo **etiqueta \_ \_ binaria** (0x9000).



| Constante o valor                                                                                                                                                                                                                                                     | Descripción                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="TAG_PATCH_BITS"></span><span id="tag_patch_bits"></span><dl> <dt>**Etiqueta \_ de \_Bits de revisión**</dt> <dt>( \| **tipo de etiqueta 0X2 \_ \_ binario**)</dt> </dl>              | Atributo de bits de archivo de revisión.<br/>                          |
| <span id="TAG_FILE_BITS"></span><span id="tag_file_bits"></span><dl> <dt>**Etiqueta \_ de \_Bits de archivo**</dt> <dt>(0X3 \| **tipo de etiqueta \_ \_ binario**)</dt> </dl>                 | Atributo de bits de archivo.<br/>                                |
| <span id="TAG_EXE_ID"></span><span id="tag_exe_id"></span><dl> <dt>**Etiqueta \_ de \_ID. de exe**</dt> <dt>(tipo de etiqueta de 0x4 \| **\_ \_ binario**)</dt> </dl>                          | Atributo **GUID** de una entrada ejecutable.<br/>          |
| <span id="TAG_DATA_BITS"></span><span id="tag_data_bits"></span><dl> <dt>**Etiqueta \_ de \_Bits de datos**</dt> <dt>( \| **tipo de etiqueta 0X5 \_ \_ binario**)</dt> </dl>                 | Atributo de bits de datos.<br/>                                |
| <span id="TAG_MSI_PACKAGE_ID"></span><span id="tag_msi_package_id"></span><dl> <dt>**Etiqueta \_ de \_ \_ Identificador de paquete MSI**</dt> <dt>( \| **tipo de etiqueta 0x6 \_ \_ binario**)</dt> </dl> | Atributo de identificador de paquete MSI de un paquete MSI.<br/> |
| <span id="TAG_DATABASE_ID"></span><span id="tag_database_id"></span><dl> <dt>**Etiqueta \_ de \_Identificador de base de datos**</dt> <dt>(tipo de \| **etiqueta 0X7 \_ \_ binario**)</dt> </dl>           | Atributo **GUID** de una base de datos.<br/>                   |
| <span id="TAG_INDEX_BITS"></span><span id="tag_index_bits"></span><dl> <dt>**Etiqueta \_ de \_Bits de índice**</dt> <dt>( \| **tipo de etiqueta 0x801 \_ \_ binario**)</dt> </dl>            | Atributo de bits de índice.<br/>                               |



Las siguientes entradas son del tipo **de \_ etiqueta \_ Word** (0x3000).



| Constante o valor                                                                                                                                                                                                                                      | Descripción                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="TAG_MATCH_MODE"></span><span id="tag_match_mode"></span><dl> <dt>**Etiqueta \_ de \_Modo de coincidencia**</dt> <dt>(0x1 \| **tipo de etiqueta \_ \_ Word**)</dt> </dl> | Atributo de modo de coincidencia.<br/>                   |
| <span id="TAG_TAG"></span><span id="tag_tag"></span><dl> <dt>**Etiqueta \_ de ETIQUETA**</dt> <dt>( \| **tipo de etiqueta 0x801 \_ \_ Word**)</dt> </dl>                     | Entrada de etiqueta.<br/>                              |
| <span id="TAG_INDEX_TAG"></span><span id="tag_index_tag"></span><dl> <dt>**Etiqueta \_ de \_Etiqueta de índice**</dt> <dt>( \| **tipo de etiqueta 0x802 \_ \_ Word**)</dt> </dl>  | Atributo de etiqueta de índice para una entrada de índice.<br/> |
| <span id="TAG_INDEX_KEY"></span><span id="tag_index_key"></span><dl> <dt>**Etiqueta \_ de \_Clave de índice**</dt> <dt>( \| **tipo de etiqueta 0x803 \_ \_ Word**)</dt> </dl>  | Atributo de clave de índice para una entrada de índice.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Exposeenums2managed. h (incluye Axextendenums. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de etiquetas](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




