---
description: Compilar aplicaciones de DirectShow
ms.assetid: 2fbdbe49-0d4d-4dce-afc3-7049c793ace0
title: Compilar aplicaciones de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c6ab8a0731e93eece734abd4380b092414ff5f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677027"
---
# <a name="building-directshow-applications"></a>Compilar aplicaciones de DirectShow

En este tema se describen los encabezados y las bibliotecas necesarios para compilar aplicaciones de DirectShow.

Los encabezados y las bibliotecas de DirectShow más recientes están disponibles en el [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx).

## <a name="header-files"></a>Archivos de encabezado

Todas las aplicaciones de DirectShow usan el archivo de encabezado que se muestra en la tabla siguiente.



| Archivo de encabezado | Necesario para                 |
|-------------|------------------------------|
| DShow. h     | Todas las aplicaciones de DirectShow. |



 

Algunas interfaces de DirectShow requieren archivos de encabezado adicionales. Estos requisitos se indican en la referencia de la interfaz.

## <a name="library-files"></a>Archivos de biblioteca

DirectShow usa los archivos de biblioteca estáticos que se muestran en la tabla siguiente.



| Archivo de biblioteca | Descripción                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| Strmiids. lib | Exporta identificadores de clase (CLSID) e identificadores de interfaz (IID).                                                           |
| Quartz. lib   | Exporta la función [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) . Si no llama a esta función, esta biblioteca no es obligatoria. |



 

Utilice los mismos archivos. lib para las compilaciones de depuración y lanzamiento.

## <a name="filter-base-classes"></a>Filtrar clases base

El Windows SDK proporciona un conjunto de clases de C++ que se recomiendan si se escribe un filtro DirectShow personalizado. Estas clases se proporcionan como código de ejemplo, que se puede compilar en una biblioteca estática. Para obtener más información, vea [clases base de DirectShow](directshow-base-classes.md).

## <a name="redistributable-dlls"></a>Archivos dll redistribuibles

Las aplicaciones de DirectShow escritas para Windows XP con Service Pack 2 (SP2) y versiones posteriores no necesitan redistribuir los archivos dll de DirectShow.

En el caso de Windows XP con Service Pack 1 (SP1) y versiones anteriores, los archivos dll de DirectShow redistribuibles están disponibles en el SDK de Microsoft DirectX. La versión más reciente de estos archivos dll es la versión 9.0 c. No se prevé ningún otro desarrollo de estos archivos dll redistribuibles. Windows XP con Service Pack 2 (SP2) contiene los archivos dll de c de la versión 9.0.

Los paquetes de redstributable contienen los siguientes archivos dll:

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

[Compilar filtros de DirectShow](building-directshow-filters.md)
</dt> </dl>

 

 
