---
description: Para Panel de control que se implementan como archivos .exe, no se requiere ninguna exportación especial ni control de mensajes. Cualquier .exe archivo se puede registrar como un objeto de comando para que aparezca con un punto de entrada en Panel de control carpeta.
title: Cómo registrar elementos ejecutables Panel de control aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b81e52e18bd2cd1c48d5d260b08844784a5286dd2cd4d9d5ec782a86f624fc42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009435"
---
# <a name="how-to-register-executable-control-panel-items"></a>Cómo registrar elementos ejecutables Panel de control aplicación

Para Panel de control que se implementan como archivos .exe, no se requiere ninguna exportación especial ni control de mensajes. Cualquier .exe archivo se puede registrar como un objeto de comando para que aparezca con un punto de entrada en Panel de control carpeta.

Aquí se usa un ejemplo para mostrar los requisitos de registro. En el ejemplo se muestra cómo registrar un elemento Panel de control denominado **My Configuración** como un objeto de comando para que aparezca en la ventana Panel de control comandos. La **ventana Mi Configuración** también aparece cuando se ejecuta el `MyApp.exe /settings` comando.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

Genere un GUID para el Panel de control elemento. El GUID identifica de forma única el Panel de control elemento. En este ejemplo, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` es el GUID del Panel de control elemento.

### <a name="step-2"></a>Paso 2:

Con el GUID como nombre, agregue una subclave al Registro como se muestra a continuación.

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

Los datos de la entrada Default son simplemente el nombre REG \_ SZ del Panel de control elemento. La entrada Default puede ser útil para identificar la entrada GUID, pero es opcional.

### <a name="step-3"></a>Paso 3:

Con el GUID como nombre, agregue una subclave y sus entradas al Registro como se muestra a continuación.

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

-   **Default**. REG \_ SZ. Nombre para mostrar del Panel de control elemento.
-   **LocalizedString**. Opcional. REG \_ SZ o REG EXPAND \_ \_ SZ. El nombre del módulo y el identificador de la tabla de cadenas del nombre localizado del Panel de control elemento. El formato es un signo "at" (@) seguido del nombre del .exe o .dll que contiene la tabla de cadenas Interfaz de usuario multilingüe (MUI). Las variables de entorno se pueden usar como sustituto de una parte de la ruta de acceso. La ruta de acceso y el nombre de archivo va seguido de una coma (,) y un guión (-), seguido del identificador de la tabla de cadenas.

    Si el módulo no tiene una tabla de cadenas, esta entrada puede ser simplemente la cadena de nombre para mostrar. Si solo usa la cadena de nombre para mostrar en lugar de una tabla de cadenas, el nombre no se ajusta al idioma para mostrar actual.

-   **Información sobre**. REG \_ SZ o REG EXPAND \_ \_ SZ. Descripción del elemento Panel de control. Esta información se muestra en una información sobre información que se muestra cuando el mouse se mantiene sobre el icono del elemento. La sintaxis es la misma que la que se usa para LocalizedString, incluida la opción de simplemente proporcionar una cadena en lugar de una referencia de tabla de cadenas.
-   **System.ApplicationName**. REG \_ SZ. El nombre canónico del elemento. El comando de formulario `control.exe /name System.ApplicationName` abre el elemento; por ejemplo, `control.exe /name MyCorporation.MySettings` . Vea [Executing Panel de control Items (Ejecutar](executing-control-panel-items.md) elementos de Control.exe).
-   **System.ControlPanel.Category**. REG \_ SZ. Valor que declara las categorías Panel de control donde aparece el elemento. Varias categorías están separadas por comas. En el caso del ejemplo anterior, la entrada especifica que el elemento **My Configuración** debe aparecer en las categorías Apariencia y **Personalización** **y Programas.** Vea [Asignación de Panel de control categorías para](assigning-control-panel-categories.md) ver los posibles valores de categoría.
-   **System.Software.TasksFileUrl**. REG \_ SZ o REG EXPAND \_ \_ SZ. Ruta de acceso del archivo XML que define los [vínculos de tarea](creating-searchable-task-links.md). Puede ser una ruta de acceso de archivo directa como se muestra en el ejemplo, o un recurso incrustado especificado como nombre de módulo e identificador de recurso como "%ProgramFiles% \\ MyCorp \\ MyApp \\MyApp.exe,-31".

### <a name="step-4"></a>Paso 4:

En esa misma subclave GUID, agregue la siguiente subclave al Registro para proporcionar la ruta de acceso del archivo que contiene el icono y el identificador de recurso de la imagen dentro de ese archivo.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

Tenga en cuenta que, aunque la sintaxis es similar a las entradas LocalizedString e InfoTip que se han mencionado anteriormente, no se usa ningún carácter '@' como prefijo en la entrada REG SZ o REG EXPAND SZ que especifica la ruta de \_ \_ \_ acceso.

### <a name="step-5"></a>Paso 5:

Agregue la siguiente información al Registro para proporcionar el comando al que llama el sistema cuando el usuario abre el Panel de control.

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

[Registro de Panel de control elementos](registering-control-panel-items.md)
</dt> <dt>

[Cómo registrar elementos Panel de control DLL](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



