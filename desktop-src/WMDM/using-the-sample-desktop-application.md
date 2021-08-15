---
title: Uso de la aplicación de escritorio de ejemplo
description: Uso de la aplicación de escritorio de ejemplo
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Windows Media Administrador de dispositivos,samples
- Administrador de dispositivos,samples
- aplicaciones de escritorio, ejemplos
- Windows Ejemplo de Administrador de dispositivos multimedia, aplicación de escritorio
- Administrador de dispositivos,ejemplo de aplicación de escritorio
- ejemplos, aplicaciones de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b418458c9e6091b3e2002a30afb95abb77919d062667a9667a3aac9d4dad6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584171"
---
# <a name="using-the-sample-desktop-application"></a>Uso de la aplicación de escritorio de ejemplo

La aplicación de escritorio de ejemplo es una ventana básica de dos panorámicas similar a Windows Explorer. Permite examinar el contenido de un dispositivo mediante una visualización de vista de árbol de carpetas en el panel izquierdo y archivos en el panel derecho. La raíz de cada árbol de carpetas se considera lógicamente un dispositivo diferente, aunque algunos dispositivos pueden representarse a sí mismos como varios objetos (uno para cada almacenamiento raíz). Para leer las propiedades básicas de una carpeta o un archivo, haga clic con el botón derecho en el objeto y seleccione **Propiedades.**

Para eliminar archivos en el dispositivo, seleccione un archivo en el panel derecho y **seleccione Eliminar en** el **menú** Archivo. Para agregar archivos multimedia al dispositivo, puede arrastrar archivos desde el escritorio hasta el panel derecho del programa. Tenga en cuenta que los archivos deben tener un formato multimedia compatible con el dispositivo; Los archivos de formatos inaceptables (archivos que no son multimedia, como archivos .txt o formatos multimedia no compatibles con el dispositivo) no se enviarán al dispositivo. (Tenga en cuenta que esta restricción es del programa; Windows La Administrador de dispositivos multimedia le permite enviar cualquier archivo a un dispositivo si el dispositivo lo acepta).

Para capturar eventos de devolución de llamada enviados a la interfaz [**IWMDMOperation,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) debe comprobar la opción "Usar interfaz de operación" en el **menú** Opciones.

El **menú** Opciones también le permite elegir si desea usar varias interfaces más avanzadas con características compatibles con dispositivos avanzados.

El **menú** Contenedores tiene opciones que le permiten crear una lista de reproducción o un álbum. Para crear una lista de reproducción, seleccione una o varias canciones en el dispositivo y haga clic **en Crear** lista de reproducción en el menú **Contenedores.** Esta característica solo funciona en dispositivos MTP, ya que el código solo admite la creación de un archivo de lista de reproducción "virtual". (Una lista de reproducción virtual es una lista de reproducción especificada solo por valores de metadatos, en lugar de por un archivo físico, por ejemplo, un archivo WPL). El dispositivo debe admitir listas de reproducción vacías para usar esta característica.

Para crear un álbum (una lista de reproducción con una imagen asociada), seleccione una o varias canciones en el dispositivo y haga clic en **Crear** álbum en el **menú Contenedores.** Un cuadro de diálogo le permite examinar un archivo de imagen en el equipo para asociarlo al álbum. De forma similar a la forma en que crea listas de reproducción, la aplicación crea un archivo de álbum "vacío"; Si el dispositivo no admite discos vacíos, esta característica no funcionará.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Aplicación de escritorio de ejemplo**](sample-desktop-application.md)
</dt> </dl>

 

 




