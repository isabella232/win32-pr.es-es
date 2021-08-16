---
description: Uso de GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Uso de GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f12dd613339680ac22352f4538b7029d8c9cea213c55f66e1986a8d32d0a68ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072164"
---
# <a name="using-graphedit"></a>Uso de GraphEdit

GraphEdit está disponible en microsoft Windows Software Development Kit (SDK) ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).

El nombre de la aplicación GraphEdit es "graphedt.exe". Después de instalar el SDK, "graphedt.exe" se encuentra en el directorio siguiente: Archivos de programa SDK de \[ \] \\ Microsoft Windows versión \\ bin \\ \[ \] \\ \\ .

Antes de ejecutar GraphEdit, use la utilidad regsvr32 para registrar los siguientes archivos DLL, que se encuentran en el mismo directorio:

-   proppage.dll
-   evrprop.dll

Estos archivos DLL permiten a GraphEdit mostrar páginas de propiedades para algunos de los filtros de DirectShow integrados.

## <a name="build-a-file-playback-graph"></a>Compilación de un archivo de reproducción Graph

GraphEdit puede crear un gráfico de filtros para la reproducción de archivos. Esta característica equivale a llamar al método [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) en una aplicación. En el menú **Archivo** , haga clic **en Representar archivo multimedia.** GraphEdit muestra un **cuadro de diálogo Abrir** archivo. Seleccione un archivo multimedia y haga clic **en Abrir.** GraphEdit crea un gráfico de filtros para reproducir el archivo que ha seleccionado.

También puede representar un archivo multimedia ubicado en una dirección URL. En el menú **Archivo** , haga clic en **Dirección URL de representación.** GraphEdit muestra un cuadro de diálogo en el que se va a escribir la dirección URL.

## <a name="build-a-filter-graph"></a>Compilación de un filtro Graph

GraphEdit puede crear un gráfico de filtros personalizado mediante cualquiera de los filtros registrados en el sistema. En el menú **Graph,** haga clic **en Insertar filtros.** Aparece un cuadro de diálogo con una lista de los filtros del sistema, organizados por categoría de filtro. GraphEdit compila esta lista a partir de la información del Registro. En la ilustración siguiente se muestra el cuadro de diálogo.

![¿Qué filtros desea insertar?](images/gedit12.png)

Para agregar un filtro al gráfico, seleccione el  nombre del filtro y haga clic en el botón Insertar filtros o haga doble clic en el nombre del filtro. Después de agregar los filtros, puede conectar dos filtros arrastrando el mouse desde el pin de salida de un filtro hasta el pin de entrada de otro filtro. Si los pines aceptan la conexión, GraphEdit dibuja una flecha que los conecta.

![conectar dos filtros](images/gedit-connect.png)

## <a name="run-the-graph"></a>Ejecute el Graph

Una vez que haya creado un gráfico de filtro Graph editar, puede ejecutar el gráfico para ver si funciona según lo previsto. El **Graph** menú contiene los comandos de menú **Reproducir,** **Pausar** y **Detener**. Estos comandos invocan a los métodos [**Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)y [**Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)de [**IMediaControl,**](/windows/desktop/api/Control/nn-control-imediacontrol) respectivamente. La barra de herramientas GraphEdit también tiene botones para estos comandos:

![pausar, reproducir y detener botones](images/gedit-toolbar.png)

> [!Note]  
> El comando GraphEdit **Stop** pausa primero el gráfico y busca el tiempo cero (suponiendo que el gráfico se puede buscar). Para la reproducción de archivos, esta acción restablece la ventana de vídeo al primer fotograma. A continuación, GraphEdit llama [**a IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).

 

Si el gráfico es buscable, puede buscarlo arrastrando la barra deslizante que aparece debajo de la barra de herramientas. Al arrastrar la barra deslizante, se invoca [**el método IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

## <a name="view-property-pages"></a>Ver páginas de propiedades

Algunos filtros admiten páginas de propiedades personalizadas, que proporcionan una interfaz de usuario para establecer propiedades en el filtro. Para ver la página de propiedades de un filtro en GraphEdit, haga clic con el botón derecho en el filtro y seleccione **Propiedades** en la ventana emergente. GraphEdit muestra una página de propiedades que contiene las hojas de propiedades definidas por el filtro (si las hay). Además, GraphEdit incluye una hoja de propiedades para cada pin del filtro. GraphEdit define las hojas de propiedades de pin, no el filtro. Si el pin está conectado, la hoja de propiedades de pin muestra el tipo de medio para la conexión. De lo contrario, enumera los tipos de medios preferidos del pin.

> [!Note]  
> Para usar las páginas de propiedades integradas de GraphEdit, debe registrar proppage.dll. Este archivo DLL está disponible en Windows SDK. El archivo DLL también contiene páginas de propiedades adicionales para algunos DirectShow filtros. Estas páginas de propiedades solo se proporcionan con fines de depuración.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Simulación Graph building con GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



