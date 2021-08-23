---
title: Reemplazo de la aplicación Windows de imágenes y fax mediante el verbo de vista previa
description: A Windows XP, los usuarios pueden ver, girar, imprimir y acercar imágenes.
ms.assetid: cb08756b-6a5d-424d-ab6d-2e34d180ec4e
keywords:
- Windows Visor de imágenes y fax
- Verbo de vista previa
- procedimientos recomendados, Windows visor de imágenes y fax
- procedimientos recomendados,verbo de versión preliminar
- performance,Windows Visor de imágenes y fax
- performance,Verbo de vista previa
- register,Preview verb
- register,Verbo de presentación
- Verbo de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518e32f7b7bf33db26e534c92cfe2fb46c9a51bc444f04f4881f18fb1fe6c738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608525"
---
# <a name="replacing-the-windows-picture-and-fax-viewer-application-using-the-preview-verb"></a>Reemplazo de la aplicación Windows de imágenes y fax mediante el verbo de vista previa

\[La característica Visor de imágenes y fax solo se admite en Windows XP. \]

A Windows XP, los usuarios pueden ver, girar, imprimir y acercar imágenes. Algunas de estas características se proporcionan a través de Windows Shell y otras a través de la Windows visor de imágenes y faxes. Aunque Windows visor de imágenes y fax proporciona una línea de base excelente de características y es una parte clave de la experiencia de creación de imágenes, si lo decide, puede reemplazarla fácilmente por otra aplicación. Este documento está diseñado para ayudarle a reemplazar eficazmente la aplicación Windows Visor de imágenes y fax sin perder características importantes ni degradar la experiencia del usuario.

-   [Procedimientos recomendados](#best-practices)
    -   [Rendimiento](#performance)
    -   [Características](#features)
    -   [Compatibilidad con formatos](#format-support)
-   [Registro para el verbo de vista previa](#registering-for-the-preview-verb)
-   [Registro para editar verbo](#registering-for-the-edit-verb)
-   [Registro para el verbo de presentación](#registering-for-the-slideshow-verb)
-   [Temas relacionados](#related-topics)

## <a name="best-practices"></a>Prácticas recomendadas

En Windows XP y versiones posteriores, el Shell incluye un verbo que puede usar para permitir que los usuarios obtengan una vista previa de las imágenes. Se denomina Vista *previa.* Este verbo resalta la tarea principal del usuario para las imágenes, que está viendo. Para que esta experiencia funcione bien, la Windows visor de imágenes y fax posee la asociación de vista previa de forma predeterminada.

El Windows de imágenes y fax, o cualquier aplicación propietaria de una asociación de archivos, incluye un elemento que inicia la aplicación de edición del usuario. Dado que el verbo Vista previa solo se usa para obtener una vista previa de las imágenes en lugar de editarlas, la aplicación debe tener cuidado de seguir las recomendaciones de este documento al reclamar esa asociación.

Quiere asegurarse de que una aplicación que edita imágenes todavía pueda asumir el verbo Editar. Por ejemplo, si un usuario tiene Microsoft Picture It. instalado, al hacer doble clic en un archivo .jpg, el equipo debe iniciar Windows aplicación Visor de imágenes y fax. Pero, al hacer clic **en Editar en** la barra de herramientas, el equipo debería iniciar La imagen. con ese .jpg archivo.

Hay tres consideraciones que debe tener en cuenta al reemplazar el visor Windows imagen y fax. Estos son:

-   [Rendimiento](#performance)
-   [Características](#features)
-   [Compatibilidad con formatos](#format-support)

### <a name="performance"></a>Rendimiento

La consideración principal con el rendimiento es la velocidad a la que se cargan las imágenes. Aunque aquí no se proporciona ninguna métrica de rendimiento, debe intentar reemplazar Windows Visor de imágenes y fax por una aplicación que coincida o aumente el rendimiento.

La propia aplicación debe cargarse rápidamente. Uno de los principales problemas que experimentan los usuarios con las aplicaciones que se hace cargo de las asociaciones de imagen es el tiempo de espera mientras se carga la aplicación. Esto suele deber a tener una carga de aplicación de edición eficaz al hacer doble clic en un archivo de imagen, incluso cuando el usuario simplemente desea ver el archivo. Es mejor para el usuario si proporciona opciones que los llevan rápidamente a una aplicación donde pueden editar la imagen solo cuando ese es su deseo.

### <a name="features"></a>Características

Hay un conjunto mínimo de características que la aplicación debe proporcionar al reemplazar la Windows visor de imágenes y fax. Los pasos son los siguientes:



| Característica                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mostrar la imagen en el mejor ajuste             | Esto ofrece al usuario la opción de ver toda la imagen escalada al tamaño donde mejor se ajuste al espacio que se puede ver de la ventana de la aplicación. De esta manera, pueden ver toda la imagen, incluso si está ligeramente degradada al alejarla. Debe ser la configuración predeterminada cada vez que se cargue una imagen que sea mayor que el espacio que se puede ver. De lo contrario, la imagen debe aparecer en su tamaño real. Por ejemplo, una imagen de 64 x 64 píxeles no se debe escalar a un tamaño de 600 x 600 simplemente porque es el tamaño de ventana de la aplicación. |
| Mostrar imagen en tamaño real          | Esto ofrece al usuario la opción de ver toda la imagen en su resolución real. Esto les permite verlo con el tamaño adecuado y desplazarse por la imagen. Esta no debe ser la vista predeterminada a menos que la imagen sea menor que el espacio que se puede ver en la aplicación.                                                                                                                                                                                                                                                              |
| Acercar imagen                    | Esto permite al usuario acercar una parte de la imagen para investigar detalles más finos o simplemente ampliar una imagen pequeña. Esto es similar a mostrar el tamaño real de la imagen, pero permite al usuario controlar la proximidad con la que ve la imagen.                                                                                                                                                                                                                                                                                            |
| Alejar imagen                  | Esto permite al usuario alejar y obtener una vista más amplia. Esto es similar a mostrar la imagen en el mejor de los casos, pero permite al usuario controlar hasta qué punto ve la imagen.                                                                                                                                                                                                                                                                                                                                                          |
| Imagen siguiente                         | Esto permite al usuario ver la siguiente imagen en la lista. Esta lista puede ser todas las imágenes de la carpeta actual o todas las imágenes que el usuario selecciona como parte de una operación de selección múltiple. es decir, cuando hace clic y arrastra para resaltar imágenes o mantiene presionado el botón de control y hace clic en archivos individuales.                                                                                                                                                                                                                       |
| Imagen anterior                     | Esto permite al usuario ver la imagen anterior en la lista.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Girar 90 grados en el sentido de las agujas del reloj        | Esto permite al usuario girar la imagen en el sentido de las agujas del reloj por trimestres. Windows XP guarda automáticamente la imagen cuando la gira para reducir la pérdida de calidad de la imagen. La aplicación también puede girar incrementos más pequeños, pero 90 grados es el estándar como rotación más común para imágenes digitales.                                                                                                                                                                                                                                 |
| Girar 90 grados en sentido contrario a las agujas del reloj | Esto permite al usuario girar la imagen en sentido contrario a las agujas del reloj por trimestres.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Impresión                              | Esto permite al usuario imprimir la imagen que aparece actualmente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Guardar como                            | Esto permite al usuario guardar la imagen en una carpeta especificada.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Eliminar imagen                       | Esto permite al usuario eliminar la imagen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ayuda                               | Esto proporciona al usuario documentación de ayuda relacionada con el uso de la aplicación de visualización.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Propiedades                         | Esto permite al usuario ver o editar las propiedades de la imagen, normalmente la información de archivo de imagen intercambiable (EXIF) almacenada en cada imagen.                                                                                                                                                                                                                                                                                                                                                                                      |
| Editar                               | Esto permite al usuario iniciar su programa de edición preferido registrado para el verbo Editar en la imagen.                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="format-support"></a>Compatibilidad con formatos

Dado que es difícil para una aplicación admitir todas las imágenes diferentes, se recomienda que la aplicación use Windows GDI+ para admitir formatos de imagen. Sin embargo, si decide no usar GDI+, la aplicación solo debe asumir las asociaciones de archivo para las que se ha probado y se sabe que funciona. A continuación, si el usuario necesita ver un formato que no controla, Windows visor de imágenes y faxes todavía puede proporcionar acceso.

Por ejemplo, Windows visor de imágenes y fax proporciona una serie de herramientas para editar anotaciones en imágenes .tiff. A menos que esta funcionalidad esté duplicada en la aplicación, no debe registrar la aplicación para controlar las imágenes .tiff. El principio de conducción debe ser asegurarse de que el usuario no pierde ninguna funcionalidad.

## <a name="registering-for-the-preview-verb"></a>Registro para el verbo de vista previa

El registro de una aplicación para controlar el verbo de vista previa es bastante sencillo. Busque el siguiente valor de la aplicación en el Registro, donde Application.Jpeg representa [](/windows/desktop/shell/default-programs) el nombre de la clave de asociación de archivos de la aplicación (consulte Programas predeterminados para obtener más detalles):

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         open
            command
               (Default) = app.exe %1
```

Cambie el nombre de la **subclave** abierta a "vista previa", como se muestra aquí.

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         preview
            command
               (Default) = app.exe %1
```

Esto registra la aplicación y la convierte en la aplicación predeterminada para el verbo Vista previa de un .jpg archivo. También se requiere lo siguiente.

**HKEY \_ CLASSES \_ ROOT** \\ **.jpg** \( Default) = Application.Jpeg

## <a name="registering-for-the-edit-verb"></a>Registro para editar verbo

Esto registra una aplicación para editar verbo y la convierte en la nueva aplicación predeterminada para editar una imagen. La aplicación registrada debe asumir la funcionalidad de edición de la aplicación predeterminada existente en el momento de la instalación e instalarla de nuevo como controlador en el momento de la desinstalación. Esto se puede lograr mediante el registro de la nueva aplicación en una parte inferior de la lista de asociaciones que la aplicación predeterminada. La aplicación predeterminada se registra aquí:

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

## <a name="registering-for-the-slideshow-verb"></a>Registro para el verbo de presentación

A Windows Vista, una aplicación también puede registrar el verbo de **presentación.** Las aplicaciones que implementan una presentación de diapositivas se pueden registrar para invocarse cuando se elige el verbo Presentación. Este registro se realiza exactamente de la misma manera que se explicó para el verbo de vista previa anterior. Se recomienda encarecidamente que las aplicaciones implementen el formato DropTarget del verbo. De este modo, se les puede pasar un conjunto completo de elementos. La implementación de DropTarget se registra como se muestra aquí:

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

 

 