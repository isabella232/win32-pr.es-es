---
description: En este tema se describen los elementos que Windows buscar índices.
ms.assetid: vs|search|~\search\wds3x\overviews\misc_items_in_index.htm
title: Qué se incluye en el índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbffec8aba8a985faca112eac434b669d22eff82d94d6b4eaf5588585ced771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463328"
---
# <a name="what-is-included-in-the-index"></a>Qué se incluye en el índice

En este tema se describen los elementos que Windows buscar índices.

Este tema se organiza de la siguiente manera:

-   [Indexado de forma predeterminada](#indexed-by-default)
-   [Formatos de archivo admitidos](#file-formats-supported)
-   [Exclusiones de archivos](#file-exclusions)
-   [Exclusiones de carpetas](#folder-exclusions)
-   [Exclusiones de unidad](#drive-exclusions)
-   [Temas relacionados](#related-topics)

 

## <a name="indexed-by-default"></a>Indexado de forma predeterminada

Los controladores y filtros de protocolo se incluyen en Windows Search para indexar los siguientes tipos de contenido:

-   En Windows Vista y versiones posteriores, los elementos de correo electrónico de Microsoft Outlook y Microsoft Outlook Express de un usuario se indexa mientras se ejecuta la aplicación de correo.
-   Los archivos sin conexión de la caché del lado cliente (CSC) se indexa Windows buscar localmente.
-   Windows La búsqueda admite la recopilación de direcciones de inicio de archivos en volúmenes NTFS y FAT32. NTFS admite la indexación basada en notificaciones y FAT32 admite un rastreo incremental al iniciarse y, a continuación, responde a las notificaciones.
-   Windows Vista y versiones posteriores siguen expondndo una propiedad por carpeta o por archivo para habilitar la indexación:  la opción "Para búsquedas rápidas, lo que permite que **Indexing Service** indexe esta carpeta" en el cuadro de diálogo Propiedad . Al establecer la marca de bits FANCI se garantiza que las propiedades básicas del protocolo, como la dirección URL, el nombre de archivo y el tamaño, estén indexadas, pero que no se ejecuten controladores de filtro ni controladores de propiedades.
-   El contenido de texto está indexado, pero la puntuación no.

## <a name="file-formats-supported"></a>Formatos de archivo admitidos

Windows La búsqueda tiene controladores de protocolo, controladores de propiedades y controladores de filtro para indexar automáticamente los siguientes formatos:

-   Archivos multimedia: todos los tipos de archivo multimedia
-   **HTML** (nlhtml.dll): .ascx, .asp, .aspx, .css, .hhc, .htm, .html, .htt, .htw, .htx, .odc, .stm
-   **MIME HTML** (mimefilt.dll): .mht, .mhtml
-   **Office** (offfilt.dll): .doc, .dot, .pot, .pps, .ppt, .xlb, .xlc, .xls, .xlt
-   **Text** (query.dll): .asm, .asx, .bat, .c, .cmd, .cpp, .cxx, .def, .dic, .h, .hpp, .hxx, .idl, .idq, .inf, .ini, .inx, .js, .log, .m3u, .rc, .reg, .rtf, .txt, .url, .vbs, .wtx
-   **XML** (xmlfilt.dll): .xml, .xsl
-   **OneNote:**.one
-   **Diario de tabletas** (jntfiltr.dll): .jnt

Las propiedades se indexa para todos los archivos, excepto el almacenamiento estructurado. En Windows Vista y versiones posteriores, se indexa muchas propiedades de archivo multimedia; sin embargo, el contenido no se indexa si los archivos están protegidos por administración de derechos digitales (DRM).

> [!Note]  
> El filtro HTML no indexa los comentarios HTML.

 

## <a name="file-exclusions"></a>Exclusiones de archivos

Cuando un tipo de archivo no tiene un filtro asociado o cuando un archivo no tiene una extensión, las propiedades del sistema de los archivos de ese tipo se indexa, pero el contenido del archivo no se indexa.

Además, Windows Search no indexa el contenido de los archivos en Information Rights Management (IRM) o administración de derechos digitales (DRM).

En Windows Vista (solo), los siguientes archivos se excluyen de la indexación de forma predeterminada:

-   Archivos marcados como Oculto o Sistema.
-   Archivos con las siguientes extensiones:

    .386, .aps, . AudioCD, .bin, .bk1, .bk2, .bkf, .bsc, .btr, .chk, .ci, .crwl, .dbg, .dct, . DeskLink, .dir, .dl \_ , .dll, .drv, .dvd, .evt, .ex \_ , .exe, .exp, .eyb, .fnd, .fnt, . Folder, .fon, .ghi, .gthr, .hqx, .icm, .idb, .idx, .ilk, .imc, .in \_ , .ini, .inv, .jbf, .latex, .lib, .local, .m14, .mac, .manifest, .map, . MAPIMail, .mmf, .movie, .mv, .mydocs, .ncb, .obj, \_ .oc, .ocx, .pch, .pdb, .pf, .pma, .pmc, .pml, .pmr, .res, .rmp, .rpc, .rsp, .sbr, .sc2, .sit, .sr \_ , \_ .sy , .sym, .sys, .tlb, .trc, .ttc, .ttf, .vbx, .vxd, .wll, .wlt, .6, . ASÍNsendToTarget.

## <a name="folder-exclusions"></a>Exclusiones de carpetas

> [!TIP]
> Los nombres de carpeta no distinguen mayúsculas de minúsculas.

 

Las siguientes carpetas se excluyen de la indexación de forma predeterminada:



| Patrón de exclusión de carpetas                                                              | Efecto en Windows 7 | Efecto en Windows Vista | Descripción                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------|---------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *%System%* \\ ProgramData \\ Microsoft \\ Search \\ Data\\                                    | **Excluded**        | Sin efecto               | Datos del indexador en la unidad del sistema.                                                                                                                                                                                          |
| *%System%* \\ Users \\ *UserName* \\ AppData\\                                              | **Excluded**        | Sin efecto               | Datos de aplicación del usuario (incluye datos temporales) en la unidad del sistema.<br/> Para cada usuario que inicia sesión en el sistema, se agrega un patrón de exclusión específico que excluye los datos de la aplicación del índice.<br/> |
| *%System%* \\ Usuarios \\ \* \\ AppData \\ Local Microsoft Windows archivos temporales de \\ \\ \\ Internet\\ | **Excluded**        | Sin efecto               | Ubicación predeterminada de Windows Internet Explorer archivos temporales de Internet en la unidad del sistema.<br/> Si se cambia la ubicación Internet Explorer archivos temporales de Internet, esos archivos se pueden indexar.<br/>    |
| *%System%* \\ \\Windows Csc\\                                                            | **Excluded**        | Sin efecto               | Si la indexación está activada para el Windows del sistema, la carpeta CSC (en la unidad del sistema) todavía se excluye de la indexación.                                                                                           |
| *%System%* \\ \\ \* Windows \\ Temp\\                                                       | **Excluded**        | Sin efecto               | Windows datos temporales en la unidad del sistema.                                                                                                                                                                                     |
| *%System%* \\ Windows.\*\\                                                              | **Excluded**        | Sin efecto               | Instalaciones Windows en la unidad del sistema.                                                                                                                                                                             |
| *%System%* \\ ProgramData\\                                                             | **Excluded**        | **Excluded**            | Tenga en cuenta que la subapartada menú Inicio compartida está indexada.                                                                                                                                                                     |
| *%System%* \\ Usuarios \\ \* \\ AppData\\                                                      | **Excluded**        | **Excluded**            | Datos de aplicación de los usuarios (incluye datos temporales).                                                                                                                                                                              |
| *%System%* \\ Usuarios \\ \* \\ AppData \\ Local \\ Temp\\                                         | **Excluded**        | **Excluded**            | Datos temporales de los usuarios. Si la indexación está activada para los datos de la aplicación de usuario, los datos temporales de usuario todavía se excluyen de la indexación de forma predeterminada.                                                                                           |
| *%System%* \\ Windows\\                                                                 | **Excluded**        | **Excluded**            | Archivos de sistema operativo en la unidad del sistema.                                                                                                                                                                                |
| *%System%* \\ $papelera de reciclaje\\                                                            | **Excluded**        | **Excluded**            | Ubicación de los archivos en el papelera de reciclaje.                                                                                                                                                                                      |
| *%System%* \\ Construir\\                                                                   | Sin efecto           | **Excluded**            | En la unidad del sistema.                                                                                                                                                                                                       |
| *%System%* \\ Repositorio instalado\\                                                    | Sin efecto           | **Excluded**            | En la unidad del sistema.                                                                                                                                                                                                       |
| *%System%* \\ Archivos de programa\\                                                           | Sin efecto           | **Excluded**            | En la unidad del sistema.                                                                                                                                                                                                       |
| *%System%* \\ Archivos de programa (x86)\\                                                     | Sin efecto           | **Excluded**            | En la unidad del sistema.                                                                                                                                                                                                       |
| \*\\Temp\\\*                                                                          | Sin efecto           | **Excluded**            | Windows datos temporales y otras carpetas con el nombre "temp".                                                                                                                                                                  |
| *%System%* \\ Usuarios \\ predeterminados\\                                                          | Sin efecto           | **Excluded**            | Ubicación de los datos predeterminados del perfil de usuario en la unidad del sistema.                                                                                                                                                             |
| \*\\Windows.\*\\                                                                      | Sin efecto           | **Excluded**            | Las Windows y otras carpetas con nombres que comienzan por "windows".                                                                                                                                         |



 

## <a name="drive-exclusions"></a>Exclusiones de unidad

En Windows 7 y Windows Vista, las unidades extraíbles no se indexa de forma predeterminada.

> [!Note]  
> Si las unidades extraíbles se informan como unidades fijas, puede agregarlas para que se indexen incluso si realmente son extraíbles. La información permanecerá en el índice y Windows Search realizará un rastreo incremental para conciliar los resultados de la indexación cuando el disco extraíble vuelva a conectarse. Dado que las unidades flash USB se informan a sí mismas como extraíbles, no se pueden indexar.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Indexación, consulta y notificaciones en Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Proceso de indexación en Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Proceso de consulta en Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Proceso de notificaciones en Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[Requisitos de formato de dirección URL](url-formatting-requirements.md)
</dt> </dl>

 

 




