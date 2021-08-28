---
description: El último paso para crear una página de referencia de eventos (ERP) es probarlo.
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: Probar una página de referencia de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2aa9fb8697181085a9b74333dba82328e90b502e6590a764fac589efa8e6f90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676645"
---
# <a name="testing-an-event-reference-page"></a>Probar una página de referencia de eventos

El último paso para crear una página de referencia de eventos (ERP) es probarlo. Puede probar un ERP viendo el archivo en un explorador HTML como Microsoft Internet Explorer. O bien, puede instalar ERP y su archivo DLL experto para probarlo para la invocación de eventos y mostrarlo en el Monitor de red Visor de eventos.

## <a name="viewing-erps-that-have-no-dll"></a>Ver LOS ARCHIVOS QUE NO TIENEN DLL

Para ver el ERP completado sin un archivo DLL experto instalado, abra el archivo con un visor HTML que admita los orígenes incrustados. En la ilustración siguiente se muestra el archivo ERP de ejemplo descrito en Writing an ERP (Escritura de un [ERP)](writing-an-event-reference-page.md) tal como se muestra con Microsoft Internet Explorer versión 4.01.

![archivo erp de ejemplo](images/ie-erp.png)

Prueba de los ERP que tienen un archivo DLL

Una vez creados los [**archivos**](experts.md) ERP y el archivo DLL experto, puede probar la funcionalidad completa de los ERP con Monitor de red. Se supone que el archivo DLL está depurado y puede generar eventos válidos.

**Para probar los ERP que tienen un archivo DLL**

1.  Compruebe que el archivo DLL experto correcto está instalado en el directorio adecuado. Para obtener más información, vea [Installing an Expert to Monitor de red 2.1](installing-an-expert-to-network-monitor-2-1.md).
2.  Compruebe el [nombre correcto](naming-an-event-reference-page.md) del archivo ERP.
3.  Compruebe la [ubicación correcta de](installing-existing-erps-to-network-monitor-2-1.md) los ERP en el Monitor de red directorio.
4.  Pruebe los ERPs expertos en la interfaz Monitor de red usuario.
5.  Generar un evento de prueba.
6.  Compruebe que erp aparece en la Monitor de red Visor de eventos.

Para obtener más información sobre cómo crear un ERP, consulte:

-   [Crear páginas de referencia de eventos expertos y de supervisión](creating-expert-and-monitor-event-reference-pages.md)
-   [Escribir una página de referencia de eventos](writing-an-event-reference-page.md)
-   [Asignar un nombre a una página de referencia de eventos](naming-an-event-reference-page.md)

 

 



