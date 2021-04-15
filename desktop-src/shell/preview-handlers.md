---
description: Se llama a los controladores de vista previa cuando se selecciona un elemento para mostrar una vista previa ligera, enriquecida y de solo lectura del contenido del archivo en el panel de lectura de la vista. Esto se hace sin iniciar la aplicación asociada del archivo.
ms.assetid: 166a4001-d237-44a4-a457-e320e995639c
title: Controladores de vista previa y host de vista previa de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993c6c8e7b15d9bfc24b5dd42352407a3a53c45b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985639"
---
# <a name="preview-handlers-and-shell-preview-host"></a>Controladores de vista previa y host de vista previa de Shell

Se llama a los controladores de vista previa cuando se selecciona un elemento para mostrar una vista previa ligera, enriquecida y de *solo lectura* del contenido del archivo en el panel de lectura de la vista. Esto se hace sin iniciar la aplicación asociada del archivo.

En este tema se tratan los temas siguientes:

-   [Arquitectura del controlador de vista previa](#preview-handler-architecture)
-   [Opciones del modelo de servidor](#server-model-options)
-   [Inicialización](#initialization)
-   [Flujo de datos del controlador de vista previa](#preview-handler-data-flow)
-   [Depurar un controlador de vista previa](#debugging-a-preview-handler)
-   [Proporcionar su propio proceso para un controlador de vista previa](#providing-your-own-process-for-a-preview-handler)
-   [Temas relacionados](#related-topics)

## <a name="preview-handler-architecture"></a>Arquitectura del controlador de vista previa

Un controlador de vista previa es una aplicación hospedada. Los hosts incluyen el explorador de Windows en Windows Vista o Microsoft Outlook 2007. Los hosts implementan [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) como un método de comunicación entre el controlador de vista previa y el host.

El controlador de vista previa implementa estas interfaces:

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)
-   [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
-   [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals) (opcional)

Se llama al controlador a través de su [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), que devuelve un puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) a través del cual se solicita un objeto [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) para interactuar con el host.

## <a name="server-model-options"></a>Opciones del modelo de servidor

Los controladores de vista previa siempre se ejecutan fuera de proceso. Hay dos métodos para implementar esto:

1.  Un controlador de vista previa se puede compilar como un servidor en proceso pero ejecutarse a través de un host suplente fuera de proceso. Este es el método preferido. El sistema proporciona un host suplente para esto en el archivo de Prevhost.exe. Los controladores de vista previa creados por este método no son compatibles con Outlook 2007 en Windows XP. Sin embargo, estos mismos controladores funcionarán en el explorador de Windows y Outlook 2007 en Windows Vista.
2.  Un controlador de vista previa se puede compilar como un servidor de modelo de objetos componentes (COM) local. Esto no se recomienda por varias razones. En primer lugar, la implementación de un servidor en proceso es más fácil. Lo que es más importante, la implementación como un servidor en proceso proporciona un mayor control sobre la duración del objeto del controlador, lo que permite una mejor limpieza y eficacia.

De forma predeterminada, los controladores de vista previa se ejecutan en un proceso de nivel de integridad bajo (IL) por motivos de seguridad. Opcionalmente, puede deshabilitar la ejecución como un proceso IL bajo estableciendo el valor siguiente en el registro. Sin embargo, no se recomienda hacerlo. Los sistemas podrían configurarse para rechazar cualquier proceso que no sea IL bajo.

```
HKEY_CLASSES_ROOT
   CLSID
      {YOUR HANDLER'S CLSID}
         DisableLowILProcessIsolation [DWORD] = 1
```

Los diferentes controladores de vista previa comparten el mismo proceso de forma predeterminada. Dos instancias de Prevhost.exe pueden ejecutarse simultáneamente; uno para los controladores que se ejecutan como procesos de IL bajo, uno para los controladores que han decidido salir de ese comportamiento.

## <a name="initialization"></a>Inicialización

Al igual que con los controladores de miniaturas y de propiedades, se recomienda encarecidamente inicializar el controlador con una secuencia. Puede inicializar a través de un archivo o elemento si es necesario, pero las secuencias proporcionan el modo más seguro de implementar un controlador. La inicialización a través de una secuencia garantiza la integridad de los archivos y las ventajas de estabilidad para el sistema de ejecución del controlador como un proceso de IL bajo, como la protección del sistema de saturaciones del búfer, la limitación de la ubicación en la que un controlador puede escribir información y la limitación de la comunicación con otras ventanas.

Si debe inicializar con un archivo o un elemento de Shell, almacene la ruta de acceso del archivo o una referencia a [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem). No lea datos de estos orígenes hasta que se llame a [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) .

En general, la inicialización no debe realizar ningún trabajo intenso, como crear y almacenar una imagen de vista previa. Para lograr una eficiencia óptima, ese tipo de procesamiento no debe realizarse hasta que se llame a la vista previa para.

## <a name="preview-handler-data-flow"></a>Flujo de datos del controlador de vista previa

El flujo de datos en el proceso de vista previa sigue la ruta de acceso general que se muestra aquí. El host puede considerarse como el explorador de Windows en Windows Vista o Outlook 2007.

1.  El controlador de vista previa se inicializa, preferiblemente con una secuencia.
2.  La ventana ver se pasa desde el host al controlador a través de [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow).
3.  En este momento, el controlador no debe hacer nada más hasta que se llama a [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) .
4.  La vista previa se muestra en el panel de lectura a través de una llamada a [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview).
5.  El tamaño de la ventana se establece a través de [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).
6.  Se cambia el tamaño de la ventana cuando es necesario a través de [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).
7.  La versión preliminar se descarga y sus recursos se liberan cuando ya no se necesitan, a través de una llamada a [**IPreviewHandler:: Unload**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-unload).

## <a name="debugging-a-preview-handler"></a>Depurar un controlador de vista previa

Si ha seguido las recomendaciones para implementar el controlador de vista previa como un servidor en proceso, para depurar el controlador de vista previa, puede adjuntar a Prevhost.exe. Como se mencionó anteriormente, tenga en cuenta que podría haber dos instancias de Prevhost.exe, una para los procesos normales de IL bajo y otra para los controladores que han optado por no ejecutarse como un proceso IL bajo.

Si no encuentra Prevhost.exe en la lista de procesos disponibles, es probable que no se haya cargado en ese momento. Al hacer clic en un archivo para obtener una vista previa, se carga el suplente y debe aparecer como un proceso que se podrá adjuntar.

## <a name="providing-your-own-process-for-a-preview-handler"></a>Proporcionar su propio proceso para un controlador de vista previa

Si desea forzar la creación de un nuevo proceso para el controlador en lugar de ejecutarlo en el proceso predeterminado, cree una nueva subclave para el controlador en **AppID** y establezca su entrada DllSurrogate en "Prevhost.exe". Use esa subclave **AppID** en lugar del valor predeterminado Prevhost.exe **AppID**.

Al proporcionar un nuevo proceso, el controlador puede evitar que se ejecute en un proceso compartido, tal y como lo haría de forma predeterminada. Esto podría permitirle, por ejemplo, garantizar la versión específica del Common Language Runtime (CLR) en el proceso. Esto es necesario si va a crear una implementación administrada de un controlador de vista previa.

> [!Note]  
> los controladores de vista previa de bits de 32 deben usar **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} cuando se instalan en sistemas operativos de 64 bits.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear controladores de vista previa](building-preview-handlers.md)
</dt> <dt>

[Cómo registrar un controlador de vista previa](how-to-register-a-preview-handler.md)
</dt> <dt>

[Instrucciones de controlador de vista previa](preview-handler-guidelines.md)
</dt> </dl>

 

 
