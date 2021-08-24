---
description: Panel de control que se implementan en un archivo DLL que exporta la función CPlApplet tienen requisitos de registro diferentes que .exe archivos.
title: Registro de elementos Panel de control DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25fffb3b06f93640c5ca8623fb24ffb53c6fd3ecae0b9e23cabafacdceba8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593195"
---
# <a name="how-to-register-dll-control-panel-items"></a>Registro de elementos Panel de control DLL

> [!Note]  
> Las directrices de implementación actuales Panel de control los nuevos elementos deben implementarse como archivos .exe en lugar de .cpl archivos. La siguiente información se incluye principalmente para fines heredados.

 

Panel de control que se implementan en un archivo DLL que exporta la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) tienen requisitos de registro diferentes a .exe archivos. A Windows XP, se deben instalar nuevos archivos DLL de Panel de control en la carpeta de la aplicación asociada en la carpeta Archivos de programa. No es necesario registrar los elementos almacenados en el directorio System32 con una .cpl extensión de almacenamiento. se muestran automáticamente en el Panel de control. Todos los Panel de control que usan **CPlApplet** deben registrarse de una de estas dos maneras:

-   Si el elemento Panel de control va a estar disponible para todos los usuarios, registre la ruta de acceso por equipo agregando un valor **REG \_ EXPAND \_ SZ** a la subclave **HKEY LOCAL \_ \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Panel de control** \\ **Cpls,** establecida en la ruta de acceso dll.
-   Si el Panel de control elemento va a estar disponible por usuario, use **HKEY \_ CURRENT \_ USER** como clave raíz en lugar de **HKEY \_ LOCAL \_ MACHINE**.

En los dos ejemplos siguientes se registra *el elemento Panel de control MyCplApp.* El archivo DLL se denomina MyCpl.cpl y se encuentra en el *directorio de la aplicación \\ MyCorp MyApp.* En este primer ejemplo se muestra el registro por equipo.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

Agregue esta información al Registro para registrar la existencia del .cpl archivo.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Cpls
                     MyCpl = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl
```

### <a name="step-2"></a>Paso 2:

**Windows Vista y versiones posteriores:** Agregue esta información adicional al Registro para proporcionar un GUID para el Panel de control elemento.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.AppId
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = {A newly generated GUID}
```

Al generar un GUID para identificar de forma Panel de control elemento, puede agregar vínculos de tarea al Panel de control. Sin este GUID, no hay ninguna manera de que los vínculos de tarea se asocie al elemento Panel de control trabajo. Vea [Creating Searchable Task Links for a Panel de control Item](creating-searchable-task-links.md).

### <a name="step-3"></a>Paso 3:

**Windows Vista y versiones posteriores:** Agregue la siguiente información al Registro para crear un nombre canónico para el elemento.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ApplicationName
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] MyCorporation.MyCpl
```

Al agregar un nombre canónico, los usuarios pueden iniciar el Panel de control desde una línea de comandos si `control.exe /name MyCorporation.MyCpl` escriben . Esto también permite cambiar una implementación de un archivo .cpl a un archivo .exe más adelante, sin necesidad de llamar a programas para realizar cambios, ya que pueden seguir abriendo el elemento a través de su nombre canónico. Para obtener más información sobre los nombres canónicos, vea [Executing Panel de control Items](executing-control-panel-items.md).

### <a name="step-4"></a>Paso 4:

**Windows Vista y versiones posteriores:** Agregue la siguiente información al Registro para asignar un elemento Panel de control a una o varias categorías.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.Category
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

**Windows XP:** Agregue la siguiente información al Registro para asignar un elemento Panel de control a una o varias categorías.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     {305CA226-D286-468e-B848-2B2E8E697B74} 2
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

En este ejemplo se asigna el elemento a la categoría 3, que es Red e Internet. Para agregar un elemento a varias categorías, proporcione la lista como un valor REG SZ separado por \_ comas, como "3,8". Los valores se pueden proporcionar como decimal o hexadecimal. Tenga en cuenta que la capacidad de agregar un elemento a varias categorías solo es posible en Windows XP Service Pack 2 (SP2) y versiones posteriores. Consulte [Asignación de Panel de control categorías para](assigning-control-panel-categories.md) todos los valores posibles.

### <a name="step-5"></a>Paso 5:

**Windows Vista y versiones posteriores:** Agregue la siguiente información al Registro para crear y apuntar a un archivo XML que contiene vínculos de tarea para el elemento. El valor debe ser una ruta de acceso REG SZ como se muestra aquí o un identificador de módulo y recurso (por ejemplo, "C: Archivos de programa \_ \\ \\ \\ MyCorp MyAppMyApp.exe,-31") si es un recurso \\ incrustado. La ubicación del archivo XML debe especificarse completamente. No puede usar una variable de entorno como %ProgramFiles%.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.TasksFileUrl
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] C:\ProgramFiles\MyCorp\MyApp\MyTasks.xml
```

Para obtener más información sobre los vínculos de tareas y cómo crear el archivo XML para contenerlos, vea [Creating Searchable Task Links for a Panel de control Item](creating-searchable-task-links.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de Panel de control elementos](registering-control-panel-items.md)
</dt> <dt>

[Cómo registrar elementos ejecutables Panel de control aplicación](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
