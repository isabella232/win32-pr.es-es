---
description: Usar GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Usar GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e78118253d86a88231456b72dc8c42ed2a674f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546054"
---
# <a name="using-graphedit"></a>Usar GraphEdit

GraphEdit está disponible en el kit de desarrollo de software (SDK) de Microsoft Windows ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).

El nombre de la aplicación GraphEdit es "graphedt.exe". Después de instalar el SDK, "graphedt.exe" se encuentra en el siguiente directorio: \[ archivos de programa \] \\ Microsoft SDK \\ Windows \\ \[ version \] \\ bin \\ .

Antes de ejecutar GraphEdit, use la utilidad regsvr32 para registrar los siguientes archivos dll, que se encuentran en el mismo directorio:

-   proppage.dll
-   evrprop.dll

Estos archivos dll permiten a GraphEdit mostrar páginas de propiedades para algunos de los filtros de DirectShow integrados.

## <a name="build-a-file-playback-graph"></a>Crear un gráfico de reproducción de archivos

GraphEdit puede crear un gráfico de filtro para la reproducción de archivos. Esta característica es equivalente a llamar al método [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) en una aplicación. En el menú **archivo** , haga clic en **representar archivo multimedia**. GraphEdit muestra un cuadro de diálogo **Abrir archivo** . Seleccione un archivo multimedia y haga clic en **abrir**. GraphEdit crea un gráfico de filtro para reproducir el archivo que ha seleccionado.

También puede representar un archivo multimedia ubicado en una dirección URL. En el menú **archivo** , haga clic en **representar dirección URL**. GraphEdit muestra un cuadro de diálogo en el que se va a escribir la dirección URL.

## <a name="build-a-filter-graph"></a>Crear un gráfico de filtro

GraphEdit puede crear un gráfico de filtro personalizado mediante cualquiera de los filtros registrados en el sistema. En el menú **gráfico** , haga clic en **Insertar filtros**. Aparece un cuadro de diálogo con una lista de los filtros del sistema organizados por categoría de filtro. GraphEdit crea esta lista a partir de la información del registro. En la ilustración siguiente se muestra el cuadro de diálogo.

![¿Qué Filtros desea insertar?](images/gedit12.png)

Para agregar un filtro al gráfico, seleccione el nombre del filtro y haga clic en el botón **Insertar filtros** o haga doble clic en el nombre del filtro. Una vez agregados los filtros, puede conectar dos filtros arrastrando el mouse desde el anclaje de salida de un filtro hasta el anclaje de entrada de otro filtro. Si los pin aceptan la conexión, GraphEdit dibuja una flecha que los conecta.

![conexión de dos filtros](images/gedit-connect.png)

## <a name="run-the-graph"></a>Ejecutar el gráfico

Una vez que haya creado un gráfico de filtro en la edición del gráfico, puede ejecutar el gráfico para ver si funciona como se espera. El menú **gráfico** contiene los comandos de menú **reproducir**, **pausar** y **detener**. Estos comandos invocan a los métodos [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) [**Ejecutar**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**pausar**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)y [**detener**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), respectivamente. La barra de herramientas GraphEdit tiene botones para estos comandos, también:

![botones pausar, reproducir y detener](images/gedit-toolbar.png)

> [!Note]  
> El comando GraphEdit **Stop** primero pausa el gráfico y busca el tiempo cero (suponiendo que se pueda buscar en el gráfico). Para la reproducción de archivos, esta acción restablece la ventana de vídeo en el primer fotograma. A continuación, GraphEdit llama a [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).

 

Si el gráfico es buscable, puede buscarlo arrastrando la barra deslizante que aparece debajo de la barra de herramientas. Al arrastrar la barra deslizante se invoca el método [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

## <a name="view-property-pages"></a>Ver páginas de propiedades

Algunos filtros admiten páginas de propiedades personalizadas, que proporcionan una interfaz de usuario para establecer las propiedades del filtro. Para ver la página de propiedades de un filtro en GraphEdit, haga clic con el botón secundario en el filtro y seleccione **propiedades** en la ventana emergente. GraphEdit muestra una página de propiedades que contiene las hojas de propiedades definidas por el filtro (si existe). Además, GraphEdit incluye una hoja de propiedades para cada pin del filtro. Las hojas de propiedades de anclaje están definidas por GraphEdit, no por el filtro. Si el PIN está conectado, la hoja de propiedades del PIN muestra el tipo de medio para la conexión. De lo contrario, muestra los tipos de medios preferidos del PIN.

> [!Note]  
> Para usar las páginas de propiedades integradas de GraphEdit, debe registrar proppage.dll. Este archivo DLL está disponible en el Windows SDK. El archivo DLL también contiene páginas de propiedades adicionales para algunos filtros de DirectShow. Estas páginas de propiedades se proporcionan solo con fines de depuración.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Simular la compilación de gráficos con GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



