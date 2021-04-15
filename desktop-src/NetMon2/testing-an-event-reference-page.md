---
description: El paso final de la creación de una página de referencia de eventos (ERP) es probarlo.
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: Probar una página de referencia de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6afaaec279403922abde578b9e73931e607680f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677421"
---
# <a name="testing-an-event-reference-page"></a>Probar una página de referencia de eventos

El paso final de la creación de una página de referencia de eventos (ERP) es probarlo. Puede probar un ERP viendo el archivo en un explorador HTML, como Microsoft Internet Explorer. O bien, puede instalar el ERP y su archivo DLL de expertos para probarlo para la invocación de eventos y mostrarlo en el Visor de eventos de Monitor de red.

## <a name="viewing-erps-that-have-no-dll"></a>Ver O ERP e que no tienen DLL

Para ver el ERP completado sin un archivo DLL de experto instalado, abra el archivo con un visor HTML que admita los orígenes incrustados. En la ilustración siguiente se muestra el archivo ERP de ejemplo que se describe en [Writing a ERP](writing-an-event-reference-page.md) , tal como se muestra con la versión 4,01 de Microsoft Internet Explorer.

![archivo ERP de ejemplo](images/ie-erp.png)

Prueba de O ERP e que tienen un archivo DLL

Después de crear los archivos ERP y el archivo dll de [**expertos**](experts.md) , puede probar la funcionalidad completa de su o erp e con monitor de red. Se supone que el archivo DLL está depurado y puede generar eventos válidos.

**Para probar O ERP e que tienen un archivo DLL**

1.  Compruebe que el archivo DLL de experto correcto está instalado en el directorio adecuado. Para obtener más información, consulte [instalación de un experto en Monitor de red 2,1](installing-an-expert-to-network-monitor-2-1.md).
2.  Compruebe el [nombre correcto](naming-an-event-reference-page.md) del archivo ERP.
3.  Compruebe la [ubicación correcta](installing-existing-erps-to-network-monitor-2-1.md) de o ERP e en el directorio de monitor de red.
4.  Pruebe Expert O ERP e en la interfaz de usuario de Monitor de red.
5.  Genere un evento de prueba.
6.  Compruebe que el ERP aparece en el Visor de eventos de Monitor de red.

Para obtener más información acerca de la creación de un ERP, consulte:

-   [Creación de páginas de referencia de eventos Expert y monitor](creating-expert-and-monitor-event-reference-pages.md)
-   [Escribir una página de referencia de eventos](writing-an-event-reference-page.md)
-   [Asignar un nombre a una página de referencia de eventos](naming-an-event-reference-page.md)

 

 



