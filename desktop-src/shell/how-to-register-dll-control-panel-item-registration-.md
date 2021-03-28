---
description: Los elementos del panel de control que se implementan en un archivo DLL que exporta la función CPlApplet tienen distintos requisitos de registro que los archivos. exe.
title: Cómo registrar elementos del panel de control DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b82225dcb40487c60210752b2c15af23f95bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813699"
---
# <a name="how-to-register-dll-control-panel-items"></a>Cómo registrar elementos del panel de control DLL

> [!Note]  
> Instrucciones de implementación actuales indican que los nuevos elementos del panel de control deben implementarse como archivos. exe en lugar de como archivos. cpl. La siguiente información se incluye principalmente para fines heredados.

 

Los elementos del panel de control que se implementan en un archivo DLL que exporta la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) tienen distintos requisitos de registro que los archivos. exe. A partir de Windows XP, los nuevos archivos dll de los elementos del panel de control deben instalarse en la carpeta de la aplicación asociada en la carpeta archivos de programa. No es necesario registrar los elementos que se almacenan en el directorio system32 con una extensión. cpl; se muestran automáticamente en el panel de control. Todos los demás elementos del panel de control que usan **CPlApplet** deben estar registrados de una de estas dos maneras:

-   Si el elemento del panel de control va a estar disponible para todos los usuarios, registre la ruta de acceso por equipo agregando un valor de **reg \_ Expand \_ SZ** a la subclave **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **control panel** \\ **CPLS** , que se establece en la ruta de acceso del archivo dll.
-   Si el elemento del panel de control va a estar disponible por usuario, use **HKEY \_ Current \_ User** como clave raíz en lugar de **HKEY \_ local \_ Machine**.

Los dos ejemplos siguientes registran el elemento del panel de control *MyCplApp* . El archivo DLL se denomina MyCpl.cpl y se encuentra en el directorio de aplicación de *MiOrg \\ MyApp* . En este primer ejemplo se muestra el registro por equipo.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Agregue esta información al registro para registrar la existencia del archivo. cpl.

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

**Windows Vista y versiones posteriores:** Agregue esta información adicional al registro para proporcionar un GUID para el elemento del panel de control.

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

Al generar un GUID para identificar de forma única el elemento del panel de control, puede Agregar vínculos de tarea al panel de control. Sin este GUID, no hay ninguna manera de asociar los vínculos de tarea con el elemento del panel de control. Consulte [crear vínculos de tarea que se pueden buscar para un elemento del panel de control](creating-searchable-task-links.md).

### <a name="step-3"></a>Paso 3:

**Windows Vista y versiones posteriores:** Agregue la siguiente información al registro para crear un nombre canónico para el elemento.

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

Al agregar un nombre canónico, los usuarios pueden iniciar el elemento del panel de control desde una línea de comandos escribiendo `control.exe /name MyCorporation.MyCpl` . Esto también permite cambiar una implementación de un archivo. cpl a un archivo. exe más adelante, sin necesidad de que los programas que llaman realicen cambios, ya que pueden continuar abriendo el elemento a través de su nombre canónico. Para obtener más información sobre los nombres canónicos, vea [Ejecutar elementos del panel de control](executing-control-panel-items.md).

### <a name="step-4"></a>Paso 4:

**Windows Vista y versiones posteriores:** Agregue la siguiente información al registro para asignar un elemento del panel de control a una o varias categorías.

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

**Windows XP:** Agregue la siguiente información al registro para asignar un elemento del panel de control a una o varias categorías.

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

En este ejemplo se asigna el elemento a la categoría 3, que es red e Internet. Para agregar un elemento a varias categorías, proporcione la lista como un valor de REG \_ SZ separado por comas, como "3, 8". Los valores se pueden proporcionar en formato decimal o hexadecimal. Tenga en cuenta que la capacidad de agregar un elemento a varias categorías solo es posible en Windows XP Service Pack 2 (SP2) y versiones posteriores. Vea [asignar categorías del panel de control](assigning-control-panel-categories.md) para todos los valores posibles.

### <a name="step-5"></a>Paso 5:

**Windows Vista y versiones posteriores:** Agregue la siguiente información al registro para crear y apuntar a un archivo XML que contenga vínculos de tareas para el elemento. El valor debe ser una \_ ruta de acceso reg SZ como se muestra aquí o un identificador de módulo y de recurso (por ejemplo, "C: \\ archivos de programa \\ Corp \\ \\MyApp.exe,-31") si es un recurso incrustado. La ubicación del archivo XML debe especificarse por completo. No puede usar una variable de entorno como% ProgramFiles%.

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

Para obtener más información sobre los vínculos de tarea y cómo crear el archivo XML que los contiene, vea [crear vínculos de tarea que se pueden buscar para un elemento del panel de control](creating-searchable-task-links.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registrar elementos del panel de control](registering-control-panel-items.md)
</dt> <dt>

[Cómo registrar elementos del panel de control ejecutable](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
