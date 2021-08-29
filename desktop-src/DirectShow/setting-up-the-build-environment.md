---
description: Creación de DirectShow aplicaciones
ms.assetid: 2fbdbe49-0d4d-4dce-afc3-7049c793ace0
title: Creación de DirectShow aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e6c062c97d64373668ef8bfd7eaf02b5d514bd648c3bc5b67ac6803d1fd804f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951904"
---
# <a name="building-directshow-applications"></a>Creación de DirectShow aplicaciones

En este tema se describen los encabezados y bibliotecas necesarios para compilar DirectShow aplicaciones.

Los encabezados DirectShow bibliotecas más recientes están disponibles en [el SDK Windows](https://msdn.microsoft.com/windows/aa904949.aspx).

## <a name="header-files"></a>Archivos de encabezado

Todas DirectShow aplicaciones usan el archivo de encabezado que se muestra en la tabla siguiente.



| Archivo de encabezado | Requerido para                 |
|-------------|------------------------------|
| Dshow.h     | Todas DirectShow aplicaciones. |



 

Algunas DirectShow interfaces requieren archivos de encabezado adicionales. Estos requisitos se anotan en la referencia de interfaz.

## <a name="library-files"></a>Archivos de biblioteca

DirectShow usa los archivos de biblioteca estática que se muestran en la tabla siguiente.



| Archivo de biblioteca | Descripción                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| Strmiids.lib | Exporta los identificadores de clase (CLID) y los identificadores de interfaz (IID).                                                           |
| Estorba.lib   | Exporta la [**función AMGetErrorText.**](/windows/win32/api/errors/nf-errors-amgeterrortexta) Si no llama a esta función, esta biblioteca no es necesaria. |



 

Use los mismos archivos .lib para las compilaciones de depuración y versión.

## <a name="filter-base-classes"></a>Filtrar clases base

El SDK Windows proporciona un conjunto de clases de C++ que se recomiendan si está escribiendo un filtro DirectShow personalizado. Estas clases se proporcionan como código de ejemplo, que puede compilar en una biblioteca estática. Para obtener más información, [vea DirectShow clases base](directshow-base-classes.md).

## <a name="redistributable-dlls"></a>Archivos DLL redistribuibles

DirectShow las aplicaciones escritas para Windows XP con Service Pack 2 (SP2) y versiones posteriores no necesitan redistribuir ningún archivo DLL DirectShow datos.

Para Windows XP con Service Pack 1 (SP1) y versiones anteriores, los archivos DLL DirectShow redistribuibles están disponibles en el SDK de Microsoft DirectX. La versión más reciente de estos archivos DLL es la versión 9.0c. No se planea ningún desarrollo adicional de estos archivos DLL redistribuibles. Windows XP con Service Pack 2 (SP2) contiene los archivos DLL de la versión 9.0c.

Los paquetes reds atribuibles contienen los siguientes archivos DLL:

-   dxnt.cab
    -   amstream.dll
    -   devenum.dll
    -   encapi.dll
    -   ks.sys
    -   ksolay.ax
    -   ksproxy.ax
    -   ksuser.dll
    -   l3codecx.ax
    -   mciqtz32.dll
    -   mpg2splt.ax
    -   msdmo.dll
    -   mskssrv.sys
    -   mspclock.sys
    -   mspqm.sys
    -   mstee.sys
    -   mswebdvd.dll
    -   qasf.dll
    -   qcap.dll
    -   qdv.dll
    -   qdvd.dll
    -   qedit.dll
    -   qedwipes.dll
    -   quartz.dll
    -   stream.sys
    -   swenum.sys
-   bda.cab
    -   bdaplgin.ax
    -   bdasup.sys
    -   ccdecode.sys
    -   ipsink.ax
    -   kstvtune.ax
    -   kswdmcap.ax
    -   ksxbar.ax
    -   mpe.sys
    -   mpeg2data.ax
    -   msdv.sys
    -   msdvbnp.ax
    -   msvidctl.dll
    -   msyuv.dll
    -   nabtsfec.sys
    -   ndisip.sys
    -   psisdecd.dll
    -   psisrndr.ax
    -   slip.sys
    -   streamip.sys
    -   vbisurf.ax
    -   wstcodec.sys
    -   wstdecod.dll

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de DirectShow filtros](building-directshow-filters.md)
</dt> </dl>

 

 
