---
description: Personalización de la apariencia y el comportamiento de una carpeta individual con Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Personalización de carpetas con Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a671b169c4b025683cdd220ee3a920b4d592488
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468204"
---
# <a name="how-to-customize-folders-with-desktopini"></a>Personalización de carpetas con Desktop.ini

Las carpetas del sistema de archivos se muestran normalmente con un icono estándar y un conjunto de propiedades, que especifican, por ejemplo, si la carpeta se comparte. Puede personalizar la apariencia y el comportamiento de una carpeta individual mediante la creación de un Desktop.ini para esa carpeta.

## <a name="instructions"></a>Instructions

### <a name="using-desktopini-files"></a>Uso de Desktop.ini archivos

Normalmente, las carpetas se muestran con el icono de carpeta estándar. Un uso común del archivo Desktop.ini es asignar un icono personalizado o una imagen en miniatura a una carpeta. También puede usar Desktop.ini para crear  una información que muestre información sobre la carpeta y controle algunos aspectos del comportamiento de la carpeta, como especificar nombres localizados para la carpeta o los elementos de la carpeta.

**Use el procedimiento siguiente para personalizar el estilo de una carpeta con Desktop.ini:**

1.  Use [**PathMakeSystemFolder para**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) convertir la carpeta en una carpeta del sistema. Esto establece el bit de solo lectura en la carpeta para indicar que el comportamiento especial reservado para Desktop.ini debe habilitarse. También puede convertir una carpeta en una carpeta del sistema desde la línea de comandos mediante **attrib +s** *FolderName*.
2.  Cree un Desktop.ini para la carpeta. Debe marcarlo como oculto *y* *sistema para* asegurarse de que está oculto para los usuarios normales.
3.  Asegúrese de que Desktop.ini archivo que cree esté en formato Unicode. Esto es necesario para almacenar las cadenas localizadas que se pueden mostrar a los usuarios.

### <a name="creating-a-desktopini-file"></a>Creación de un Desktop.ini archivo

El Desktop.ini es un archivo de texto que permite especificar cómo se ve una carpeta del sistema de archivos. . \[ La sección ShellClassInfo permite personalizar la vista de la carpeta mediante la asignación de \] valores a varias entradas:

| Value             | Descripción                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ConfirmFileOp** | Establezca esta entrada en 0 para evitar una advertencia "Está eliminando una carpeta del sistema" al eliminar o mover la carpeta.                                                                                                                                                                                                                                                                  |
| **No compartir**     | No se admite en Windows Vista o versiones posteriores. Establezca esta entrada en 1 para evitar que la carpeta se comparta.                                                                                                                                                                                                                                                                       |
| **IconFile**      | Si desea especificar un icono personalizado para la carpeta, establezca esta entrada en el nombre de archivo del icono. Se prefiere la extensión de nombre de archivo .ico, pero también es posible especificar .bmp archivos o .exe y .dll archivos que contienen iconos. Si usa una ruta de acceso relativa, el icono está disponible para las personas que ven la carpeta a través de la red. También debe establecer la entrada **IconIndex.** |
| **IconIndex**     | Establezca esta entrada para especificar el índice de un icono personalizado. Si el archivo asignado a **IconFile** solo contiene un solo icono, establezca **IconIndex** en 0.                                                                                                                                                                                                                               |
| **InfoTip**       | Establezca esta entrada en una cadena de texto informativo. Se muestra como información cuando el cursor mantiene el puntero sobre la carpeta. Si el usuario hace clic en la carpeta, el texto de la información se muestra en el bloque de información de la carpeta, debajo de la información estándar.                                                                                                                      |



 

Las siguientes ilustraciones son de la carpeta Música con un archivo Desktop.ini personalizado. La carpeta ahora:

-   Tiene un icono personalizado.
-   No muestra una advertencia "Está eliminando una carpeta del sistema" si la carpeta se mueve o elimina.
-   No se puede compartir.
-   Muestra texto informativo cuando el cursor mantiene el puntero sobre la carpeta.

Las opciones de carpeta de las ilustraciones siguientes se establecen para mostrar los archivos ocultos para que Desktop.ini esté visible. La carpeta tiene el siguiente aspecto:

![captura de pantalla de la carpeta con icono personalizado](images/webview4.jpg)

Cuando el cursor mantiene el puntero sobre la carpeta, se muestra la información.

![captura de pantalla de la carpeta con información](images/webview6.jpg)

El icono personalizado reemplaza el icono de carpeta donde aparezca el nombre de la carpeta.

![captura de pantalla del icono personalizado reemplazando el icono de carpeta](images/webview5.jpg)

El siguiente desktop.ini se usó para personalizar la carpeta Música, como se muestra en las ilustraciones anteriores.


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



