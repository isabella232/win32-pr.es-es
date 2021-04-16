---
title: Tipos de recursos (Winuser. h)
description: A continuación se muestran los tipos de recursos predefinidos.
ms.assetid: 8d27f79a-8165-4565-a975-f25b2344efdc
topic_type:
- apiref
api_name:
- RT_ACCELERATOR
- RT_ANICURSOR
- RT_ANIICON
- RT_BITMAP
- RT_CURSOR
- RT_DIALOG
- RT_DLGINCLUDE
- RT_FONT
- RT_FONTDIR
- RT_GROUP_CURSOR
- RT_GROUP_ICON
- RT_HTML
- RT_ICON
- RT_MANIFEST
- RT_MENU
- RT_MESSAGETABLE
- RT_PLUGPLAY
- RT_RCDATA
- RT_STRING
- RT_VERSION
- RT_VXD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595f1d459f645d26014a644d0e2b7cb608f4c6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709171"
---
# <a name="resource-types"></a>Tipos de recursos

A continuación se muestran los tipos de recursos predefinidos.



| Constante o valor                                                                                                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RT_ACCELERATOR"></span><span id="rt_accelerator"></span><dl> <dt>**RT \_ ACELERAdor**</dt> <dt>MAKEINTRESOURCE (9)</dt> </dl>                                 | Tabla de aceleradores.<br/>                                                                                                                                                                                                                                                                    |
| <span id="RT_ANICURSOR"></span><span id="rt_anicursor"></span><dl> <dt>**RT \_ ANICURSOR**</dt> <dt>MAKEINTRESOURCE (21)</dt> </dl>                                      | Cursor animado.<br/>                                                                                                                                                                                                                                                                      |
| <span id="RT_ANIICON"></span><span id="rt_aniicon"></span><dl> <dt>**RT \_ ANIICON**</dt> <dt>MAKEINTRESOURCE (22)</dt> </dl>                                            | Icono animado.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_BITMAP"></span><span id="rt_bitmap"></span><dl> <dt>**RT \_ MAPA de bits**</dt> <dt>MAKEINTRESOURCE (2)</dt> </dl>                                                | Recurso de mapa de bits.<br/>                                                                                                                                                                                                                                                                      |
| <span id="RT_CURSOR"></span><span id="rt_cursor"></span><dl> <dt>**RT \_ CURSOR**</dt> <dt>MAKEINTRESOURCE (1)</dt> </dl>                                                | Recurso de cursor dependiente del hardware.<br/>                                                                                                                                                                                                                                                   |
| <span id="RT_DIALOG"></span><span id="rt_dialog"></span><dl> <dt>**RT \_ Cuadro de diálogo**</dt> <dt>MAKEINTRESOURCE (5)</dt> </dl>                                                | Cuadro de diálogo.<br/>                                                                                                                                                                                                                                                                           |
| <span id="RT_DLGINCLUDE"></span><span id="rt_dlginclude"></span><dl> <dt>**RT \_ DLGINCLUDE**</dt> <dt>MAKEINTRESOURCE (17)</dt> </dl>                                   | Permite a una herramienta de edición de recursos asociar una cadena a un archivo. rc. Normalmente, la cadena es el nombre del archivo de encabezado que proporciona nombres simbólicos. El compilador de recursos analiza la cadena pero, de lo contrario, omite el valor. Por ejemplo, <br/> `1 DLGINCLUDE "MyFile.h"`<br/> |
| <span id="RT_FONT"></span><span id="rt_font"></span><dl> <dt>**RT \_ FONT**</dt> <dt>MAKEINTRESOURCE (8)</dt> </dl>                                                      | Recurso de fuente.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_FONTDIR"></span><span id="rt_fontdir"></span><dl> <dt>**RT \_ FONTDIR**</dt> <dt>MAKEINTRESOURCE (7)</dt> </dl>                                             | Recurso de directorio de fuentes.<br/>                                                                                                                                                                                                                                                              |
| <span id="RT_GROUP_CURSOR"></span><span id="rt_group_cursor"></span><dl> <dt>**RT \_ \_Cursor de grupo**</dt> <dt>MAKEINTRESOURCE ((ulong \_ ) (cursor RT \_ ) + 11)</dt> </dl> | Recurso de cursor independiente del hardware.<br/>                                                                                                                                                                                                                                                 |
| <span id="RT_GROUP_ICON"></span><span id="rt_group_icon"></span><dl> <dt>**RT \_ \_Icono de grupo**</dt> <dt>MAKEINTRESOURCE ((ulong \_ ptr) ( \_ icono RT) + 11)</dt> </dl>         | Recurso de icono independiente del hardware.<br/>                                                                                                                                                                                                                                                   |
| <span id="RT_HTML"></span><span id="rt_html"></span><dl> <dt>**RT \_ MAKEINTRESOURCE HTML**</dt> <dt>(23)</dt> </dl>                                                     | Recurso HTML.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_ICON"></span><span id="rt_icon"></span><dl> <dt>**RT \_ ICONO**</dt> <dt>MAKEINTRESOURCE (3)</dt> </dl>                                                      | Recurso de icono dependiente del hardware.<br/>                                                                                                                                                                                                                                                     |
| <span id="RT_MANIFEST"></span><span id="rt_manifest"></span><dl> <dt>**RT \_ MANIFIESTO**</dt> <dt>MAKEINTRESOURCE (24)</dt> </dl>                                         | Manifiesto de ensamblado en paralelo.<br/>                                                                                                                                                                                                                                                       |
| <span id="RT_MENU"></span><span id="rt_menu"></span><dl> <dt>**RT \_ MENÚ**</dt> <dt>MAKEINTRESOURCE (4)</dt> </dl>                                                      | Recurso de menú.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_MESSAGETABLE"></span><span id="rt_messagetable"></span><dl> <dt>**RT \_ MESSAGETABLE**</dt> <dt>MAKEINTRESOURCE (11)</dt> </dl>                             | Entrada de tabla de mensajes.<br/>                                                                                                                                                                                                                                                                  |
| <span id="RT_PLUGPLAY"></span><span id="rt_plugplay"></span><dl> <dt>**RT \_ PLUGPLAY**</dt> <dt>MAKEINTRESOURCE (19)</dt> </dl>                                         | Plug and Play recurso.<br/>                                                                                                                                                                                                                                                               |
| <span id="RT_RCDATA"></span><span id="rt_rcdata"></span><dl> <dt>**RT \_ RCDATA**</dt> <dt>MAKEINTRESOURCE (10)</dt> </dl>                                               | Recurso definido por la aplicación (datos sin procesar).<br/>                                                                                                                                                                                                                                              |
| <span id="RT_STRING"></span><span id="rt_string"></span><dl> <dt>**RT \_ STRING**</dt> <dt>MAKEINTRESOURCE (6)</dt> </dl>                                                | Entrada de tabla de cadena.<br/>                                                                                                                                                                                                                                                                   |
| <span id="RT_VERSION"></span><span id="rt_version"></span><dl> <dt>**RT \_ VERSIÓN**</dt> <dt>MAKEINTRESOURCE (16)</dt> </dl>                                            | Recurso de versión.<br/>                                                                                                                                                                                                                                                                     |
| <span id="RT_VXD"></span><span id="rt_vxd"></span><dl> <dt>**RT \_ VXD**</dt> <dt>MAKEINTRESOURCE (20)</dt> </dl>                                                        | VXD.<br/>                                                                                                                                                                                                                                                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

 





