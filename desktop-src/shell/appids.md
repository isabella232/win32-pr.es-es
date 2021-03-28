---
description: Los identificadores de modelo de usuario de la aplicación (AppUserModelIDs) se usan en gran medida en la barra de tareas de Windows 7 y sistemas posteriores para asociar procesos, archivos y ventanas a una aplicación determinada.
ms.assetid: ebce2d99-6f20-4545-9f12-d79cd8d0828f
title: Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b79f0bdd7fb5e6c4d5c41caa3cd6be3f4fb57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540579"
---
# <a name="application-user-model-ids-appusermodelids"></a>Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)

Los identificadores de modelo de usuario de la aplicación (AppUserModelIDs) se usan en gran medida en la barra de tareas de Windows 7 y sistemas posteriores para asociar procesos, archivos y ventanas a una aplicación determinada. En algunos casos, es suficiente confiar en el AppUserModelID interno asignado a un proceso por el sistema. Sin embargo, una aplicación que posee varios procesos o una aplicación que se ejecuta en un proceso de host puede tener que identificarse explícitamente para que pueda agrupar las ventanas dispares de otro modo en un solo botón de la barra de tareas y controlar el contenido de la Jump List de esa aplicación.

-   [Definido por la aplicación y System-Defined AppUserModelIDs](#application-defined-and-system-defined-appusermodelids)
-   [Cómo formar un Application-Defined AppUserModelID](#how-to-form-an-application-defined-appusermodelid)
-   [Dónde asignar un AppUserModelID](#where-to-assign-an-appusermodelid)
-   [Registro de una aplicación como un proceso de host](#registering-an-application-as-a-host-process)
-   [Listas de exclusión para el anclaje de la barra de tareas y listas recientes/frecuentes](#exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists)
-   [Temas relacionados](#related-topics)

## <a name="application-defined-and-system-defined-appusermodelids"></a>Application-Defined y System-Defined AppUserModelIDs

Algunas aplicaciones no declaran un AppUserModelID explícito. Son opcionales. En ese caso, el sistema utiliza una serie de heurística para asignar un AppUserModelID interno. Sin embargo, hay una ventaja de rendimiento para evitar esos cálculos y un AppUserModelID explícito es la única manera de garantizar una experiencia de usuario exacta. Por lo tanto, se recomienda establecer un identificador explícito. Las aplicaciones no pueden recuperar un AppUserModelID asignado por el sistema.

Si una aplicación utiliza un AppUserModelID explícito, también debe asignar el mismo AppUserModelID a todas las ventanas o procesos, accesos directos y asociaciones de archivo en ejecución. También debe usar ese AppUserModelID al personalizar su Jump List a través de [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)y en cualquier llamada a [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).

> [!Note]  
> Si las aplicaciones no tienen un AppUserModelID explícito, deben llamar a los métodos [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations), [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)y [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist) , así como a [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) desde dentro de la aplicación. Si se llama a esos métodos desde otro proceso, como un instalador o un desinstalador, el sistema no puede generar el AppUserModelID correcto y esas llamadas no tendrán ningún efecto.

 

Los siguientes elementos describen escenarios comunes que requieren un AppUserModelID explícito. También señalan casos en los que se deben usar varios AppUserModelIDs explícitos.

-   Un único archivo ejecutable con una interfaz de usuario con varios modos que se muestran al usuario como aplicaciones independientes deben asignar AppUserModelIDs diferentes a cada modo. Por ejemplo, una parte de una aplicación que los usuarios ven como una experiencia independiente que puede anclar e iniciar desde la barra de tareas por separado del resto de la aplicación debe tener su propio AppUserModelID, independiente de la experiencia principal.
-   Varios accesos directos con argumentos diferentes que conducen a lo que el usuario ve como la misma aplicación deben usar un AppUserModelID para todos los métodos abreviados. Por ejemplo, Windows Internet Explorer tiene distintos métodos abreviados para distintos modos (como el inicio sin complementos), pero todos deben aparecer para el usuario como una única instancia de Internet Explorer.
-   Un ejecutable que actúa como un proceso de host y que ejecuta el contenido de destino, ya que una aplicación debe [registrarse como una aplicación host](#registering-an-application-as-a-host-process), después de la cual puede asignar AppUserModelIDs diferentes a cada experiencia percibida que hospeda. Como alternativa, el proceso de host puede permitir que el programa hospedado establezca su AppUserModelIDs. En cualquier caso, el proceso de host debe mantener un registro del origen de AppUserModelIDs, ya sea en sí mismo o en la aplicación hospedada. En este caso, no hay ninguna experiencia de usuario principal del proceso de host sin el contenido de destino. Algunos ejemplos son las aplicaciones remotas integradas de Windows (raíl), el tiempo de ejecución de Java, RunDLL32.exe o DLLHost.exe.

    En el caso de las aplicaciones hospedadas existentes, el sistema intenta identificar experiencias individuales, pero las aplicaciones nuevas deben usar AppUserModelIDs explícitas para garantizar la experiencia del usuario prevista.

-   Los procesos cooperativos o encadenados que al usuario forman parte de la misma aplicación deben tener el mismo AppUserModelID aplicado a cada proceso. Entre los ejemplos se incluyen juegos con un proceso de iniciador (encadenado) y Microsoft Windows Media Player, que tiene una experiencia de primera ejecución y configuración que se ejecuta en un proceso y la aplicación principal que se ejecuta en otro proceso (cooperativo).
-   Una extensión de espacio de nombres de Shell que actúa como una aplicación independiente para más que examinar y administrar contenido en el explorador de Windows debe asignar un AppUserModelID en sus propiedades de carpeta. Un ejemplo es el panel de control.
-   En un entorno de virtualización, como un marco de implementación, el entorno de virtualización debe asignar AppUserModelIDs diferentes a cada aplicación que administra. En estos casos, un iniciador de aplicaciones utiliza un proceso intermediario para configurar el entorno y, a continuación, entrega la operación a un proceso diferente para ejecutar la aplicación. Tenga en cuenta que esto hace que el sistema no pueda relacionar el proceso de destino en ejecución de nuevo con el acceso directo porque el acceso directo apunta al proceso intermediario.

    Si alguna aplicación tiene varias ventanas, accesos directos o procesos, el entorno de virtualización también debe aplicar a cada uno de esos elementos.

    Un ejemplo de esta situación es el marco de trabajo ClickOnce, que asigna correctamente AppUserModelIDs en nombre de las aplicaciones que administra. Como en todos estos entornos, las aplicaciones implementadas y administradas por ClickOnce no deben asignar AppUserModelIDs explícitos, ya que, al hacerlo, se producirá un conflicto con la AppUserModelIDs asignada por ClickOnce y se producirán resultados inesperados.

## <a name="how-to-form-an-application-defined-appusermodelid"></a>Cómo formar un Application-Defined AppUserModelID

Una aplicación debe proporcionar su AppUserModelID en el formato siguiente. No puede tener más de 128 caracteres y no puede contener espacios. Cada sección debe tener mayúsculas y minúsculas Pascal.

`CompanyName.ProductName.SubProduct.VersionInformation`

`CompanyName` y `ProductName` deben usarse siempre, mientras que `SubProduct` las `VersionInformation` partes y son opcionales y dependen de los requisitos de la aplicación. `SubProduct` permite que una aplicación principal que consta de varias subaplicacións proporcione un botón de la barra de tareas independiente para cada subaplicación y sus ventanas asociadas. `VersionInformation` permite que dos versiones de una aplicación coexistan mientras se vean como entidades discretas. Si una aplicación no está diseñada para usarse de esta manera, `VersionInformation` se debe omitir para que una versión actualizada pueda usar el mismo AppUserModelID que la versión que se reemplazó.

## <a name="where-to-assign-an-appusermodelid"></a>Dónde asignar un AppUserModelID

Cuando una aplicación usa uno o más AppUserModelIDs explícitos, debe aplicar esos AppUserModelIDs en las siguientes ubicaciones y situaciones:

-   En la propiedad [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) del archivo de acceso directo de la aplicación. Un acceso directo (como un [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka), CLSID \_ ShellLink o un archivo. lnk) admite propiedades a través de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) y otros mecanismos de configuración de propiedades que se usan en todo el shell. Esto permite que la barra de tareas identifique el acceso directo adecuado al pin y garantiza que las ventanas que pertenecen al proceso están asociadas correctamente a ese botón de la barra de tareas.
    > [!Note]  
    > La propiedad [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) se debe aplicar a un acceso directo cuando se crea el acceso directo. Al usar el Microsoft Windows Installer (MSI) para instalar la aplicación, la tabla [MsiShortcutProperty](../msi/msishortcutproperty-table.md) permite aplicar el AppUserModelID al acceso directo cuando se crea durante la instalación.

     

-   Como propiedad de cualquiera de las ventanas de la aplicación en ejecución. Se puede establecer de una de estas dos maneras:

    1.  Si varias ventanas que pertenecen a un proceso requieren AppUserModelIDs diferentes para controlar la agrupación de la barra de tareas, use [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)) para recuperar el almacén de propiedades de la ventana y establecer el valor de AppUserModelID como una propiedad de ventana.
    2.  Si todas las ventanas del proceso usan el mismo AppUserModelID, establezca el AppUserModelID en el proceso a través de [**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid). Una aplicación debe llamar a **SetCurrentProcessExplicitAppUserModelID** para establecer su AppUserModelID durante la rutina de inicio inicial de la aplicación antes de que la aplicación presente una interfaz de usuario, realice cualquier manipulación de las listas de accesos directos o haga (o haga que el sistema realice) cualquier llamada a [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).

    Un AppUserModelID de nivel de ventana invalida un AppUserModelID de nivel de proceso.

    Cuando una aplicación establece un AppUserModelID explícito en el nivel de ventana, la aplicación puede proporcionar los detalles de su comando de reinicio para el botón de la barra de tareas. Para proporcionar esa información, se usan las siguientes propiedades:

    -   [System. AppUserModel. RelaunchCommand](../properties/props-system-appusermodel-relaunchcommand.md)
    -   [System. AppUserModel. RelaunchDisplayNameResource](../properties/props-system-appusermodel-relaunchdisplaynameresource.md)
    -   [System. AppUserModel. RelaunchIconResource](../properties/props-system-appusermodel-relaunchiconresource.md)

    > [!Note]  
    > Si existe un acceso directo para iniciar la aplicación, una aplicación debe aplicar el AppUserModelID como una propiedad del acceso directo en lugar de usar las propiedades de reinicio. En ese caso, se usan la línea de comandos, el icono y el texto del acceso directo para proporcionar la misma información que las propiedades de reinicio.

     

    Un AppUserModelID explícito de nivel de ventana también puede usar la propiedad [System. AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) para especificar que no debe estar disponible para el anclaje o el reinicio.

-   En una llamada a Customize o Update ([**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)), recupere ([**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)) o borre ([**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)) la Jump List de la aplicación.
-   En el registro de Asociación de archivos (a través de su [ProgID](fa-progids.md)) si la aplicación usa las listas de destino **frecuentes** o **recientes** generadas automáticamente por el sistema. [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)hace referencia a esta información de asociación. Esta información también se usa al agregar destinos de [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) a las listas de saltos personalizadas a través de [**ICustomDestinationList:: AppendCategory**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory).
-   En cualquier llamada, la aplicación realiza directamente en [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Si la aplicación depende del cuadro de diálogo de archivo común para realizar llamadas a **SHAddToRecentDocs** en su nombre, esas llamadas pueden deducir el valor de appusermodelid explícito solo si se ha establecido el appusermodelid para todo el proceso. Si la aplicación establece AppUserModelIDs en su Windows en lugar de en el proceso, la aplicación debe realizar todas las llamadas a **SHAddToRecentDocs** , con su AppUserModelID explícito, y evitar que el cuadro de diálogo de archivo común realice sus propias llamadas. Esto se debe hacer cada vez que se abre un elemento, para asegurarse de que las secciones **recientes** o **frecuentes** de la Jump List de la aplicación son precisas.

Los siguientes elementos describen escenarios comunes y dónde aplicar AppUserModelIDs explícitas en esos escenarios.

-   Cuando un único proceso contiene varias aplicaciones, use [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar el almacén de propiedades de la ventana y establezca el valor de AppUserModelID como una propiedad de ventana.
-   Cuando una aplicación usa varios procesos, aplique el AppUserModelID a cada proceso. El uso del mismo AppUserModelID en cada proceso depende de si desea que cada proceso aparezca como parte de la aplicación principal o como entidades individuales.
-   Para separar ciertas ventanas de un conjunto en el mismo proceso, utilice el almacén de propiedades de la ventana para aplicar un solo AppUserModelID a las ventanas que desee separar y, a continuación, aplique un AppUserModelID diferente al proceso. Cualquier ventana de ese proceso que no se etiquete explícitamente con el nivel de ventana de AppUserModelID hereda el AppUserModelID del proceso.
-   Si un tipo de archivo está asociado a una aplicación, asigne el AppUserModelID en el registro de [ProgID](fa-progids.md) del tipo de archivo. Si un único archivo ejecutable se inicia en modos diferentes que se muestran al usuario como aplicaciones distintas, se requiere un AppUserModelID independiente para cada modo. En ese caso, debe haber varios registros ProgID para el tipo de archivo, cada uno con un AppUserModelID diferente.
-   Cuando hay varias ubicaciones de accesos directos desde las que un usuario puede iniciar una aplicación (en el menú **Inicio** , en el escritorio o en cualquier otro lugar), recupere el almacén de propiedades del acceso directo para aplicar un solo AppUserModelID a todos los accesos directos como propiedades de acceso directo.
-   Cuando una aplicación realiza una llamada explícita a [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) , utilice el AppUserModelID en la llamada. Cuando se usa el cuadro de diálogo de archivo común para abrir o guardar archivos, el cuadro de diálogo llama a **SHAddToRecentDocs** en nombre de la aplicación. Esa llamada puede inferir el AppUserModelID explícito del proceso. Sin embargo, si se aplica un AppUserModelID explícito como una propiedad de ventana, el cuadro de diálogo de archivo común no puede determinar el AppUserModelID correcto. En ese caso, la propia aplicación debe llamar explícitamente a **SHAddToRecentDocs** y proporcionarle el AppUserModelID correcto. Además, la aplicación debe impedir que el cuadro de diálogo de archivo común llame a **SHAddToRecentDocs** en su nombre estableciendo la marca de FOS \_ DONTADDTORECENT en el método **GetOptions** de [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) o [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog).

## <a name="registering-an-application-as-a-host-process"></a>Registro de una aplicación como un proceso de host

Una aplicación puede establecer la entrada del registro IsHostApp para que el proceso de ese ejecutable se considere como un proceso de host por parte de la barra de tareas. Esto afecta a sus entradas de agrupación y Jump List predeterminadas.

En el ejemplo siguiente se muestra la entrada del registro requerida. Tenga en cuenta que no se asigna un valor a la entrada. su presencia es todo lo que se necesita. Es un valor de REG \_ null.

```
HKEY_CLASSES_ROOT
   Applications
      example.exe
         IsHostApp
```

Si el propio proceso o el archivo de acceso directo que se usa para iniciar el proceso tiene un AppUserModelID explícito, se omite la lista de procesos de host y la barra de tareas trata la aplicación como una aplicación normal. Las ventanas que se ejecutan en la aplicación se agrupan en un solo botón de la barra de tareas y la aplicación se puede anclar a la barra de tareas.

Si solo se conoce el nombre del archivo ejecutable del proceso en ejecución, sin un AppUserModelID explícito y ese ejecutable está en la lista de procesos de host, cada instancia del proceso se trata como una entidad independiente para la agrupación de la barra de tareas. El botón de la barra de tareas asociado a cualquier instancia específica del proceso no muestra una opción de anclar/desanclar o un icono de inicio para una nueva instancia del proceso. El proceso tampoco es válido para su inclusión en la lista de uso más frecuente (MFU) del menú **Inicio** . Sin embargo, si el proceso se ha iniciado a través de un acceso directo que contiene argumentos de inicio (normalmente el contenido de destino que se va a hospedar como "aplicación"), el sistema puede determinar la identidad y se puede anclar y reiniciar la aplicación.

## <a name="exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists"></a>Listas de exclusión para el anclaje de la barra de tareas y listas recientes/frecuentes

Las aplicaciones, los procesos y las ventanas pueden optar por dejar de estar disponibles para el anclaje en la barra de tareas o para su inclusión en la lista de MFU del menú **Inicio** . Existen tres mecanismos para lograr esto:

1.  Agregue la entrada NoStartPage al registro de la aplicación como se muestra aquí:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    Se omiten los datos asociados a la entrada NoStartPage. Solo se requiere la presencia de la entrada. Por lo tanto, el tipo ideal para NoStartPage es REG \_ None.

    Tenga en cuenta que cualquier uso de AppUserModelID explícito invalida la entrada NoStartPage. Si se aplica un AppUserModelID explícito a un acceso directo, proceso o ventana, se convierte en anclable y es válido para la lista de MFU del menú **Inicio** .

2.  Establezca la propiedad [System. AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) en Windows y los métodos abreviados. Esta propiedad se debe establecer en una ventana antes de la propiedad [PKEY \_ AppUserModel \_ ID](../properties/props-system-appusermodel-id.md) .
3.  Agregue un AppUserModelID explícito como valor en la siguiente subclave del registro, como se muestra aquí:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    Cada entrada es un \_ valor de reg null con el nombre de AppUserModelID. Cualquier AppUserModelID que se encuentre en esta lista no es anclable y no es válido para su inclusión en la lista de MFU del menú **Inicio** .

Tenga en cuenta que determinados archivos ejecutables, así como accesos directos que contienen determinadas cadenas en su nombre, se excluyen automáticamente del anclaje y la inclusión en la lista de MFU.

> [!Note]  
> Esta exclusión automática se puede invalidar mediante la aplicación de un AppUserModelID explícito.

 

Si alguna de las siguientes cadenas, con independencia del caso, se incluye en el nombre de acceso directo, el programa no se muestra anclado y no se muestra en la lista de elementos usados con mayor frecuencia (no aplicable a Windows 10):

-   Documentación
-   Ayuda
-   Instalar
-   Más información
-   Léame
-   Leer primero
-   Léame
-   Quitar
-   Configurar
-   Soporte técnico
-   Novedades

La siguiente lista de programas no es anclable y se excluyen de la lista de usados con mayor frecuencia.

-   Applaunch.exe
-   Control.exe
-   Dfsvc.exe
-   Dllhost.exe
-   Guestmodemsg.exe
-   Hh.exe
-   Install.exe
-   Isuninst.exe
-   Lnkstub.exe
-   Mmc.exe
-   Mshta.exe
-   Msiexec.exe
-   Msoobe.exe
-   Rundll32.exe
-   Setup.exe
-   St5unst.exe
-   Unwise.exe
-   Unwise32.exe
-   Werfault.exe
-   Winhlp32.exe
-   Wlrmdr.exe
-   Wuapp.exe

Las listas anteriores se almacenan en los siguientes valores del registro.

> [!Note]  
> Las aplicaciones no deben modificar estas listas. Use uno de los métodos de lista de exclusión enumerados anteriormente para la misma experiencia.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid)
</dt> <dt>

[**GetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid)
</dt> <dt>

[Extensiones de la barra de tareas](taskbar-extensions.md)
</dt> <dt>

[**ICustomDestinationList::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-setappid)
</dt> <dt>

[**IApplicationDocumentLists::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-setappid)
</dt> <dt>

[**IApplicationDestinations::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-setappid)
</dt> <dt>

[**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> </dl>

 

 
