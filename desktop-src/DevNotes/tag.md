---
description: Identifica una entrada en la base de datos shim.
ms.assetid: c092592d-a4f4-4b2f-9b03-c07951ed214a
title: TAG (Exposeenums2managed.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7e4df727245ead30ecefef0cd941148b8f4c76e2881ab19f41c3388934abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075799"
---
# <a name="tag"></a>ETIQUETA

Identifica una entrada en la base de datos shim.

Las siguientes entradas son de tipo **TAG \_ TYPE \_ LIST** (0x7000).



| Constante o valor                                                                                                                                                                                                                                                             | Descripción                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span id="TAG_DATABASE"></span><span id="tag_database"></span><dl> <dt>**TAG \_ DATABASE**</dt> <dt>(0x1 \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                               | Entrada de la base de datos.<br/>                                                |
| <span id="TAG_LIBRARY"></span><span id="tag_library"></span><dl> <dt>**TAG \_ LIBRARY**</dt> <dt>(0x2 \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                                  | Entrada de la biblioteca.<br/>                                                 |
| <span id="TAG_INEXCLUDE"></span><span id="tag_inexclude"></span><dl> <dt>**TAG \_ INEXCLUDE**</dt> <dt>(0x3 \| **LISTA DE TIPOS \_ DE \_ ETIQUETA**)</dt> </dl>                            | Incluya y excluya la entrada.<br/>                                     |
| <span id="TAG_SHIM"></span><span id="tag_shim"></span><dl> <dt>**TAG \_ SHIM**</dt> <dt>(0x4 \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                                           | Entrada de corrección de compatibilidad (SHIM) que contiene el nombre y la información de propósito.<br/>     |
| <span id="TAG_PATCH"></span><span id="tag_patch"></span><dl> <dt>**TAG \_ PATCH**</dt> <dt>(0x5 \| **TAG TYPE \_ \_ LIST**)</dt> </dl>                                        | Entrada de revisión que contiene la información de aplicación de revisiones en memoria.<br/>  |
| <span id="TAG_APP"></span><span id="tag_app"></span><dl> <dt>**TAG \_ APP**</dt> <dt>(0x6 \| **TAG TYPE \_ \_ LIST**)</dt> </dl>                                              | Entrada de la aplicación.<br/>                                             |
| <span id="TAG_EXE"></span><span id="tag_exe"></span><dl> <dt>**TAG \_ EXE**</dt> <dt>(0x7 \| **TAG TYPE \_ \_ LIST**)</dt> </dl>                                              | Entrada ejecutable.<br/>                                              |
| <span id="TAG_MATCHING_FILE"></span><span id="tag_matching_file"></span><dl> <dt>**TAG \_ ARCHIVO DE \_ COINCIDENCIA**</dt> <dt>(0x8 LISTA DE TIPOS \| **DE \_ \_ ETIQUETA**)</dt> </dl>               | Entrada de archivo correspondiente.<br/>                                           |
| <span id="TAG_SHIM_REF"></span><span id="tag_shim_ref"></span><dl> <dt>**TAG \_ SHIM \_ REF**</dt> <dt>(0x9 \| TAG TYPE \_ \_ LIST)</dt> </dl>                                   | Entrada de definición de correcciones de compatibilidad (SHIM).<br/>                                         |
| <span id="TAG_PATCH_REF"></span><span id="tag_patch_ref"></span><dl> <dt>**TAG \_ PATCH \_ REF**</dt> <dt>(0xA TAG TYPE \| **\_ \_ LIST**)</dt> </dl>                           | Entrada de definición de revisión.<br/>                                        |
| <span id="TAG_LAYER"></span><span id="tag_layer"></span><dl> <dt>**TAG \_ LAYER**</dt> <dt>(0xB \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                                        | Entrada de corrección de compatibilidad (shim) de capa.<br/>                                              |
| <span id="TAG_FILE"></span><span id="tag_file"></span><dl> <dt>**TAG \_ FILE**</dt> <dt>(0xC \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                                           | Atributo de archivo usado en una entrada de corrección de compatibilidad (shim).<br/>                           |
| <span id="TAG_APPHELP"></span><span id="tag_apphelp"></span><dl> <dt>**TAG \_ APPHELP**</dt> <dt>(0xD \| **LISTA DE TIPOS \_ DE \_ ETIQUETA**)</dt> </dl>                                  | Entrada de información de ayuda.<br/>                                     |
| <span id="TAG_LINK"></span><span id="tag_link"></span><dl> <dt>**TAG \_ LINK**</dt> <dt>(0xE \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                                           | Entrada de información de vínculo en línea de Apphelp.<br/>                         |
| <span id="TAG_DATA"></span><span id="tag_data"></span><dl> <dt>**TAG \_ DATA**</dt> <dt>(0xF \| **TAG TYPE \_ \_ LIST**)</dt> </dl>                                           | Entrada de asignación de nombre y valor.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM"></span><span id="tag_msi_transform"></span><dl> <dt>**TAG \_ MSI \_ TRANSFORM**</dt> <dt>(0x10 \| **TAG TYPE \_ \_ LIST**)</dt> </dl>              | Entrada de transformación MSI.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM_REF"></span><span id="tag_msi_transform_ref"></span><dl> <dt>**TAG \_ MSI \_ TRANSFORM \_ REF**</dt> <dt>(0x11 TAG TYPE \| **\_ \_ LIST**)</dt> </dl> | Entrada de definición de transformación MSI.<br/>                           |
| <span id="TAG_MSI_PACKAGE"></span><span id="tag_msi_package"></span><dl> <dt>**TAG \_ PAQUETE \_ MSI**</dt> <dt>(0x12 \| **LISTA DE TIPOS DE \_ \_ ETIQUETA**)</dt> </dl>                    | Entrada del paquete MSI.<br/>                                             |
| <span id="TAG_FLAG"></span><span id="tag_flag"></span><dl> <dt>**TAG \_ FLAG**</dt> <dt>(0x13 \| **TAG TYPE \_ \_ LIST**)</dt> </dl>                                          | Entrada de marca.<br/>                                                    |
| <span id="TAG_MSI_CUSTOM_ACTION"></span><span id="tag_msi_custom_action"></span><dl> <dt>**TAG \_ ACCIÓN \_ PERSONALIZADA \_ DE MSI**</dt> <dt>(0x14 LISTA DE TIPOS DE \| **\_ \_ ETIQUETA**)</dt> </dl> | Entrada de acción personalizada de MSI.<br/>                                       |
| <span id="TAG_FLAG_REF"></span><span id="tag_flag_ref"></span><dl> <dt>**TAG \_ FLAG \_ REF**</dt> <dt>(0x15 \| **TAG TYPE \_ \_ LIST**)</dt> </dl>                             | Entrada de definición de marca.<br/>                                         |
| <span id="TAG_ACTION"></span><span id="tag_action"></span><dl> <dt>**TAG \_ ACTION**</dt> <dt>(0x16 \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                                    | Sin usar.<br/>                                                        |
| <span id="TAG_LOOKUP"></span><span id="tag_lookup"></span><dl> <dt>**TAG \_ LOOKUP**</dt> <dt>(0x17 \| **TAG TYPE \_ \_ LIST**)</dt> </dl>                                    | Entrada de búsqueda usada para la búsqueda en una base de datos de controladores.<br/>             |
| <span id="TAG_STRINGTABLE"></span><span id="tag_stringtable"></span><dl> <dt>**TAG \_ STRINGTABLE**</dt> <dt>(0x801 \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                    | Entrada de tabla de cadenas.<br/>                                            |
| <span id="TAG_INDEXES"></span><span id="tag_indexes"></span><dl> <dt>**TAG \_ INDEXES**</dt> <dt>(0x802 \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                                | Entrada de índices que define todos los índices de una base de datos shim.<br/> |
| <span id="TAG_INDEX"></span><span id="tag_index"></span><dl> <dt>**TAG \_ INDEX**</dt> <dt>(0x803 \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                                      | Entrada de índice que define un índice en una base de datos shim.<br/>          |



Las siguientes entradas son de tipo **TAG \_ TYPE \_ STRINGREF** (0x6000).



| Constante o valor                                                                                                                                                                                                                                                                     | Descripción                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="TAG_NAME"></span><span id="tag_name"></span><dl> <dt>**TAG \_ NAME**</dt> <dt>(0X1 \| **TIPO DE ETIQUETA \_ \_ STRINGREF**)</dt> </dl>                                              | Atributo name.<br/>                                                                    |
| <span id="TAG_DESCRIPTION"></span><span id="tag_description"></span><dl> <dt>**TAG \_ DESCRIPTION**</dt> <dt>(0X2 \| **TIPO \_ DE ETIQUETA \_ STRINGREF**)</dt> </dl>                         | Entrada de descripción.<br/>                                                                 |
| <span id="TAG_MODULE"></span><span id="tag_module"></span><dl> <dt>**TAG \_ MODULE**</dt> <dt>(0x3 \| **TIPO \_ DE ETIQUETA \_ STRINGREF**)</dt> </dl>                                        | Atributo de módulo.<br/>                                                                  |
| <span id="TAG_API"></span><span id="tag_api"></span><dl> <dt>**TAG \_ API**</dt> <dt>(0X4 \| **TIPO \_ DE ETIQUETA \_ STRINGREF**)</dt> </dl>                                                 | Entrada de API.<br/>                                                                         |
| <span id="TAG_VENDOR"></span><span id="tag_vendor"></span><dl> <dt>**TAG \_ VENDOR**</dt> <dt>(0X5 \| **TIPO \_ DE ETIQUETA \_ STRINGREF**)</dt> </dl>                                        | Atributo de nombre de proveedor.<br/>                                                             |
| <span id="TAG_APP_NAME"></span><span id="tag_app_name"></span><dl> <dt>**TAG \_ NOMBRE \_ DE LA**</dt> APLICACIÓN <dt>(0X6 TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl>                                 | Atributo de nombre de aplicación que describe una entrada de aplicación en una base de datos de correcciones de compatibilidad (shim).<br/> |
| <span id="TAG_COMMAND_LINE"></span><span id="tag_command_line"></span><dl> <dt>**TAG \_ LÍNEA \_ DE COMANDOS**</dt> <dt>(0X8 TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl>                     | Atributo de línea de comandos que se usa al pasar argumentos a una corrección de compatibilidad (shim), por ejemplo.<br/> |
| <span id="TAG_COMPANY_NAME"></span><span id="tag_company_name"></span><dl> <dt>**TAG \_ COMPANY \_ NAME**</dt> <dt>(0X9 \| **TAG TYPE \_ \_ STRINGREF**)</dt> </dl>                     | Atributo de nombre de empresa.<br/>                                                            |
| <span id="TAG_DLLFILE"></span><span id="tag_dllfile"></span><dl> <dt>**TAG \_ DLLFILE**</dt> <dt>(0XA \| **TIPO \_ DE ETIQUETA \_ STRINGREF**)</dt> </dl>                                     | Atributo de archivo DLL para una entrada shim.<br/>                                               |
| <span id="TAG_WILDCARD_NAME"></span><span id="tag_wildcard_name"></span><dl> <dt>**TAG \_ NOMBRE \_ DE CARÁCTER COMODÍN**</dt> <dt>(0XB TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl>                  | Atributo de nombre de carácter comodín para una entrada ejecutable con un carácter comodín como nombre de archivo.<br/>  |
| <span id="TAG_PRODUCT_NAME"></span><span id="tag_product_name"></span><dl> <dt>**TAG \_ NOMBRE \_ DEL PRODUCTO**</dt> <dt>(0X10 TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl>                    | Atributo de nombre de producto.<br/>                                                            |
| <span id="TAG_PRODUCT_VERSION"></span><span id="tag_product_version"></span><dl> <dt>**TAG \_ VERSIÓN \_ DEL PRODUCTO**</dt> <dt>(0X11 TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl>           | Atributo de versión del producto.<br/>                                                         |
| <span id="TAG_FILE_DESCRIPTION"></span><span id="tag_file_description"></span><dl> <dt>**TAG \_ DESCRIPCIÓN \_ DEL ARCHIVO**</dt> <dt>(0X12 TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl>        | Atributo de descripción del archivo.<br/>                                                        |
| <span id="TAG_FILE_VERSION"></span><span id="tag_file_version"></span><dl> <dt>**TAG \_ VERSIÓN \_ DEL ARCHIVO**</dt> <dt>(0X13 TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl>                    | Atributo de versión de archivo.<br/>                                                            |
| <span id="TAG_ORIGINAL_FILENAME"></span><span id="tag_original_filename"></span><dl> <dt>**TAG \_ NOMBRE \_ DE ARCHIVO**</dt> ORIGINAL <dt>(0X14 TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl>     | Atributo de nombre de archivo original.<br/>                                                      |
| <span id="TAG_INTERNAL_NAME"></span><span id="tag_internal_name"></span><dl> <dt>**TAG \_ NOMBRE \_ INTERNO**</dt> <dt>(0X15 \| **TIPO DE ETIQUETA \_ \_ STRINGREF**)</dt> </dl>                 | Atributo de nombre de archivo interno.<br/>                                                      |
| <span id="TAG_LEGAL_COPYRIGHT"></span><span id="tag_legal_copyright"></span><dl> <dt>**TAG \_ COPYRIGHT \_ LEGAL**</dt> <dt>(0X16 \| **TIPO DE ETIQUETA \_ \_ STRINGREF**)</dt> </dl>           | Atributo copyright.<br/>                                                               |
| <span id="TAG_16BIT_DESCRIPTION"></span><span id="tag_16bit_description"></span><dl> <dt>**DESCRIPCIÓN \_ DE LA ETIQUETA DE 16 \_ BITS**</dt> <dt>(0X17 TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl>     | Atributo de descripción de 16 bits.<br/>                                                      |
| <span id="TAG_APPHELP_DETAILS"></span><span id="tag_apphelp_details"></span><dl> <dt>**TAG \_ DETALLES DE \_ APPHELP**</dt> <dt>(0X18 \| **TIPO DE \_ ETIQUETA \_ STRINGREF**)</dt> </dl>           | Atributo de información de mensajes de detalles de apphelp.<br/>                                     |
| <span id="TAG_LINK_URL"></span><span id="tag_link_url"></span><dl> <dt>**TAG \_ DIRECCIÓN \_ URL DE**</dt> VÍNCULO <dt>(0X19 TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl>                                | Atributo de dirección URL de vínculo en línea de Apphelp.<br/>                                                 |
| <span id="TAG_LINK_TEXT"></span><span id="tag_link_text"></span><dl> <dt>**TAG \_ TEXTO \_ DE VÍNCULO**</dt> <dt>(0X1A TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl>                             | Atributo de texto de vínculo en línea apphelp.<br/>                                                |
| <span id="TAG_APPHELP_TITLE"></span><span id="tag_apphelp_title"></span><dl> <dt>**TAG \_ TÍTULO \_ DE APPHELP**</dt> <dt>(0X1B \| **TIPO DE \_ ETIQUETA \_ STRINGREF**)</dt> </dl>                 | Atributo de título apphelp.<br/>                                                           |
| <span id="TAG_APPHELP_CONTACT"></span><span id="tag_apphelp_contact"></span><dl> <dt>**TAG \_ APPHELP \_ CONTACT**</dt> <dt>(0X1C \| **TIPO DE ETIQUETA \_ \_ STRINGREF**)</dt> </dl>           | Atributo de contacto del proveedor de Apphelp.<br/>                                                  |
| <span id="TAG_SXS_MANIFEST"></span><span id="tag_sxs_manifest"></span><dl> <dt>**TAG \_ MANIFIESTO DE \_ SXS**</dt> <dt>(0x1D \| **TIPO DE ETIQUETA \_ \_ STRINGREF**)</dt> </dl>                    | Entrada de manifiesto en paralelo.<br/>                                                       |
| <span id="TAG_DATA_STRING"></span><span id="tag_data_string"></span><dl> <dt>**TAG \_ CADENA \_ DE DATOS**</dt> <dt>(0X1E TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl>                       | Atributo de cadena para una entrada de datos.<br/>                                                 |
| <span id="TAG_MSI_TRANSFORM_FILE"></span><span id="tag_msi_transform_file"></span><dl> <dt>**TAG \_ ARCHIVO \_ DE TRANSFORMACIÓN DE \_ MSI**</dt> <dt>(0X1F TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl> | Atributo de nombre de archivo de una entrada de transformación MSI.<br/>                                |
| <span id="TAG_16BIT_MODULE_NAME"></span><span id="tag_16bit_module_name"></span><dl> TAG NOMBRE DEL MÓDULO DE <dt>**\_ 16 \_ \_ BITS**</dt> <dt>(0X20 \| **TIPO DE \_ ETIQUETA \_ STRINGREF**)</dt> </dl>    | Atributo de nombre de módulo de 16 bits.<br/>                                                      |
| <span id="TAG_LAYER_DISPLAYNAME"></span><span id="tag_layer_displayname"></span><dl> <dt>**TAG \_ LAYER \_ DISPLAYNAME**</dt> <dt>(0X21 \| **TIPO DE \_ ETIQUETA \_ STRINGREF**)</dt> </dl>     | Sin usar.<br/>                                                                            |
| <span id="TAG_COMPILER_VERSION"></span><span id="tag_compiler_version"></span><dl> <dt>**TAG \_ VERSIÓN \_ DEL COMPILADOR**</dt> <dt>(0X22 TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl>        | Versión del compilador de base de datos shim.<br/>                                                    |
| <span id="TAG_ACTION_TYPE"></span><span id="tag_action_type"></span><dl> <dt>**TAG \_ TIPO \_ DE ACCIÓN**</dt> <dt>(0X23 TIPO DE ETIQUETA \| **\_ \_ STRINGREF**)</dt> </dl>                       | Sin usar.<br/>                                                                            |
| <span id="TAG_EXPORT_NAME"></span><span id="tag_export_name"></span><dl> <dt>**TAG \_ EXPORT \_ NAME**</dt> <dt>(0X24 \| **TAG TYPE \_ \_ STRINGREF**)</dt> </dl>                       | Exporte el atributo de nombre de archivo.<br/>                                                        |



Las siguientes entradas son de tipo **TAG \_ TYPE \_ DWORD** (0x4000).



| Constante o valor                                                                                                                                                                                                                                                                    | Descripción                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| <span id="TAG_SIZE"></span><span id="tag_size"></span><dl> <dt>**TAG \_ SIZE**</dt> <dt>(0X1 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                                                 | Atributo de tamaño de archivo.<br/>                                                                                  |
| <span id="TAG_OFFSET"></span><span id="tag_offset"></span><dl> <dt>**TAG \_ OFFSET**</dt> <dt>(0x2 \| **TIPO \_ DE ETIQUETA \_ DWORD**)</dt> </dl>                                           | Sin usar.<br/>                                                                                               |
| <span id="TAG_CHECKSUM"></span><span id="tag_checksum"></span><dl> <dt>**TAG \_ CHECKSUM**</dt> <dt>(0x3 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                                     | Atributo de suma de comprobación de archivo.<br/>                                                                              |
| <span id="TAG_SHIM_TAGID"></span><span id="tag_shim_tagid"></span><dl> <dt>**TAG \_ SHIM \_ TAGID**</dt> <dt>(0X4 \| **TIPO DE \_ \_ ETIQUETA DWORD**)</dt> </dl>                              | Atributo **TAGID de** shim.<br/>                                                                             |
| <span id="TAG_PATCH_TAGID"></span><span id="tag_patch_tagid"></span><dl> <dt>**TAG \_ PATCH \_ TAGID**</dt> <dt>(0X5 \| **TIPO DE \_ ETIQUETA \_ DWORD**)</dt> </dl>                           | Atributo **TAGID de** revisión.<br/>                                                                            |
| <span id="TAG_MODULE_TYPE"></span><span id="tag_module_type"></span><dl> <dt>**TAG \_ MODULE \_ TYPE**</dt> <dt>(0X6 \| **TAG TYPE \_ \_ DWORD**)</dt> </dl>                           | Atributo de tipo de módulo.<br/>                                                                                |
| <span id="TAG_VERDATEHI"></span><span id="tag_verdatehi"></span><dl> <dt>**TAG \_ VERDATEHI**</dt> <dt>(TIPO 0x7 \| **ETIQUETA \_ \_ DWORD**)</dt> </dl>                                  | Parte de orden superior del atributo de fecha de la versión del archivo.<br/>                                                |
| <span id="TAG_VERDATELO"></span><span id="tag_verdatelo"></span><dl> <dt>**TAG \_ VERDATELO**</dt> <dt>(0X8 \| **TIPO \_ DE ETIQUETA \_ DWORD**)</dt> </dl>                                  | Parte de orden bajo del atributo de fecha de versión del archivo.<br/>                                                 |
| <span id="TAG_VERFILEOS"></span><span id="tag_verfileos"></span><dl> <dt>**TAG \_ VERFILEOS**</dt> <dt>(0X9 \| **TIPO \_ DE ETIQUETA \_ DWORD**)</dt> </dl>                                  | Atributo de versión del archivo de sistema operativo.<br/>                                                              |
| <span id="TAG_VERFILETYPE"></span><span id="tag_verfiletype"></span><dl> <dt>**TAG \_ VERFILETYPE**</dt> <dt>(TIPO 0xA \| **ETIQUETA \_ \_ DWORD**)</dt> </dl>                            | Atributo de tipo de archivo.<br/>                                                                                  |
| <span id="TAG_PE_CHECKSUM"></span><span id="tag_pe_checksum"></span><dl> <dt>**TAG \_ SUMA \_ DE COMPROBACIÓN DE PE**</dt> <dt>(0XB TIPO DE ETIQUETA \| **\_ \_ DWORD**)</dt> </dl>                           | Atributo de suma de comprobación de archivos PE.<br/>                                                                           |
| <span id="TAG_PREVOSMAJORVER"></span><span id="tag_prevosmajorver"></span><dl> <dt>**TAG \_ PREVOSMAJORVER**</dt> <dt>(0XC \| **TIPO \_ DE ETIQUETA \_ DWORD**)</dt> </dl>                   | Atributo de versión principal del sistema operativo.<br/>                                                             |
| <span id="TAG_PREVOSMINORVER"></span><span id="tag_prevosminorver"></span><dl> <dt>**TAG \_ PREVOSMINORVER**</dt> <dt>(0XD \| **TIPO \_ DE ETIQUETA \_ DWORD**)</dt> </dl>                   | Atributo de versión del sistema operativo secundaria.<br/>                                                             |
| <span id="TAG_PREVOSPLATFORMID"></span><span id="tag_prevosplatformid"></span><dl> <dt>**TAG \_ PREVOSPLATFORMID**</dt> <dt>(0XE \| **TIPO \_ DE ETIQUETA \_ DWORD**)</dt> </dl>             | Atributo de identificador de plataforma de sistema operativo.<br/>                                                       |
| <span id="TAG_PREVOSBUILDNO"></span><span id="tag_prevosbuildno"></span><dl> <dt>**TAG \_ PREVOSBUILDNO**</dt> <dt>(TIPO 0xF \| **ETIQUETA \_ \_ DWORD**)</dt> </dl>                      | Atributo de número de compilación del sistema operativo.<br/>                                                              |
| <span id="TAG_PROBLEMSEVERITY"></span><span id="tag_problemseverity"></span><dl> <dt>**TAG \_ PROBLEMSEVERITY**</dt> <dt>(0X10 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>               | Atributo Block de una entrada de Apphelp. Esto determina si la aplicación está bloqueada temporalmente o de forma temporal.<br/> |
| <span id="TAG_LANGID"></span><span id="tag_langid"></span><dl> <dt>**TAG \_ LANGID**</dt> <dt>(TIPO 0x11 \| **ETIQUETA \_ \_ DWORD**)</dt> </dl>                                          | Identificador de idioma de una entrada de Apphelp.<br/>                                                              |
| <span id="TAG_VER_LANGUAGE"></span><span id="tag_ver_language"></span><dl> <dt>**TAG \_ VER \_ LANGUAGE**</dt> <dt>(0X12 \| **TAG TYPE \_ \_ DWORD**)</dt> </dl>                       | Atributo de versión de lenguaje de un archivo.<br/>                                                                 |
| <span id="TAG_ENGINE"></span><span id="tag_engine"></span><dl> <dt>**TAG \_ ENGINE**</dt> <dt>(TIPO 0x14 \| **ETIQUETA \_ \_ DWORD**)</dt> </dl>                                          | Sin usar.<br/>                                                                                               |
| <span id="TAG_HTMLHELPID"></span><span id="tag_htmlhelpid"></span><dl> <dt>**TAG \_ HTMLHELPID**</dt> <dt>(TIPO 0x15 \| **ETIQUETA \_ \_ DWORD**)</dt> </dl>                              | Atributo de identificador de ayuda para una entrada de Apphelp.<br/>                                                       |
| <span id="TAG_INDEX_FLAGS"></span><span id="tag_index_flags"></span><dl> <dt>**TAG \_ INDEX \_ FLAGS**</dt> <dt>(0X16 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                          | Atributo Flags para una entrada de índice.<br/>                                                                   |
| <span id="TAG_FLAGS"></span><span id="tag_flags"></span><dl> <dt>**TAG \_ FLAGS**</dt> <dt>(0x17 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                                             | Atributo Flags para una entrada de Apphelp.<br/>                                                                 |
| <span id="TAG_DATA_VALUETYPE"></span><span id="tag_data_valuetype"></span><dl> <dt>**TAG \_ DATA \_ VALUETYPE**</dt> <dt>(TIPO 0x18 \| **\_ ETIQUETA \_ DWORD**)</dt> </dl>                 | Atributo de tipo de datos para una entrada de datos.<br/>                                                                 |
| <span id="TAG_DATA_DWORD"></span><span id="tag_data_dword"></span><dl> <dt>**TAG \_ DATA \_ DWORD**</dt> <dt>(0X19 \| **TIPO DE \_ ETIQUETA \_ DWORD**)</dt> </dl>                             | Atributo de valor **DWORD** para una entrada de datos.<br/>                                                           |
| <span id="TAG_LAYER_TAGID"></span><span id="tag_layer_tagid"></span><dl> <dt>**TAG \_ LAYER \_ TAGID**</dt> <dt>(0x1A \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                          | Atributo **TAGID de corrección de compatibilidad de** capa.<br/>                                                                       |
| <span id="TAG_MSI_TRANSFORM_TAGID"></span><span id="tag_msi_transform_tagid"></span><dl> <dt>**TAG \_ MSI \_ TRANSFORM \_ TAGID**</dt> <dt>(0X1B TIPO DE ETIQUETA \| **\_ \_ DWORD**)</dt> </dl> | Atributo **TAGID de transformación de** MSI.<br/>                                                                    |
| <span id="TAG_LINKER_VERSION"></span><span id="tag_linker_version"></span><dl> <dt>**TAG \_ VERSIÓN DEL \_ VINCULADOR**</dt> <dt>(0X1C \| **TIPO DE ETIQUETA \_ \_ DWORD**)</dt> </dl>                 | Atributo de versión del vinculador de un archivo.<br/>                                                                   |
| <span id="TAG_LINK_DATE"></span><span id="tag_link_date"></span><dl> <dt>**TAG \_ LINK \_ DATE**</dt> <dt>(0X1D \| **TAG TYPE \_ \_ DWORD**)</dt> </dl>                                | Atributo de fecha de vínculo de un archivo.<br/>                                                                        |
| <span id="TAG_UPTO_LINK_DATE"></span><span id="tag_upto_link_date"></span><dl> <dt>**TAG \_ UPTO \_ LINK \_ DATE (0X1E**</dt> TAG TYPE <dt> \| **\_ \_ DWORD**)</dt> </dl>                | Atributo de fecha de vínculo de un archivo. La coincidencia se realiza hasta e incluye esta fecha de vínculo.<br/>                   |
| <span id="TAG_OS_SERVICE_PACK"></span><span id="tag_os_service_pack"></span><dl> <dt>**TAG \_ SERVICE \_ PACK DEL \_ SISTEMA OPERATIVO**</dt> <dt>(0X1F TIPO DE ETIQUETA \| **\_ \_ DWORD**)</dt> </dl>             | Atributo service pack del sistema operativo para una entrada ejecutable.<br/>                                      |
| <span id="TAG_FLAG_TAGID"></span><span id="tag_flag_tagid"></span><dl> <dt>**TAG \_ FLAG \_ TAGID**</dt> <dt>(0x20 \| **TIPO DE \_ \_ ETIQUETA DWORD**)</dt> </dl>                             | Atributo **TAGID de** marcas.<br/>                                                                            |
| <span id="TAG_RUNTIME_PLATFORM"></span><span id="tag_runtime_platform"></span><dl> <dt>**TAG \_ RUNTIME \_ PLATFORM**</dt> <dt>(0X21 \| **TAG TYPE \_ \_ DWORD**)</dt> </dl>           | Atributo de plataforma en tiempo de ejecución de un archivo.<br/>                                                                |
| <span id="TAG_OS_SKU"></span><span id="tag_os_sku"></span><dl> <dt>**TAG \_ SKU DEL \_ SISTEMA OPERATIVO**</dt> <dt>(0x22 TIPO DE ETIQUETA \| **\_ \_ DWORD**)</dt> </dl>                                         | Atributo de SKU del sistema operativo para una entrada ejecutable.<br/>                                               |
| <span id="TAG_OS_PLATFORM"></span><span id="tag_os_platform"></span><dl> <dt>**TAG \_ PLATAFORMA DEL \_ SISTEMA OPERATIVO**</dt> <dt>(0X23 TIPO DE ETIQUETA \| **\_ \_ DWORD**)</dt> </dl>                          | Atributo de plataforma del sistema operativo.<br/>                                                                  |
| <span id="TAG_APP_NAME_RC_ID"></span><span id="tag_app_name_rc_id"></span><dl> <dt>**TAG \_ ID. \_ \_ RC DE NOMBRE \_ DE**</dt> <dt>APLICACIÓN (0x24 \| **TIPO DE \_ ETIQUETA \_ DWORD**)</dt> </dl>               | Atributo de identificador de recurso de nombre de aplicación para las entradas de Apphelp.<br/>                                   |
| <span id="TAG_VENDOR_NAME_RC_ID"></span><span id="tag_vendor_name_rc_id"></span><dl> <dt>**TAG \_ VENDOR \_ NAME \_ RC \_ ID**</dt> <dt>(0X25 TAG TYPE \| **\_ \_ DWORD**)</dt> </dl>      | Atributo de identificador de recurso de nombre de proveedor para las entradas de Apphelp.<br/>                                        |
| <span id="TAG_SUMMARY_MSG_RC_ID"></span><span id="tag_summary_msg_rc_id"></span><dl> <dt>**TAG \_ SUMMARY \_ MSG \_ RC \_ ID**</dt> <dt>(0X26 TAG TYPE \| **\_ \_ DWORD**)</dt> </dl>      | Atributo de identificador de recurso de mensaje de resumen para las entradas de Apphelp.<br/>                                    |
| <span id="TAG_VISTA_SKU"></span><span id="tag_vista_sku"></span><dl> <dt>**TAG \_ \_SKU de VISTA**</dt> <dt>(0x27 TIPO DE ETIQUETA \| **\_ \_ DWORD**)</dt> </dl>                                | Windows Atributo de SKU de Vista.<br/>                                                                          |
| <span id="TAG_DESCRIPTION_RC_ID"></span><span id="tag_description_rc_id"></span><dl> <dt>**TAG \_ DESCRIPTION \_ RC \_ ID**</dt> <dt>(0x28 TAG TYPE \| **\_ \_ DWORD**)</dt> </dl>       | Descripción del atributo de identificador de recurso para las entradas de Apphelp.<br/>                                        |
| <span id="TAG_PARAMETER1_RC_ID"></span><span id="tag_parameter1_rc_id"></span><dl> <dt>**TAG \_ PARAMETER1 \_ RC \_ ID**</dt> <dt>(0x29 TAG TYPE \| **\_ \_ DWORD**)</dt> </dl>          | Atributo de identificador de recurso Parameter1 para las entradas de Apphelp.<br/>                                         |
| <span id="TAG_TAGID"></span><span id="tag_tagid"></span><dl> <dt>**TAG \_ TAGID**</dt> <dt>(0X801 \| **TIPO DE ETIQUETA \_ \_ DWORD**)</dt> </dl>                                            | **Atributo TAGID.**<br/>                                                                                  |



La entrada siguiente es de tipo **TAG \_ TYPE \_ STRING** (0x8000).



| Constante o valor                                                                                                                                                                                                                                                            | Descripción                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------|
| <span id="TAG_STRINGTABLE_ITEM"></span><span id="tag_stringtable_item"></span><dl> <dt>**TAG \_ STRINGTABLE \_ ITEM**</dt> <dt>(0x801 \| **TAG TYPE \_ \_ STRING**)</dt> </dl> | Entrada de elemento de tabla de cadenas.<br/> |



Las siguientes entradas son de tipo **TAG \_ TYPE \_ NULL** (0x1000).



| Constante o valor                                                                                                                                                                                                                                                                            | Descripción                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span id="TAG_INCLUDE"></span><span id="tag_include"></span><dl> <dt>**TAG \_ INCLUDE**</dt> <dt>(0X1 \| **TAG \_ TYPE \_ NULL**)</dt> </dl>                                                 | Incluir entrada de lista.<br/>                           |
| <span id="TAG_GENERAL"></span><span id="tag_general"></span><dl> <dt>**TAG \_ GENERAL**</dt> <dt>(0X2 \| **TIPO \_ DE ETIQUETA \_ NULL**)</dt> </dl>                                                 | Entrada de shim de uso general.<br/>                   |
| <span id="TAG_MATCH_LOGIC_NOT"></span><span id="tag_match_logic_not"></span><dl> <dt>**TAG \_ MATCH \_ LOGIC \_ NOT**</dt> <dt>(0X3 TAG TYPE \| **\_ \_ NULL**)</dt> </dl>                       | NO de la entrada lógica correspondiente.<br/>                  |
| <span id="TAG_APPLY_ALL_SHIMS"></span><span id="tag_apply_all_shims"></span><dl> <dt>**TAG \_ APPLY \_ ALL \_ SHIMS**</dt> <dt>(0X4 TAG TYPE \| **\_ \_ NULL**)</dt> </dl>                       | Sin usar.<br/>                                       |
| <span id="TAG_USE_SERVICE_PACK_FILES"></span><span id="tag_use_service_pack_files"></span><dl> <dt>**TAG \_ USAR \_ ARCHIVOS DE SERVICE \_ \_ PACK**</dt> <dt>(0X5 TIPO DE ETIQUETA \| **\_ \_ NULL**)</dt> </dl> | Información de Service Pack para las entradas de Apphelp.<br/> |
| <span id="TAG_MITIGATION_OS"></span><span id="tag_mitigation_os"></span><dl> <dt>**TAG \_ SISTEMA \_ OPERATIVO DE MITIGACIÓN**</dt> <dt>(0x6 TIPO DE ETIQUETA \| **\_ \_ NULL**)</dt> </dl>                              | Mitigación en la entrada del ámbito del sistema operativo.<br/>   |
| <span id="TAG_BLOCK_UPGRADE"></span><span id="tag_block_upgrade"></span><dl> <dt>**TAG \_ ACTUALIZACIÓN \_ DE BLOQUES**</dt> <dt>(0X7 TIPO DE ETIQUETA \| **\_ \_ NULL**)</dt> </dl>                              | Actualizar entrada de bloque.<br/>                          |
| <span id="TAG_INCLUDEEXCLUDEDLL"></span><span id="tag_includeexcludedll"></span><dl> <dt>**TAG \_ INCLUDEEXCLUDEDLL**</dt> <dt>(0X8 \| **TAG \_ TYPE \_ NULL**)</dt> </dl>                   | Entrada include/exclude de DLL.<br/>                    |



Las siguientes entradas son de tipo **TAG \_ TYPE \_ QWORD** (0x5000).



| Constante o valor                                                                                                                                                                                                                                                                                   | Descripción                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TAG_TIME"></span><span id="tag_time"></span><dl> <dt>**TAG \_ TIME**</dt> <dt>(0X1 \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                                                                | Atributo time.<br/>                                                                                     |
| <span id="TAG_BIN_FILE_VERSION"></span><span id="tag_bin_file_version"></span><dl> <dt>**TAG \_ BIN \_ FILE \_ VERSION**</dt> <dt>(0X2 TAG TYPE \| **\_ \_ QWORD**)</dt> </dl>                          | Atributo bin file version para las entradas de archivo.<br/>                                                        |
| <span id="TAG_BIN_PRODUCT_VERSION"></span><span id="tag_bin_product_version"></span><dl> <dt>**TAG \_ BIN \_ PRODUCT \_ VERSION**</dt> <dt>(0X3 TAG TYPE \| **\_ \_ QWORD**)</dt> </dl>                 | Atributo bin product version para las entradas de archivo.<br/>                                                     |
| <span id="TAG_MODTIME"></span><span id="tag_modtime"></span><dl> <dt>**TAG \_ MODTIME**</dt> <dt>(TIPO 0x4 \| **ETIQUETA \_ \_ QWORD**)</dt> </dl>                                                       | Sin usar.<br/>                                                                                             |
| <span id="TAG_FLAG_MASK_KERNEL"></span><span id="tag_flag_mask_kernel"></span><dl> <dt>**TAG \_ KERNEL \_ DE MÁSCARA DE \_ MARCA**</dt> <dt>(0X5 TIPO DE ETIQUETA \| **\_ \_ QWORD**)</dt> </dl>                          | Atributo de máscara de marca de kernel.<br/>                                                                         |
| <span id="TAG_UPTO_BIN_PRODUCT_VERSION"></span><span id="tag_upto_bin_product_version"></span><dl> <dt>**TAG \_ UPTO \_ BIN \_ PRODUCT \_ VERSION**</dt> <dt>(0X6 TAG TYPE \| **\_ \_ QWORD**)</dt> </dl> | Atributo bin product version de un archivo. La coincidencia se realiza hasta e incluye esta versión del producto.<br/> |
| <span id="TAG_DATA_QWORD"></span><span id="tag_data_qword"></span><dl> <dt>**TAG \_ DATA \_ QWORD**</dt> <dt>(0X7 \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                                             | **Atributo de valor ULONGLONG** para una entrada de datos.<br/>                                                     |
| <span id="TAG_FLAG_MASK_USER"></span><span id="tag_flag_mask_user"></span><dl> <dt>**TAG \_ FLAG \_ MASK \_ USER**</dt> <dt>(0X8 TAG TYPE \| **\_ \_ QWORD**)</dt> </dl>                                | Atributo de máscara de marca de usuario.<br/>                                                                           |
| <span id="TAG_FLAGS_NTVDM1"></span><span id="tag_flags_ntvdm1"></span><dl> <dt>**TAG \_ FLAGS \_ NTVDM1**</dt> <dt>(0X9 \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                                       | Atributo de máscara de marca NTVDM1.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM2"></span><span id="tag_flags_ntvdm2"></span><dl> <dt>**TAG \_ FLAGS \_ NTVDM2**</dt> <dt>(0XA \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                                       | Atributo de máscara de marca NTVDM2.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM3"></span><span id="tag_flags_ntvdm3"></span><dl> <dt>**TAG \_ FLAGS \_ NTVDM3**</dt> <dt>(0XB \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                                       | Atributo de máscara de marca NTVDM3.<br/>                                                                         |
| <span id="TAG_FLAG_MASK_SHELL"></span><span id="tag_flag_mask_shell"></span><dl> <dt>**TAG \_ FLAG \_ MASK \_ SHELL**</dt> <dt>(0XC TAG TYPE \| **\_ \_ QWORD**)</dt> </dl>                             | Atributo de máscara de marca de shell.<br/>                                                                          |
| <span id="TAG_UPTO_BIN_FILE_VERSION"></span><span id="tag_upto_bin_file_version"></span><dl> <dt>**TAG \_ UPTO \_ BIN \_ FILE \_ VERSION**</dt> <dt>(0XD TAG TYPE \| **\_ \_ QWORD**)</dt> </dl>          | Atributo bin file version de un archivo. La coincidencia se realiza hasta e incluye esta versión de archivo.<br/>       |
| <span id="TAG_FLAG_MASK_FUSION"></span><span id="tag_flag_mask_fusion"></span><dl> <dt>**TAG \_ FLAG \_ MASK \_ FUSION**</dt> <dt>(0XE TAG TYPE \| **\_ \_ QWORD**)</dt> </dl>                          | Atributo de máscara de marca de fusión.<br/>                                                                         |
| <span id="TAG_FLAG_PROCESSPARAM"></span><span id="tag_flag_processparam"></span><dl> <dt>**TAG \_ FLAG \_ PROCESSPARAM**</dt> <dt>(0XF \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                        | Atributo de marca de param de proceso.<br/>                                                                       |
| <span id="TAG_FLAG_LUA"></span><span id="tag_flag_lua"></span><dl> <dt>**TAG \_ FLAG \_ LUA**</dt> <dt>(0X10 \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                                                  | Atributo de marca LUA.<br/>                                                                                 |
| <span id="TAG_FLAG_INSTALL"></span><span id="tag_flag_install"></span><dl> <dt>**TAG \_ FLAG \_ INSTALL**</dt> <dt>(0X11 \| **TAG TYPE \_ \_ QWORD**)</dt> </dl>                                      | Instale el atributo de marca.<br/>                                                                             |



Las siguientes entradas son de tipo **TAG \_ TYPE \_ BINARY** (0x9000).



| Constante o valor                                                                                                                                                                                                                                                     | Descripción                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="TAG_PATCH_BITS"></span><span id="tag_patch_bits"></span><dl> <dt>**TAG \_ PATCH \_ BITS**</dt> <dt>(0X2 TAG TYPE \| **\_ \_ BINARY**)</dt> </dl>              | Atributo de bits de archivo de revisión.<br/>                          |
| <span id="TAG_FILE_BITS"></span><span id="tag_file_bits"></span><dl> <dt>**TAG \_ BITS \_ DE ARCHIVO**</dt> <dt>(0X3 TIPO DE ETIQUETA \| **\_ \_ BINARY**)</dt> </dl>                 | Atributo de bits de archivo.<br/>                                |
| <span id="TAG_EXE_ID"></span><span id="tag_exe_id"></span><dl> <dt>**TAG \_ IDENTIFICADOR \_ DE EXE**</dt> <dt>(0X4 TIPO DE ETIQUETA \| **\_ \_ BINARY**)</dt> </dl>                          | **Atributo GUID** de una entrada ejecutable.<br/>          |
| <span id="TAG_DATA_BITS"></span><span id="tag_data_bits"></span><dl> <dt>**TAG \_ BITS \_ DE DATOS**</dt> <dt>(0X5 TIPO DE ETIQUETA \| **\_ \_ BINARY**)</dt> </dl>                 | Atributo de bits de datos.<br/>                                |
| <span id="TAG_MSI_PACKAGE_ID"></span><span id="tag_msi_package_id"></span><dl> <dt>**TAG \_ IDENTIFICADOR \_ DE PAQUETE \_ MSI**</dt> <dt>(0X6 TIPO DE ETIQUETA \| **\_ \_ BINARY**)</dt> </dl> | Atributo de identificador de paquete MSI de un paquete MSI.<br/> |
| <span id="TAG_DATABASE_ID"></span><span id="tag_database_id"></span><dl> <dt>**TAG \_ IDENTIFICADOR \_ DE BASE**</dt> DE DATOS <dt>(0X7 TIPO DE ETIQUETA \| **\_ \_ BINARY**)</dt> </dl>           | **Atributo GUID** de una base de datos.<br/>                   |
| <span id="TAG_INDEX_BITS"></span><span id="tag_index_bits"></span><dl> <dt>**TAG \_ BITS \_ DE ÍNDICE**</dt> <dt>(0X801 TIPO DE ETIQUETA \| **\_ \_ BINARY**)</dt> </dl>            | Atributo de bits de índice.<br/>                               |



Las siguientes entradas son de tipo **TAG \_ TYPE \_ WORD** (0x3000).



| Constante o valor                                                                                                                                                                                                                                      | Descripción                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="TAG_MATCH_MODE"></span><span id="tag_match_mode"></span><dl> <dt>**TAG \_ MATCH \_ MODE**</dt> <dt>(0X1 \| **TAG TYPE \_ \_ WORD**)</dt> </dl> | Atributo de modo de coincidencia.<br/>                   |
| <span id="TAG_TAG"></span><span id="tag_tag"></span><dl> <dt>**TAG \_ TAG**</dt> <dt>(0X801 \| **TAG \_ TYPE \_ WORD**)</dt> </dl>                     | Entrada TAG.<br/>                              |
| <span id="TAG_INDEX_TAG"></span><span id="tag_index_tag"></span><dl> <dt>**TAG \_ INDEX \_ TAG**</dt> <dt>(0X802 \| **TAG TYPE \_ \_ WORD**)</dt> </dl>  | Atributo INDEX TAG para una entrada de índice.<br/> |
| <span id="TAG_INDEX_KEY"></span><span id="tag_index_key"></span><dl> <dt>**TAG \_ INDEX \_ KEY**</dt> <dt>(0X803 \| **TAG TYPE \_ \_ WORD**)</dt> </dl>  | Atributo de clave de índice para una entrada de índice.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Exposeenums2managed.h (incluye Axextendenums.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos TAG](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




