---
description: En el caso de los elementos del panel de control que se implementan como archivos. exe, no se requiere ninguna exportación especial ni control de mensajes. Cualquier archivo. exe se puede registrar como un objeto de comando para que aparezca con un punto de entrada en la carpeta del panel de control.
title: Cómo registrar elementos del panel de control ejecutable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778bac10fea661f73c0967401a7c708ebf6b8273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082634"
---
# <a name="how-to-register-executable-control-panel-items"></a>Cómo registrar elementos del panel de control ejecutable

En el caso de los elementos del panel de control que se implementan como archivos. exe, no se requiere ninguna exportación especial ni control de mensajes. Cualquier archivo. exe se puede registrar como un objeto de comando para que aparezca con un punto de entrada en la carpeta del panel de control.

Aquí se usa un ejemplo para mostrar los requisitos de registro. En el ejemplo se muestra cómo registrar un elemento del panel de control denominado **My Settings** como un objeto Command para que aparezca en la ventana Panel de control. La ventana **My Settings (mi configuración** ) también aparece cuando `MyApp.exe /settings` se ejecuta el comando.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Genere un GUID para el elemento del panel de control. El GUID identifica de forma única el elemento del panel de control. En este ejemplo, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` es el GUID del elemento del panel de control.

### <a name="step-2"></a>Paso 2:

Con el GUID como nombre, agregue una subclave al registro como se indica a continuación.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ControlPanel
                     NameSpace
                        {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
                           (Default) = My Settings
```

Los datos de la entrada predeterminada son simplemente el \_ nombre de reg SZ del elemento del panel de control. La entrada predeterminada puede ser útil para identificar la entrada de GUID, pero es opcional.

### <a name="step-3"></a>Paso 3:

Con el GUID como nombre, agregue una subclave y sus entradas al registro como se indica a continuación.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         (Default) = My Settings
         LocalizedString = @%ProgramFiles%\MyCorp\MyApp.exe,-9
         InfoTip = @%ProgramFiles%\MyCorp\MyApp.exe,-5
         System.ApplicationName = MyCorporation.MySettings
         System.ControlPanel.Category = 1,8
         System.Software.TasksFileUrl = %ProgramFiles%\MyCorp\MyApp\MyTaskLinks.xml
```

-   **Default**. REG \_ . Nombre para mostrar del elemento del panel de control.
-   **LocalizedString**. Opcional. REG \_ SZ o REG \_ Expand \_ . El nombre del módulo y el identificador de la tabla de cadenas del nombre localizado del elemento del panel de control. El formato es un signo "arroba" (@) seguido del nombre del archivo. exe o. dll que contiene la tabla de cadenas de la interfaz de usuario multilingüe (MUI). Las variables de entorno se pueden usar como sustituto de una parte de la ruta de acceso. La ruta de acceso y el nombre de archivo van seguidos de una coma (,) y un guión (-), seguido del identificador de la tabla de cadenas.

    Si el módulo no tiene una tabla de cadenas, esta entrada puede ser simplemente la cadena del nombre para mostrar. Si solo usa la cadena de nombre para mostrar en lugar de una tabla de cadenas, el nombre no se ajusta al idioma para mostrar actual.

-   Recuadro informativo. REG \_ SZ o REG \_ Expand \_ . Descripción del elemento del panel de control. Esta información se muestra en un recuadro informativo que se muestra cuando se mantiene el mouse sobre el icono del elemento. La sintaxis es la misma que la que se usa para LocalizedString, incluida la opción de simplemente proporcionar una cadena en lugar de una referencia de tabla de cadenas.
-   **System. ApplicationName**. REG \_ . El nombre canónico del elemento. El comando del formulario `control.exe /name System.ApplicationName` abre el elemento; por ejemplo, `control.exe /name MyCorporation.MySettings` . Vea [Ejecutar elementos del panel de control](executing-control-panel-items.md) para obtener más información sobre el uso de Control.exe.
-   **System. ControlPanel. Category**. REG \_ . Valor que declara las categorías del panel de control donde aparece el elemento. Varias categorías se separan mediante comas. En el caso del ejemplo anterior, la entrada especifica que el elemento **My Settings** debe aparecer en las categorías **Appearance y personalización** y **programas** . Vea [asignar categorías del panel de control](assigning-control-panel-categories.md) para posibles valores de categoría.
-   **System. software. TasksFileUrl**. REG \_ SZ o REG \_ Expand \_ . Ruta de acceso del archivo XML que define los [vínculos de tarea](creating-searchable-task-links.md). Puede ser una ruta de acceso de archivo directa, tal como se muestra en el ejemplo, o un recurso incrustado especificado como un nombre de módulo y un identificador de recurso como "% ProgramFiles% \\ Corp \\ MyApp \\MyApp.exe,-31".

### <a name="step-4"></a>Paso 4:

En la misma subclave GUID, agregue la siguiente subclave al registro para proporcionar la ruta de acceso del archivo que contiene el icono y el identificador de recurso de la imagen dentro de ese archivo.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

Tenga en cuenta que, aunque la sintaxis es similar a las entradas LocalizedString y de la sugerencia que se han descrito anteriormente, no se usa ningún carácter ' @ ' como prefijo en la \_ entrada reg SZ o REG \_ Expand, \_ que especifica la ruta de acceso.

### <a name="step-5"></a>Paso 5:

Agregue la siguiente información al registro para proporcionar el comando al que llama el sistema cuando el usuario abre el panel de control.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         Shell
            Open
               Command
                  (Default) = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp.exe /Settings
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registrar elementos del panel de control](registering-control-panel-items.md)
</dt> <dt>

[Cómo registrar elementos del panel de control DLL](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



