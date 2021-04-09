---
title: Reemplazar la aplicación Visor de imágenes y fax de Windows con el verbo vista previa
description: A partir de Windows XP, los usuarios pueden ver, girar, imprimir y acercar las imágenes.
ms.assetid: cb08756b-6a5d-424d-ab6d-2e34d180ec4e
keywords:
- Visor de imágenes y fax de Windows
- Vista previa del verbo
- prácticas recomendadas, visor de imágenes y fax de Windows
- prácticas recomendadas, verbo de vista previa
- rendimiento, visor de imágenes y fax de Windows
- rendimiento, verbo de vista previa
- registro, verbo de vista previa
- Register, verbo de presentación de diapositivas
- Verbo de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6769e13aaea41b3b05bbf674ea95d7f88fb646
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995259"
---
# <a name="replacing-the-windows-picture-and-fax-viewer-application-using-the-preview-verb"></a>Reemplazar la aplicación Visor de imágenes y fax de Windows con el verbo vista previa

\[La característica visor de imágenes y fax solo se admite en Windows XP. \]

A partir de Windows XP, los usuarios pueden ver, girar, imprimir y acercar las imágenes. Algunas de estas características se proporcionan a través del shell de Windows y otras a través de la aplicación Visor de imágenes y fax de Windows. Aunque el visor de imágenes y fax de Windows proporciona una línea base excelente de características y es una parte fundamental de la experiencia de creación de imágenes, si lo prefiere, puede reemplazarla fácilmente por otra aplicación. Este documento está diseñado para ayudarle a reemplazar de forma eficaz la aplicación Visor de imágenes y fax de Windows sin perder características importantes o degradar la experiencia del usuario.

-   [Procedimientos recomendados](#best-practices)
    -   [Rendimiento](#performance)
    -   [Características](#features)
    -   [Compatibilidad con formato](#format-support)
-   [Registro del verbo de vista previa](#registering-for-the-preview-verb)
-   [Registrando el verbo de edición](#registering-for-the-edit-verb)
-   [Registro del verbo de presentación de diapositivas](#registering-for-the-slideshow-verb)
-   [Temas relacionados](#related-topics)

## <a name="best-practices"></a>Prácticas recomendadas

En Windows XP y versiones posteriores, el shell incluye un verbo que puede usar para permitir que los usuarios obtengan una vista previa de las imágenes. Se denomina *vista previa*. Este verbo resalta la tarea de usuario principal para las imágenes, que está viendo. Para que esta experiencia funcione correctamente, la aplicación Visor de imágenes y fax de Windows posee la Asociación de vista previa de forma predeterminada.

El visor de imágenes y fax de Windows, o cualquier aplicación que posea una asociación de archivo, incluye un elemento que inicia la aplicación de edición del usuario. Dado que el verbo de vista previa solo se usa para obtener una vista previa de las imágenes en lugar de editarlas, la aplicación debe asegurarse de seguir las recomendaciones de este documento al solicitar esa asociación.

Desea asegurarse de que una aplicación que edita imágenes puede seguir aprovechando el verbo Edit. Por ejemplo, si un usuario tiene Microsoft Picture It! instalado, al hacer doble clic en un archivo. jpg, el equipo debe iniciar la aplicación Visor de imágenes y fax de Windows. Sin embargo, al hacer clic en **Editar** en la barra de herramientas, el equipo debe iniciar Picture It! con ese archivo. jpg.

Hay tres consideraciones que debe tener en cuenta al reemplazar el visor de imágenes y fax de Windows. Dichos componentes son:

-   [Rendimiento](#performance)
-   [Características](#features)
-   [Compatibilidad con formato](#format-support)

### <a name="performance"></a>Rendimiento

La consideración principal del rendimiento es la velocidad a la que se cargan las imágenes. Aunque no se proporciona ninguna métrica de rendimiento, debe intentar reemplazar el visor de imágenes y fax de Windows con una aplicación que coincida o aumente el rendimiento.

La propia aplicación debe cargarse rápidamente. Uno de los principales problemas que experimentan los usuarios con las aplicaciones que toman las asociaciones de imágenes es el tiempo de espera mientras se carga la aplicación. A menudo, esto se debe a tener una eficaz carga de la aplicación de edición al hacer doble clic en un archivo de imagen, incluso cuando el usuario simplemente desea ver el archivo. Es mejor para el usuario si proporciona opciones que las llevan rápidamente a una aplicación en la que pueden editar la imagen solo cuando sea su voluntad.

### <a name="features"></a>Características

Existe un conjunto mínimo de características que la aplicación debe proporcionar al reemplazar la aplicación Visor de imágenes y fax de Windows. Los pasos son los siguientes:



| Característica                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mostrar imagen en el mejor ajuste             | Esto ofrece al usuario la opción de ver la imagen completa escalada hasta el tamaño en el que mejor se adapta al espacio visible de la ventana de la aplicación. De esta manera, pueden ver toda la imagen, incluso si está ligeramente degradada, para ello. Este debe ser el valor predeterminado cada vez que se carga una imagen que es mayor que el espacio visible. De lo contrario, la imagen debe aparecer en su tamaño real. Por ejemplo, una imagen de 64 x 64 píxeles no se debe escalar a un tamaño de 600 x 600 simplemente porque es el tamaño de la ventana de la aplicación. |
| Mostrar imagen en tamaño real          | Esto ofrece al usuario la opción de ver la imagen completa en su resolución real. Esto les permite verlos en su tamaño adecuado y desplazarse sobre la imagen. No debe ser la vista predeterminada a menos que la imagen sea más pequeña que el espacio visible en la aplicación.                                                                                                                                                                                                                                                              |
| Acercar imagen                    | Esto permite al usuario acercar una parte de la imagen para investigar detalles más precisos, o simplemente ampliar una imagen pequeña. Esto es similar a mostrar el tamaño real de la imagen, pero permite al usuario controlar el grado de visualización de la imagen.                                                                                                                                                                                                                                                                                            |
| Alejar imagen                  | Esto permite al usuario alejar y obtener una vista más amplia. Esto es similar a mostrar la imagen en el mejor ajuste, pero permite al usuario controlar hasta qué punto ven la imagen.                                                                                                                                                                                                                                                                                                                                                          |
| Siguiente imagen                         | Esto permite al usuario ver la siguiente imagen de la lista. Esta lista puede ser todas las imágenes de la carpeta actual o todas las imágenes que el usuario selecciona como parte de una operación de selección MultiSelect. es decir, cuando hace clic y arrastra a imágenes de resaltado o mantiene presionado el botón de control y hace clic en archivos individuales.                                                                                                                                                                                                                       |
| Imagen anterior                     | Esto permite al usuario ver la imagen anterior en la lista.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Girar a la derecha 90 grados        | Esto permite al usuario girar la imagen en el sentido de las agujas del reloj por trimestres. Windows XP guarda automáticamente la imagen cuando la gira para reducir la pérdida de calidad de la imagen. La aplicación también puede girar incrementos más pequeños, pero 90 grados es el estándar como la rotación más común de las imágenes digitales.                                                                                                                                                                                                                                 |
| Girar a la derecha 90 grados | Esto permite al usuario girar la imagen en sentido contrario a las agujas del reloj por trimestres.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Impresión                              | Esto permite al usuario imprimir la imagen que aparece actualmente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Guardar como                            | Esto permite al usuario guardar la imagen en una carpeta especificada.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Eliminar imagen                       | Esto permite al usuario eliminar la imagen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ayuda                               | Esto proporciona al usuario la documentación de ayuda relacionada con el uso de la aplicación de visualización.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Propiedades                         | Esto permite al usuario ver o editar las propiedades de la imagen, normalmente la información de archivo de imagen intercambiable (EXIF) almacenada en cada imagen.                                                                                                                                                                                                                                                                                                                                                                                      |
| Editar                               | Esto permite al usuario iniciar su programa de edición preferido registrado para el verbo editar en la imagen.                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="format-support"></a>Compatibilidad con formato

Dado que es difícil para una aplicación admitir todas las imágenes diferentes, se recomienda que la aplicación use GDI+ de Windows para admitir formatos de imagen. Sin embargo, si decide no usar GDI+, la aplicación debe asumir solo las asociaciones de archivos para las que se ha probado y se sabe que funciona. A continuación, si el usuario necesita ver un formato que no controla, el visor de imágenes y fax de Windows puede seguir proporcionando acceso.

Por ejemplo, el visor de imágenes y fax de Windows proporciona una serie de herramientas para editar anotaciones en imágenes. tiff. A menos que esta funcionalidad esté duplicada en la aplicación, no debe registrar la aplicación para controlar las imágenes. tiff. El principio de conducción debe ser asegurarse de que el usuario no pierde ninguna funcionalidad.

## <a name="registering-for-the-preview-verb"></a>Registro del verbo de vista previa

El registro de una aplicación para controlar el verbo de vista previa es bastante sencillo. Busque el siguiente valor de la aplicación en el registro, donde Application. JPEG representa el nombre de la clave de Asociación de archivo de la aplicación (consulte [programas predeterminados](/windows/desktop/shell/default-programs) para obtener más detalles):

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         open
            command
               (Default) = app.exe %1
```

Cambie el nombre de la subclave **Open** a "Preview" como se muestra aquí.

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         preview
            command
               (Default) = app.exe %1
```

Esto registra la aplicación y la convierte en la aplicación predeterminada para el verbo de vista previa de un archivo. jpg. También se requiere lo siguiente.

**HKEY \_ Clases \_ root** \\ **. jpg** \( predeterminado) = Application. JPEG

## <a name="registering-for-the-edit-verb"></a>Registrando el verbo de edición

Esto registra una aplicación para el verbo Edit y la convierte en la nueva aplicación predeterminada para editar una imagen. La aplicación registrada debe asumir la funcionalidad de edición de la aplicación predeterminada existente en el momento de la instalación y volver a instalarla como controlador en el momento de la desinstalación. Esto puede lograrse registrando la nueva aplicación en la lista de asociaciones más baja que la aplicación predeterminada. La aplicación predeterminada se registra aquí:

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      image
         shell
            edit
               command
                  (Default) = app.exe %1
```

La nueva aplicación debe registrarse aquí:

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         edit
            command
               (Default) = app.exe %1
```

## <a name="registering-for-the-slideshow-verb"></a>Registro del verbo de presentación de diapositivas

A partir de Windows Vista, una aplicación también puede registrar el verbo de la **presentación de diapositivas** . Las aplicaciones que implementan una presentación de diapositivas se pueden registrar para que se invoquen cuando se elige el verbo de presentación. Este registro se realiza exactamente de la misma manera que se explicó para el verbo de vista previa anterior. Se recomienda encarecidamente que las aplicaciones implementen el formulario DropTarget del verbo. De este modo, se puede pasar un conjunto completo de elementos. La implementación de DropTarget se registra como se muestra aquí:

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         slideshow
            DropTarget
               CLSID = {CLSID of the implementation}
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a las asociaciones de archivos](/windows/desktop/shell/fa-intro)
</dt> <dt>

[Acerca de GDI+](../gdiplus/-gdiplus-about-gdi--about.md)
</dt> </dl>

 

 