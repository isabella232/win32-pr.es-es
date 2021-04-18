---
description: Personalizar la apariencia y el comportamiento de una carpeta individual con Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Cómo personalizar carpetas con Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaac3e6a96257e63b5e4210da0aa6e6e1db77eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560229"
---
# <a name="how-to-customize-folders-with-desktopini"></a>Cómo personalizar carpetas con Desktop.ini

Las carpetas del sistema de archivos se muestran normalmente con un icono y un conjunto de propiedades estándar que especifican, por ejemplo, si la carpeta está compartida. Puede personalizar la apariencia y el comportamiento de una carpeta individual creando un archivo de Desktop.ini para esa carpeta.

## <a name="instructions"></a>Instrucciones

### <a name="using-desktopini-files"></a>Usar archivos de Desktop.ini

Las carpetas se muestran normalmente con el icono de la carpeta estándar. Un uso común del archivo Desktop.ini es asignar un icono personalizado o una imagen en miniatura a una carpeta. También puede usar Desktop.ini para crear un recuadro informativo *que muestra* información sobre la carpeta y controla algunos aspectos del comportamiento de la carpeta, como la especificación de nombres localizados para la carpeta o los elementos de la carpeta.

**Utilice el siguiente procedimiento para personalizar el estilo de una carpeta con Desktop.ini:**

1.  Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) para convertir la carpeta en una carpeta del sistema. Esto establece el bit de solo lectura en la carpeta para indicar que debe habilitarse el comportamiento especial reservado para Desktop.ini. También puede convertir una carpeta en una carpeta del sistema desde la línea de comandos mediante **attrib + s** *nombreDeCarpeta*.
2.  Cree un archivo de Desktop.ini para la carpeta. Debe marcarlo como *oculto* y *sistema* para asegurarse de que está oculto para los usuarios normales.
3.  Asegúrese de que el archivo de Desktop.ini que crea está en el formato Unicode. Esto es necesario para almacenar las cadenas traducidas que se pueden mostrar a los usuarios.

### <a name="creating-a-desktopini-file"></a>Crear un archivo de Desktop.ini

El archivo Desktop.ini es un archivo de texto que le permite especificar cómo se ve una carpeta del sistema de archivos. El \[ . \] La sección ShellClassInfo permite personalizar la vista de la carpeta asignando valores a varias entradas:

|                   |                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Entrada**         | **Valor**                                                                                                                                                                                                                                                                                                                                                                      |
| **ConfirmFileOp** | Establezca esta entrada en 0 para evitar que se produzca una advertencia al eliminar una carpeta del sistema al eliminar o mover la carpeta.                                                                                                                                                                                                                                                                  |
| **Uso compartido**     | No se admite en Windows Vista o posterior. Establezca esta entrada en 1 para evitar que se comparta la carpeta.                                                                                                                                                                                                                                                                       |
| **IconFile**      | Si desea especificar un icono personalizado para la carpeta, establezca esta entrada en el nombre de archivo del icono. Se prefiere la extensión de nombre de archivo. ico, pero también es posible especificar archivos. bmp, o archivos. exe y. dll que contengan iconos. Si usa una ruta de acceso relativa, el icono está disponible para los usuarios que ven la carpeta a través de la red. También debe establecer la entrada de **IconIndex** . |
| **IconIndex**     | Establezca esta entrada para especificar el índice de un icono personalizado. Si el archivo asignado a **IconFile** solo contiene un único icono, establezca **IconIndex** en 0.                                                                                                                                                                                                                               |
| **InfoTip**       | Establezca esta entrada en una cadena de texto informativo. Se muestra como un recuadro informativo cuando el cursor se mantiene sobre la carpeta. Si el usuario hace clic en la carpeta, se muestra el texto de información en el bloque de información de la carpeta, debajo de la información estándar.                                                                                                                      |



 

Las siguientes ilustraciones son de la carpeta música con un archivo de Desktop.ini personalizado. La carpeta ahora:

-   Tiene un icono personalizado.
-   No muestra la advertencia "se está eliminando una carpeta de sistema" si la carpeta se mueve o se elimina.
-   No se puede compartir.
-   Muestra texto informativo cuando el cursor se mantiene sobre la carpeta.

Las opciones de carpeta de las ilustraciones siguientes se establecen para mostrar los archivos ocultos de modo que Desktop.ini esté visible. La carpeta tiene el siguiente aspecto:

![captura de pantalla de la carpeta con icono personalizado](images/webview4.jpg)

Cuando el cursor se mantiene sobre la carpeta, se muestra el recuadro informativo.

![captura de pantalla de la carpeta con un recuadro informativo](images/webview6.jpg)

El icono personalizado reemplaza el icono de carpeta en todas partes donde aparece el nombre de la carpeta.

![captura de pantalla del icono personalizado que reemplaza el icono de carpeta](images/webview5.jpg)

El siguiente archivo de desktop.ini se usó para personalizar la carpeta música, tal como se ha descrito en las ilustraciones anteriores.


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



