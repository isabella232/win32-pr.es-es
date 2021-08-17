---
title: Estructura de la aplicación de escritorio de ejemplo
description: Estructura de la aplicación de escritorio de ejemplo
ms.assetid: e042470d-dc78-488c-bcad-2e8d34714d5d
keywords:
- Windows Media Administrador de dispositivos,samples
- Administrador de dispositivos,samples
- aplicaciones de escritorio, ejemplos
- Windows Ejemplo de Administrador de dispositivos multimedia, aplicación de escritorio
- Administrador de dispositivos,ejemplo de aplicación de escritorio
- ejemplos, aplicaciones de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dde8250a5efc8bc0f0b9582739bd8770d95ee586ea571a43bcbb9be69e8774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957165"
---
# <a name="structure-of-the-sample-desktop-application"></a>Estructura de la aplicación de escritorio de ejemplo

La aplicación de escritorio de ejemplo consta de dos partes principales:

-   El proyecto wmdapp contiene la mayoría de las clases que muestran la interfaz de usuario, controlan el arrastre y la colocación, y realizan todas las funciones necesarias del programa.
-   El proyecto proghelp es una aplicación auxiliar que contiene clases no esenciales para controlar las notificaciones de estado y las transferencias de archivos manuales desde el escritorio a la aplicación.

El ejecutable usa el proyecto auxiliar  solo cuando el  usuario selecciona Usar interfaz de operación en el menú Opciones para controlar la transferencia manual de archivos al dispositivo e incrementar la barra de estado en el formulario de progreso de descarga. Todo el resto de la aplicación se controla en el proyecto wmdapp.



| Clase                | Archivo                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| —                    | wmdmapp.cpp             | Clase que controla la ventana primaria de la interfaz de usuario. El código de este archivo también controla algunas entradas del usuario no manipuladas por CDevFiles, como la creación de una lista de reproducción o un álbum en un dispositivo, la eliminación de archivos y el registro de opciones de menú.                                                                                                                                                    |
| CDevices             | Devices.cpp             | Clase que controla el panel izquierdo de la ventana principal de la aplicación, donde se enumeran los dispositivos disponibles. Esta clase administra el bucle de mensajería, que controla la entrada del usuario, como seleccionar un dispositivo y notificar al panel CDevFiles que cargue los archivos adecuados cuando la selección del dispositivo haya cambiado.                                                                              |
| CDevFiles            | Devfiles.cpp            | Clase que controla el panel derecho de la ventana principal de la aplicación, donde se enumeran los archivos del dispositivo seleccionado. Esta clase administra el bucle de mensajería y controla la entrada del usuario, como arrastrar archivos al dispositivo y eliminar archivos del dispositivo.                                                                                                                          |
| CStatus              | Status.cpp              | Clase que controla la barra de estado inferior de la ventana principal, donde se muestra el número de dispositivos y archivos, junto con la cantidad de memoria libre y usada en el dispositivo seleccionado.                                                                                                                                                                                                         |
| CWMDM                | Wmdevmgr.cpp            | Interfaz de nivel superior para Windows Media Administrador de dispositivos. Esta clase controla la autenticación, recupera la interfaz **IWMDeviceManager** de nivel superior y registra las notificaciones con la **interfaz IWMDMNotification.**                                                                                                                                                                  |
| CProgress            | Progress.cpp            | Clase del proyecto de aplicación principal que crea y administra el cuadro de diálogo que muestra el progreso de un evento.                                                                                                                                                                                                                                                                             |
| CItemData            | ItemData.cpp            | Una clase contenedora que contiene un puntero a un almacenamiento (si representa un archivo o carpeta en el dispositivo) o un dispositivo (si representa un dispositivo), así como una variedad de información sobre el objeto, incluidos el tamaño y los atributos.                                                                                                                                                                  |
| CNotificationHandler | Notificationhandler.cpp | Controla las notificaciones de llegada y eliminación del dispositivo mediante una alerta a la ventana CDevices.                                                                                                                                                                                                                                                                                                               |
| CProgressHelper      | ProgressHelper.cpp      | Creado por CDevFiles en funciones locales para recibir notificaciones de Windows Media Administrador de dispositivos mediante la implementación **de IWMDMProgress**. La clase CProgress la usa para determinar la cantidad de barras de la barra de progreso y cuándo finaliza una acción. Esta clase se define como un objeto COM que expone la interfaz del SDK **IWMDMProgress** y una interfaz personalizada IWMDMProgressHelper. |
| COperationHelper     | Operationhelper.cpp     | Esta clase implementa **IWMDMOperation para** controlar la transferencia manual de archivos. Tiene varios subprocesos para permitir que se produzca de forma asincrónica y se define como un objeto COM que expone una interfaz personalizada, IWMDMOperationHelper, para crear instancias e inicializar la clase. Esta clase solo se usa si el usuario selecciona "Usar interfaz de operación" en el **menú** Opciones.                            |



 

En las listas siguientes se describen los pasos básicos que se producen para varias acciones del usuario:

**Al iniciar**

Los siguientes pasos principales se producen cuando se inicia la aplicación de ejemplo.

1.  Se crea una instancia de la variable GLOBAL CWMDM y se autentica, y se registra para recibir notificaciones.
2.  Se crea una instancia de CDevices global y se llama a CDevices::Create para crear y rellenar el panel de dispositivos.
3.  Se crea una instancia de CDevFiles global y se llama a CDevFiles::Create para crear el panel de archivos (que no se rellena hasta que el usuario selecciona un dispositivo).
4.  Se crea una instancia de CStatus global y se llama a CStatus::Create para crear una instancia de la barra de estado.
5.  \_OnViewRefresh enumera todos los dispositivos e inicializa y agrega todos los dispositivos (CItemData) a CDevices y actualiza la barra de estado para mostrar el número de dispositivos.
6.  CDevices::AddItem agrega el elemento a la vista de árbol que representa los dispositivos, con un puntero a sí mismo como TVITEM.lparam. Todos los objetos CDevice (dispositivos) y CDevFiles (archivo) se almacenan en este miembro del nodo treeview en la ventana adecuada.

**Al seleccionar un dispositivo**

Los siguientes pasos principales se producen cuando el usuario selecciona un dispositivo en el panel izquierdo de la ventana de la aplicación.

1.  La ventana CDevices captura un clic y envía un mensaje UPDATEDEVICE de DRM de WM \_ \_ a sí mismo.
2.  CDevices recibe su propio mensaje y llama a UpdateSelection, que indica al objeto CDevFiles global que borre todo, enumere todos los elementos de nivel superior del dispositivo y llame a CDevFiles::AddItem para agregar cada uno al panel de archivos.
3.  Por último, CDevices llama a CDevFiles::UpdateStatusBar para actualizar la barra de estado con la información correcta del dispositivo y del archivo.

**Al crear una lista de reproducción**

Después de hacer clic en "Crear lista de reproducción" en el **menú Contenedores,** la aplicación llama a la función local \_ OnCreatePlaylist, que realiza las siguientes acciones:

1.  Obtenga el número de elementos seleccionados de la variable global CDevFiles.
2.  Llame a la función local DlgNamePlaylist para abrir un cuadro de diálogo para obtener un nombre para la lista de reproducción.
3.  Llame a CProgress::Create para crear una ventana de diálogo que muestre el progreso de la acción y establezca parámetros en la clase CProgress, como el texto del título, el intervalo, el valor actual, entre otros.
4.  Recorrer en bucle todos los elementos seleccionados en el objeto de vista de árbol CDevFiles y solicitar el objeto CItemData asociado a cada archivo seleccionado en la vista de árbol, incrementando la barra de diálogo de progreso con cada archivo. Los archivos se agregan a una matriz de [**interfaces IWMDMStorage.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage)
5.  Obtenga un identificador para el elemento seleccionado actualmente y consulte una interfaz [**IWMDMStorageControl3,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) que se usará más adelante para crear la nueva lista de reproducción en el dispositivo.
6.  Consulte el objeto seleccionado para [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)y llame a [**CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject) para crear una nueva [**interfaz IWMDMMetaData.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)
7.  Agregue el código de formato WMDM FORMATCODE ABSTRACTAUDIOVIDEOPLAYLIST a la nueva interfaz IWMDMMetadata y cree una lista de reproducción en el dispositivo mediante una llamada \_ \_ a [**IWMDMStorageControl3::Insert3,**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)  pasando la interfaz de metadatos. El método recupera un puntero al nuevo **IWMDMStorage** en el dispositivo.
8.  Rellene la lista de reproducción consultando el nuevo almacenamiento para [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)y llamando a [**IWMDMStorage4::SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences), pasando la matriz de punteros **IWMDMStorage** recopilados en el paso 4.
9.  Por último, cree un nuevo objeto CItemData para contener la nueva lista de reproducción en el dispositivo, inicialíicelo con el nuevo almacenamiento y llame a CDevFiles::AddItem para agregarlo al panel CDevFiles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Aplicación de escritorio de ejemplo**](sample-desktop-application.md)
</dt> </dl>

 

 




