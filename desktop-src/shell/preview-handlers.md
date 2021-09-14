---
description: Se llama a los controladores de vista previa cuando se selecciona un elemento para mostrar una vista previa ligera, completa y de solo lectura del contenido del archivo en el panel de lectura de la vista. Esto se hace sin iniciar la aplicación asociada del archivo.
ms.assetid: 166a4001-d237-44a4-a457-e320e995639c
title: Controladores de vista previa y host de vista previa del shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993c6c8e7b15d9bfc24b5dd42352407a3a53c45b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256941"
---
# <a name="preview-handlers-and-shell-preview-host"></a>Controladores de vista previa y host de vista previa del shell

Se llama a los controladores de vista previa cuando se selecciona un elemento para mostrar una vista previa *ligera,* completa y de solo lectura del contenido del archivo en el panel de lectura de la vista. Esto se hace sin iniciar la aplicación asociada del archivo.

En este tema se tratan los temas siguientes:

-   [Arquitectura del controlador de vista previa](#preview-handler-architecture)
-   [Opciones del modelo de servidor](#server-model-options)
-   [Inicialización](#initialization)
-   [Vista previa del controlador de datos Flow](#preview-handler-data-flow)
-   [Depuración de un controlador de vista previa](#debugging-a-preview-handler)
-   [Proporcionar su propio proceso para un controlador de vista previa](#providing-your-own-process-for-a-preview-handler)
-   [Temas relacionados](#related-topics)

## <a name="preview-handler-architecture"></a>Arquitectura del controlador de vista previa

Un controlador de vista previa es una aplicación hospedada. Los hosts incluyen Windows Explorer en Windows Vista o Microsoft Outlook 2007. Los hosts [**implementan IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) como método de comunicación entre el controlador de vista previa y el host.

El propio controlador de vista previa implementa estas interfaces:

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)
-   [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
-   [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals) (opcional)

Se llama al controlador a través de [**su IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), que devuelve un puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) a través del cual se solicita un objeto [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) para interactuar con el host.

## <a name="server-model-options"></a>Opciones del modelo de servidor

Los controladores de vista previa siempre se ejecutan fuera de proceso. Hay dos métodos para implementar esto:

1.  Un controlador de versión preliminar se puede crear como un servidor en proceso, pero ejecutarse a través de un host suplente fuera de proceso. Este es el método preferido. El sistema proporciona un host suplente para esto en el Prevhost.exe archivo. Los controladores de vista previa creados por este método no son compatibles con Outlook 2007 en Windows XP. Sin embargo, estos mismos controladores funcionarán en Windows Explorer y Outlook 2007 que se ejecutan en Windows Vista.
2.  Un controlador de vista previa se puede compilar como un servidor de Modelo de objetos componentes (COM) local. Esto no se recomienda por varios motivos. En primer lugar, la implementación de un servidor en proceso es más fácil. Lo que es más importante, la implementación como servidor en proceso proporciona un mayor control sobre la duración del objeto de controlador, lo que permite una mejor limpieza y eficacia.

De forma predeterminada, los controladores de vista previa se ejecutan en un proceso de nivel de integridad bajo (IL) por motivos de seguridad. Opcionalmente, puede deshabilitar la ejecución como un proceso de IL bajo estableciendo el siguiente valor en el Registro. Sin embargo, no se recomienda hacerlo. Los sistemas podrían configurarse finalmente para rechazar cualquier proceso que no sea il bajo.

```
HKEY_CLASSES_ROOT
   CLSID
      {YOUR HANDLER'S CLSID}
         DisableLowILProcessIsolation [DWORD] = 1
```

Los distintos controladores de vista previa comparten el mismo proceso de forma predeterminada. Dos instancias de Prevhost.exe se pueden ejecutar simultáneamente; uno para los controladores que se ejecutan como procesos de IL bajos, otro para los controladores que han optado por no participar en ese comportamiento.

## <a name="initialization"></a>Inicialización

Al igual que con los controladores de miniaturas y propiedades, se recomienda encarecidamente inicializar el controlador con una secuencia. Puede inicializar a través de un archivo o elemento si es necesario, pero las secuencias proporcionan la manera más segura de implementar un controlador. La inicialización a través de una secuencia garantiza la integridad de los archivos y las ventajas de estabilidad para el sistema de ejecutar el controlador como un proceso de IL bajo, como proteger el sistema de saturaciones de búfer, limitar dónde puede escribir información un controlador y limitar la comunicación con otras ventanas.

Si debe inicializar con un archivo o un elemento de Shell, almacene la ruta de acceso del archivo o una referencia a [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem). No lea datos de estos orígenes hasta que se llame [**a IPreviewHandler::D oPreview.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview)

En general, la inicialización no debe realizar ningún trabajo pesado, como crear y almacenar una imagen de vista previa. Para lograr una eficacia óptima, ese tipo de procesamiento no debe realizarse hasta que se llame a la versión preliminar.

## <a name="preview-handler-data-flow"></a>Vista previa del controlador de datos Flow

El flujo de datos del proceso de versión preliminar sigue la ruta de acceso general que se muestra aquí. El host se puede pensar como explorador Windows en Windows Vista o Outlook 2007.

1.  El controlador de vista previa se inicializa, preferiblemente con una secuencia.
2.  La ventana de vista se pasa desde el host al controlador a través [**de IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow).
3.  En este punto, el controlador no debe hacer nada más hasta que se llame a [**IPreviewHandler::D oPreview.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview)
4.  La vista previa se muestra en el panel de lectura mediante una llamada a [**IPreviewHandler::D oPreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview).
5.  El tamaño de la ventana se establece mediante [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).
6.  Se cambia el tamaño de la ventana cuando es necesario a través [**de IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).
7.  La versión preliminar se descarga y sus recursos se liberan cuando ya no se necesitan, a través de una llamada a [**IPreviewHandler::Unload**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-unload).

## <a name="debugging-a-preview-handler"></a>Depuración de un controlador de vista previa

Si ha seguido las recomendaciones para implementar el controlador de vista previa como un servidor en proceso, para depurar el controlador de vista previa, puede adjuntar a Prevhost.exe. Como se mencionó anteriormente, tenga en cuenta que podría haber dos instancias de Prevhost.exe, una para los procesos de IL bajos normales y otra para los controladores que han optado por no ejecutarse como un proceso de IL bajo.

Si no encuentra ningún Prevhost.exe en la lista de procesos disponibles, es probable que no se haya cargado en ese momento. Al hacer clic en un archivo para una vista previa, se carga el suplente y, a continuación, debería aparecer como un proceso adjuntable.

## <a name="providing-your-own-process-for-a-preview-handler"></a>Proporcionar su propio proceso para un controlador de vista previa

Si desea forzar la creación de un nuevo proceso para el controlador en lugar de ejecutarse en el proceso predeterminado, cree una nueva subclave para el controlador en **AppID** y establezca su entrada DllSurrogate en "Prevhost.exe". Use esa **subclave AppID** en lugar del valor predeterminado Prevhost.exe **AppID**.

Al proporcionar un nuevo proceso, el controlador puede evitar la ejecución en un proceso compartido como lo haría de forma predeterminada. Esto podría permitirle, por ejemplo, garantizar la versión específica de Common Language Runtime (CLR) en el proceso. Esto es necesario si va a compilar una implementación administrada de un controlador de versión preliminar.

> [!Note]  
> Los controladores de versión preliminar de 32 bits deben usar **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} cuando se instalan en sistemas operativos de 64 bits.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar controladores de vista previa](building-preview-handlers.md)
</dt> <dt>

[Cómo registrar un controlador de vista previa](how-to-register-a-preview-handler.md)
</dt> <dt>

[Instrucciones del controlador de vista previa](preview-handler-guidelines.md)
</dt> </dl>

 

 
