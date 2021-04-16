---
description: En este tema se describen los elementos que Windows Search indexa.
ms.assetid: vs|search|~\search\wds3x\overviews\misc_items_in_index.htm
title: Qué se incluye en el índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5560a14e3537c8e3ac8c7544aa7ffc9a0bc1bc64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705499"
---
# <a name="what-is-included-in-the-index"></a>Qué se incluye en el índice

En este tema se describen los elementos que Windows Search indexa.

Este tema se organiza de la siguiente manera:

-   [Indexado de forma predeterminada](#indexed-by-default)
-   [Formatos de archivo admitidos](#file-formats-supported)
-   [Exclusiones de archivos](#file-exclusions)
-   [Exclusiones de carpetas](#folder-exclusions)
-   [Exclusiones de unidad](#drive-exclusions)
-   [Temas relacionados](#related-topics)

 

## <a name="indexed-by-default"></a>Indexado de forma predeterminada

Los filtros y controladores de protocolo se incluyen en Windows Search para indexar los siguientes tipos de contenido:

-   En Windows Vista y versiones posteriores, los elementos de correo de Microsoft Outlook y Microsoft Outlook Express de un usuario se indexan mientras se ejecuta la aplicación de correo.
-   Los archivos sin conexión en la memoria caché del lado cliente (CSC) los indexa Windows Search de forma local.
-   Windows Search admite la recopilación de direcciones de inicio de archivo en volúmenes NTFS y FAT32. NTFS admite la indexación basada en notificaciones y FAT32 admite un rastreo incremental al iniciarse y, a continuación, responde a las notificaciones.
-   Windows Vista y versiones posteriores continúan exponiendo una propiedad por carpeta/archivo para habilitar la indización: la opción "**para búsqueda rápida, permitir el servicio de indización para indizar esta carpeta**" del cuadro de diálogo de **propiedades** . Al establecer la marca de bits FANCI se garantiza que las propiedades básicas del Protocolo, como URL, nombre de archivo y tamaño, se indizan, pero no se ejecutan controladores de filtro ni controladores de propiedades.
-   El contenido de texto está indexado, pero no la puntuación.

## <a name="file-formats-supported"></a>Formatos de archivo admitidos

Windows Search tiene controladores de protocolo, controladores de propiedades y controladores de filtro para indizar los formatos siguientes automáticamente:

-   Archivos multimedia: todos los tipos de archivos multimedia
-   **HTML** (nlhtml.dll):. ascx,. asp,. aspx,. CSS,. HHC,. htm,. html,. htt,. HTW,. htx,. odc y. stm
-   **MIME HTML** (mimefilt.dll):. mht,. MHTML
-   **Office** (offfilt.dll):. doc,. dot,. pot,. PPS,. ppt,. XLB,. XLC,. xls,. xlt
-   **Texto** (query.dll):. ASM,. ASX,. bat,. c,. cmd,. cpp,. CXX,. def,. dic,. h,. HPP,. HXX,. idl,. idq,. inf,. ini,. INX,. js,. log,. m3u,. rc,. reg,. rtf,. txt,. URL,. vbs,. WTX
-   **XML** (xmlfilt.dll):. XML,. xsl
-   **OneNote**:. One
-   **Tablet Journal** (jntfiltr.dll):. JNT

Las propiedades se indizan para todos los archivos excepto el almacenamiento estructurado. En Windows Vista y versiones posteriores, se indizan muchas propiedades de archivo multimedia. sin embargo, el contenido no se indexa si los archivos están protegidos por la administración de derechos digitales (DRM).

> [!Note]  
> El filtro HTML no indiza los comentarios HTML.

 

## <a name="file-exclusions"></a>Exclusiones de archivos

Cuando un tipo de archivo no tiene un filtro asociado, o cuando un archivo no tiene una extensión, las propiedades del sistema para los archivos de ese tipo se indizan, pero el contenido del archivo no está indizado.

Además, Windows Search no indiza el contenido de los archivos en Information Rights Management (IRM) o administración de derechos digitales (DRM).

En Windows Vista (solo), los siguientes archivos se excluyen de la indexación de forma predeterminada:

-   Archivos marcados como ocultos o sistema.
-   Archivos con las siguientes extensiones:

    .386,. APS,. CD de audio,. bin,. BK1,. BK2,. bkf,. BSC,. BTR,. chk,. CI,. crwl,. dbg,. DCT,. DeskLink,. dir,. DL \_ ,. dll,. drv,. DVD,. evt,. ex \_ ,. exe,. exp,. Eyb,. FND,. FNT,. Folder,. fon,. ghi,. gthr,. hqx,. ICM,. IDB,. idx,. ILK,. IMC,. in \_ ,. ini,. INV,. JBF,. latex,. lib,. local,. M14,. Mac,. manifest,. map,. MAPIMail,. MMF,. Movie,. mv,. mis documentos,. NCB,. obj,. OC \_ ,. ocx,. PCH,. pdb,. PF,. PMA,. PMC,. PML,. PMR,. res,. RMP,. RPC,. RSP,. SBR,. SC2,. Sit,. Sr \_ ,. SY \_ ,. sym,. sys,. tlb,. TRC,. TTC,. ttf,. VBX,. vxd,. WLL,. WLT,. XIX,. Z96,. ZFSendToTarget.

## <a name="folder-exclusions"></a>Exclusiones de carpetas

> [!TIP]
> Los nombres de carpeta no distinguen mayúsculas de minúsculas.

 

Las siguientes carpetas se excluyen de la indexación de forma predeterminada:



| Patrón de exclusión de carpetas                                                              | Efecto en Windows 7 | Efecto en Windows Vista | Descripción                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------|---------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *% Del sistema* \\ ProgramData \\ datos de Microsoft \\ Search \\\\                                    | **Excluded**        | Sin efecto               | Datos del indexador en la unidad del sistema.                                                                                                                                                                                          |
| *% Del sistema* \\ \\*Nombre de usuario* \\ AppData\\                                              | **Excluded**        | Sin efecto               | Datos de la aplicación del usuario (incluye datos temporales) en la unidad del sistema.<br/> Para cada usuario que inicia sesión en el sistema, se agrega un patrón de exclusión específico que excluye los datos de la aplicación del índice.<br/> |
| *% Del sistema* \\ Usuarios \\ \* \\ AppData \\ locales \\ \\ \\ archivos temporales de Microsoft Windows\\ | **Excluded**        | Sin efecto               | Ubicación predeterminada de los archivos temporales de Internet de Windows Internet Explorer en la unidad del sistema.<br/> Si se cambia la ubicación de los archivos temporales de Internet Explorer, es posible que se hayan indizado los archivos.<br/>    |
| *% Del sistema* \\ CSC de Windows \\\\                                                            | **Excluded**        | Sin efecto               | Si la indización está activada para el directorio del sistema de Windows, la carpeta CSC (en la unidad del sistema) todavía se excluye de la indización.                                                                                           |
| *% Del sistema* \\ Temp de Windows \\ \* \\\\                                                       | **Excluded**        | Sin efecto               | Datos temporales de Windows en la unidad del sistema.                                                                                                                                                                                     |
| *% Del sistema* \\ Windows.\*\\                                                              | **Excluded**        | Sin efecto               | Instalaciones anteriores de Windows en la unidad del sistema.                                                                                                                                                                             |
| *% Del sistema* \\ ProgramData\\                                                             | **Excluded**        | **Excluded**            | Tenga en cuenta que la subcarpeta del menú Inicio compartido está indizada.                                                                                                                                                                     |
| *% Del sistema* \\ Usuarios \\ \* \\ AppData\\                                                      | **Excluded**        | **Excluded**            | Datos de la aplicación de los usuarios (incluye datos temporales).                                                                                                                                                                              |
| *% Del sistema* \\ Usuarios \\ \* \\ AppData \\ locales \\ Temp\\                                         | **Excluded**        | **Excluded**            | Datos temporales de los usuarios. Si la indexación está activada para los datos de la aplicación de usuario, los datos temporales del usuario todavía se excluyen de la indexación de forma predeterminada.                                                                                           |
| *% Del sistema* \\ Windows\\                                                                 | **Excluded**        | **Excluded**            | Archivos del sistema operativo en la unidad del sistema.                                                                                                                                                                                |
| *% Del sistema* \\ $Recycle Bin\\                                                            | **Excluded**        | **Excluded**            | Ubicación de los archivos en la papelera de reciclaje.                                                                                                                                                                                      |
| *% Del sistema* \\ Versión\\                                                                   | Sin efecto           | **Excluded**            | En la unidad del sistema.                                                                                                                                                                                                       |
| *% Del sistema* \\ Repositorio instalado\\                                                    | Sin efecto           | **Excluded**            | En la unidad del sistema.                                                                                                                                                                                                       |
| *% Del sistema* \\ Archivos de programa\\                                                           | Sin efecto           | **Excluded**            | En la unidad del sistema.                                                                                                                                                                                                       |
| *% Del sistema* \\ Archivos de programa (x86)\\                                                     | Sin efecto           | **Excluded**            | En la unidad del sistema.                                                                                                                                                                                                       |
| \*\\Temperatura\\\*                                                                          | Sin efecto           | **Excluded**            | Datos temporales de Windows y otras carpetas con el nombre "Temp".                                                                                                                                                                  |
| *% Del sistema* \\ Usuarios \\ predeterminados\\                                                          | Sin efecto           | **Excluded**            | La ubicación de los datos de Perfil de usuario predeterminados en la unidad del sistema.                                                                                                                                                             |
| \*\\Windows.\*\\                                                                      | Sin efecto           | **Excluded**            | Instalaciones anteriores de Windows y otras carpetas con nombres que comienzan por "Windows".                                                                                                                                         |



 

## <a name="drive-exclusions"></a>Exclusiones de unidad

En Windows 7 y Windows Vista, las unidades extraíbles no se indexan de forma predeterminada.

> [!Note]  
> Si las unidades extraíbles se informan como unidades fijas, puede agregarlas para indizarlas aunque realmente sean extraíbles. La información permanecerá en el índice y Windows Search realizará un rastreo incremental para conciliar los resultados de la indexación cuando el disco extraíble vuelva a conectarse. Dado que las unidades flash USB se informan como extraíbles, no se pueden indexar.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Indexación, consulta y notificaciones en Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Proceso de indexación en Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Consulta del proceso en Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Proceso de notificaciones en Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[Requisitos de formato de dirección URL](url-formatting-requirements.md)
</dt> </dl>

 

 




