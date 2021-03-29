---
title: Usar la aplicación de escritorio de ejemplo
description: Usar la aplicación de escritorio de ejemplo
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Administrador de dispositivos de Windows Media, ejemplos
- Administrador de dispositivos, ejemplos
- aplicaciones de escritorio, ejemplos
- Windows Media Administrador de dispositivos, ejemplo de aplicación de escritorio
- Administrador de dispositivos, ejemplo de aplicación de escritorio
- ejemplos, aplicaciones de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd511ea5241f458d2cd926dc8fb2f3681757ff8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774281"
---
# <a name="using-the-sample-desktop-application"></a>Usar la aplicación de escritorio de ejemplo

La aplicación de escritorio de ejemplo es una ventana básica de dos paneles similar a la del explorador de Windows. Permite examinar el contenido de un dispositivo, usar una vista de árbol de carpetas en el panel izquierdo y archivos en el panel derecho. La raíz de cada árbol de carpetas se considera lógicamente un dispositivo diferente, aunque algunos dispositivos pueden representarse como varios objetos (uno por cada almacenamiento raíz). Para leer las propiedades básicas de una carpeta o un archivo, haga clic con el botón secundario en el objeto y seleccione **propiedades**.

Puede eliminar archivos en el dispositivo seleccionando un archivo en el panel derecho y seleccionando **eliminar** en el menú **archivo** . Para agregar archivos multimedia al dispositivo, puede arrastrar archivos desde el escritorio hasta el panel derecho del programa. Tenga en cuenta que los archivos deben tener un formato multimedia compatible con el dispositivo. los archivos de formatos no aceptables (archivos no multimedia, como archivos. txt o formatos multimedia no admitidos por el dispositivo) no se enviarán al dispositivo. (Tenga en cuenta que esta restricción es la del programa; Windows Media Administrador de dispositivos permite enviar cualquier archivo a un dispositivo si el dispositivo lo aceptará.

Para capturar los eventos de devolución de llamada enviados a la interfaz [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) , debe activar la opción "usar interfaz de operación" en el menú **Opciones** .

El menú **Opciones** también le permite elegir si desea usar varias interfaces más avanzadas con características compatibles con dispositivos avanzados.

El menú **contenedores** tiene opciones que le permiten crear una lista de reproducción o un álbum. Para crear una lista de reproducción, seleccione una o varias canciones en el dispositivo y haga clic en **crear lista de reproducción** en el menú **contenedores** . Esta característica solo funciona en dispositivos MTP, ya que el código solo admite la creación de un archivo de lista de reproducción "virtual". (Una lista de reproducción virtual es una lista de reproducción que solo se especifica mediante valores de metadatos, en lugar de un archivo físico, por ejemplo un archivo WPL). El dispositivo debe admitir listas de reproducción vacías para usar esta característica.

Para crear un álbum (una lista de reproducción con una imagen asociada), seleccione una o varias canciones en el dispositivo y haga clic en **crear álbum** en el menú **contenedores** . Un cuadro de diálogo le permite buscar un archivo de imagen en el equipo para asociarlo con el álbum. Del mismo modo que crea listas de reproducción, la aplicación crea un archivo de álbum "vacío"; Si el dispositivo no admite álbumes vacíos, esta característica no funcionará.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Aplicación de escritorio de ejemplo**](sample-desktop-application.md)
</dt> </dl>

 

 




