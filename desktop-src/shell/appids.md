---
description: Los id. de modelo de usuario de aplicación (AppUserModelID) se usan ampliamente en la barra de tareas de Windows 7 y sistemas posteriores para asociar procesos, archivos y ventanas con una aplicación determinada.
ms.assetid: ebce2d99-6f20-4545-9f12-d79cd8d0828f
title: Id. de modelo de usuario de aplicación (AppUserModelIDs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd0835af241a36e4d9c95237890cb63790f7fe9031476dfa8ec21254266ffd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351475"
---
# <a name="application-user-model-ids-appusermodelids"></a>Id. de modelo de usuario de aplicación (AppUserModelIDs)

Los id. de modelo de usuario de aplicación (AppUserModelID) se usan ampliamente en la barra de tareas de Windows 7 y sistemas posteriores para asociar procesos, archivos y ventanas con una aplicación determinada. En algunos casos, es suficiente con basarse en el AppUserModelID interno asignado a un proceso por el sistema. Sin embargo, una aplicación que posee varios procesos o una aplicación que se ejecuta en un proceso host podría tener que identificarse explícitamente para que pueda agrupar sus ventanas distintas en un solo botón de la barra de tareas y controlar el contenido de la aplicación Lista de accesos directos.

-   [Application-Defined and System-Defined AppUserModelIDs](#application-defined-and-system-defined-appusermodelids)
-   [Cómo crear un Application-Defined AppUserModelID](#how-to-form-an-application-defined-appusermodelid)
-   [Dónde asignar un AppUserModelID](#where-to-assign-an-appusermodelid)
-   [Registro de una aplicación como proceso de host](#registering-an-application-as-a-host-process)
-   [Listas de exclusión para anclar la barra de tareas y listas recientes o frecuentes](#exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists)
-   [Temas relacionados](#related-topics)

## <a name="application-defined-and-system-defined-appusermodelids"></a>Application-Defined y System-Defined AppUserModelID

Algunas aplicaciones no declaran un AppUserModelID explícito. Son opcionales. En ese caso, el sistema usa una serie de heurísticas para asignar un AppUserModelID interno. Sin embargo, hay una ventaja de rendimiento al evitar esos cálculos y un AppUserModelID explícito es la única manera de garantizar una experiencia de usuario exacta. Por lo tanto, se recomienda encarecidamente establecer un identificador explícito. Las aplicaciones no pueden recuperar un AppUserModelID asignado por el sistema.

Si una aplicación usa un AppUserModelID explícito, también debe asignar el mismo AppUserModelID a todas las ventanas o procesos en ejecución, accesos directos y asociaciones de archivo. También debe usar ese AppUserModelID al personalizar su Lista de accesos directos a través de [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)y en cualquier llamada a [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).

> [!Note]  
> Si las aplicaciones no tienen un AppUserModelID explícito, deben llamar a los métodos [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations), [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)e [**ICustomDestinationList,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist) así como [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) desde dentro de la aplicación. Si se llama a esos métodos desde otro proceso, como un instalador o un desinstalador, el sistema no puede generar el AppUserModelID correcto y esas llamadas no tendrán ningún efecto.

 

Los elementos siguientes describen escenarios comunes que requieren un AppUserModelID explícito. También señalan los casos en los que se deben usar varios AppUserModelID explícitos.

-   Un único archivo ejecutable con una interfaz de usuario con varios modos que aparecen al usuario como aplicaciones independientes debe asignar diferentes AppUserModelID a cada modo. Por ejemplo, una parte de una aplicación que los usuarios ven como una experiencia independiente que pueden anclar e iniciar desde la barra de tareas por separado del resto de la aplicación debe tener su propio AppUserModelID, independiente de la experiencia principal.
-   Varios accesos directos con argumentos diferentes que conducen a lo que el usuario ve como la misma aplicación deben usar un AppUserModelID para todos los accesos directos. Por ejemplo, Windows Internet Explorer tiene accesos directos diferentes para distintos modos (por ejemplo, iniciar sin complementos), pero todos deben aparecer al usuario como una única instancia Internet Explorer usuario.
-   Un ejecutable que actúa como un proceso de host y ejecuta el contenido de destino como una aplicación debe registrarse como una aplicación host , después de lo cual puede asignar diferentes AppUserModelID [a](#registering-an-application-as-a-host-process)cada experiencia percibida que hospeda. Como alternativa, el proceso de host puede permitir que el programa hospedado establezca sus AppUserModelID. En cualquier caso, el proceso de host debe mantener un registro del origen de AppUserModelIDs, ya sea a sí mismo o a la aplicación hospedada. En este caso, no hay ninguna experiencia de usuario principal del proceso de host sin el contenido de destino. Algunos ejemplos son Windows aplicaciones remotas integradas localmente (RAIL), java runtime, RunDLL32.exe o DLLHost.exe.

    En el caso de las aplicaciones hospedadas existentes, el sistema intenta identificar experiencias individuales, pero las nuevas aplicaciones deben usar AppUserModelID explícitos para garantizar la experiencia de usuario deseada.

-   Los procesos cooperativas o encadenados que forman parte de la misma aplicación deben tener aplicado el mismo AppUserModelID a cada proceso. Algunos ejemplos son los juegos con un proceso de iniciador (encadenado) y Microsoft Reproductor de Windows Media, que tiene una experiencia de primera ejecución o configuración que se ejecuta en un proceso y la aplicación principal que se ejecuta en otro proceso (cooperativa).
-   Una extensión de espacio de nombres de Shell que actúa como una aplicación independiente para algo más que examinar y administrar contenido en Windows Explorer debe asignar un AppUserModelID en sus propiedades de carpeta. Un ejemplo es el Panel de control.
-   En un entorno de virtualización como un marco de implementación, el entorno de virtualización debe asignar diferentes AppUserModelID a cada aplicación que administra. En estos casos, un iniciador de aplicaciones usa un proceso intermedio para configurar el entorno y, a continuación, entrega la operación a un proceso diferente para ejecutar la aplicación. Tenga en cuenta que esto hace que el sistema no pueda relacionar el proceso de destino en ejecución con el acceso directo porque el acceso directo apunta al proceso intermedio.

    Si alguna aplicación tiene varias ventanas, accesos directos o procesos, el AppUserModelID asignado de esa aplicación también se debe aplicar a cada una de esas partes mediante el entorno de virtualización.

    Un ejemplo de esta situación es el marco ClickOnce, que asigna correctamente AppUserModelID en nombre de las aplicaciones que administra. Al igual que en todos estos entornos, las aplicaciones implementadas y administradas por ClickOnce no deben asignar appUserModelID explícitos, ya que si lo hace, entra en conflicto con los AppUserModelID asignados por ClickOnce y conduce a resultados inesperados.

## <a name="how-to-form-an-application-defined-appusermodelid"></a>Cómo crear un Application-Defined AppUserModelID

Una aplicación debe proporcionar su AppUserModelID en el formulario siguiente. No puede tener más de 128 caracteres y no puede contener espacios. Cada sección debe estar en mayúsculas y minúsculas pascal.

`CompanyName.ProductName.SubProduct.VersionInformation`

`CompanyName` y `ProductName` siempre se deben usar, mientras que las partes y son `SubProduct` `VersionInformation` opcionales y dependen de los requisitos de la aplicación. `SubProduct` permite que una aplicación principal que consta de varias subaplicaciones proporcione un botón de barra de tareas independiente para cada subaplicación y sus ventanas asociadas. `VersionInformation` permite que dos versiones de una aplicación coexistan mientras se ven como entidades discretas. Si una aplicación no está pensada para usarse de ese modo, se debe omitir para que una versión actualizada pueda usar el mismo AppUserModelID que la versión que `VersionInformation` reemplazó.

## <a name="where-to-assign-an-appusermodelid"></a>Dónde asignar un AppUserModelID

Cuando una aplicación usa uno o varios AppUserModelID explícitos, debe aplicar esos AppUserModelID en las siguientes ubicaciones y situaciones:

-   En la [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) propiedad del archivo de acceso directo de la aplicación. Un acceso directo (como [**IShellLink,**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka)CLSID ShellLink o un archivo .lnk) admite propiedades a través de IPropertyStore y otros mecanismos de configuración de propiedades que se usan en el \_ Shell. [](/windows/win32/api/propsys/nn-propsys-ipropertystore) Esto permite a la barra de tareas identificar el acceso directo adecuado para anclar y garantiza que las ventanas que pertenecen al proceso están asociadas correctamente a ese botón de la barra de tareas.
    > [!Note]  
    > La [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) propiedad debe aplicarse a un acceso directo cuando se crea ese acceso directo. Cuando se usa Microsoft Windows Installer (MSI) para instalar la aplicación, la tabla [MsiShortcutProperty](../msi/msishortcutproperty-table.md) permite aplicar AppUserModelID al acceso directo cuando se crea durante la instalación.

     

-   Como propiedad de cualquiera de las ventanas en ejecución de la aplicación. Esto se puede establecer de una de estas dos maneras:

    1.  Si las distintas ventanas que pertenecen a un proceso requieren diferentes AppUserModelID para controlar la agrupación de la barra de tareas, use [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)) para recuperar el almacén de propiedades de la ventana y establecer AppUserModelID como una propiedad de ventana.
    2.  Si todas las ventanas del proceso usan el mismo AppUserModelID, establezca AppUserModelID en el proceso a través de [**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid). Una aplicación debe llamar a **SetCurrentProcessExplicitAppUserModelID** para establecer su AppUserModelID durante la rutina de inicio inicial de una aplicación antes de que la aplicación presente cualquier interfaz de usuario, realice cualquier manipulación de sus listas de accesos directos o realice (o haga que el sistema realice) cualquier llamada a [**SHAddToRecentDocs.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)

    Un AppUserModelID de nivel de ventana invalida un AppUserModelID de nivel de proceso.

    Cuando una aplicación establece un AppUserModelID explícito en el nivel de ventana, la aplicación puede proporcionar los detalles de su comando de reinició para su botón de la barra de tareas. Para proporcionar esa información, se usan las siguientes propiedades:

    -   [System.AppUserModel.RelaunchCommand](../properties/props-system-appusermodel-relaunchcommand.md)
    -   [System.AppUserModel.RelaunchDisplayNameResource](../properties/props-system-appusermodel-relaunchdisplaynameresource.md)
    -   [System.AppUserModel.RelaunchIconResource](../properties/props-system-appusermodel-relaunchiconresource.md)

    > [!Note]  
    > Si existe un acceso directo para iniciar la aplicación, una aplicación debe aplicar AppUserModelID como una propiedad del acceso directo en lugar de usar las propiedades de reintenciones. En ese caso, la línea de comandos, el icono y el texto del acceso directo se usan para proporcionar la misma información que las propiedades de reininició.

     

    Un AppUserModelID explícito de nivel de ventana también puede usar la propiedad [System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) para especificar que no debe estar disponible para anclar o reiniciar.

-   En una llamada para personalizar o actualizar ([**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)), recupere ([**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)) o desactive ([**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)) el valor de la aplicación Lista de accesos directos.
-   En el registro de asociación de archivos (a través de  [su ProgID),](fa-progids.md)si la aplicación usa las listas de destinos Recientes o **Frecuentes generadas** automáticamente por el sistema. [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)hace referencia a esta información de asociación. Esta información también se usa al agregar destinos [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) a listas de saltos personalizadas a través [**de ICustomDestinationList::AppendCategory**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory).
-   En cualquier llamada que la aplicación realiza directamente a [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Si la aplicación depende del cuadro de diálogo de archivo común para realizar llamadas a **SHAddToRecentDocs** en su nombre, esas llamadas pueden deducir el AppUserModelID explícito solo si AppUserModelID está establecido para todo el proceso. Si la aplicación establece AppUserModelIDs en sus ventanas en lugar de en el proceso, la aplicación debe realizar todas las llamadas al propio **SHAddToRecentDocs, con** su AppUserModelID explícito, así como impedir que el cuadro de diálogo de archivo común realice sus propias llamadas. Esto se debe hacer cada vez que  se  abre un elemento, para asegurarse de que las secciones Recientes o Frecuentes de los Lista de accesos directos de la aplicación son precisas.

Los siguientes elementos describen escenarios comunes y dónde aplicar appUserModelID explícitos en esos escenarios.

-   Cuando un único proceso contiene varias aplicaciones, use [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar el almacén de propiedades de la ventana y establecer AppUserModelID como una propiedad de ventana.
-   Cuando una aplicación usa varios procesos, aplique AppUserModelID a cada proceso. El uso del mismo AppUserModelID en cada proceso depende de si desea que cada proceso aparezca como parte de la aplicación principal o como entidades individuales.
-   Para separar determinadas ventanas de un conjunto en el mismo proceso, use el almacén de propiedades de la ventana para aplicar un único AppUserModelID a las ventanas que desea separar y, a continuación, aplique otro AppUserModelID al proceso. Cualquier ventana de ese proceso que no se etiquetara explícitamente con el AppUserModelID de nivel de ventana hereda el AppUserModelID del proceso.
-   Si un tipo de archivo está asociado a una aplicación, asigne AppUserModelID en el registro [ProgID del tipo de](fa-progids.md) archivo. Si se inicia un único archivo ejecutable en distintos modos que se muestran al usuario como aplicaciones distintas, se requiere un AppUserModelID independiente para cada modo. En ese caso, debe haber varios registros ProgID para el tipo de archivo, cada uno con un AppUserModelID diferente.
-   Cuando hay varias ubicaciones de acceso directo desde las  que un usuario puede iniciar una aplicación (en el menú Inicio, en el escritorio o en otro lugar) recupera el almacén de propiedades del acceso directo para aplicar un único AppUserModelID a todos los métodos abreviados como propiedades de acceso directo.
-   Cuando una aplicación realiza una llamada explícita a [**SHAddToRecentDocs,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) use AppUserModelID en la llamada. Cuando se usa el cuadro de diálogo de archivo común para abrir o guardar archivos, el cuadro de diálogo llama a **SHAddToRecentDocs** en nombre de la aplicación. Esa llamada puede deducir el AppUserModelID explícito del proceso. Sin embargo, si se aplica un AppUserModelID explícito como una propiedad de ventana, el cuadro de diálogo de archivo común no puede determinar el AppUserModelID correcto. En ese caso, la propia aplicación debe llamar explícitamente a **SHAddToRecentDocs** y proporcionarle el AppUserModelID correcto. Además, la aplicación debe evitar que el cuadro de diálogo de archivo común llame a **SHAddToRecentDocs** en su nombre estableciendo la marca FOS DONTADDTORECENT en el método \_ **GetOptions** de [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) o [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog).

## <a name="registering-an-application-as-a-host-process"></a>Registro de una aplicación como proceso de host

Una aplicación puede establecer la entrada del Registro IsHostApp para que la barra de tareas considere el proceso de ese ejecutable como un proceso de host. Esto afecta a su agrupación y a las Lista de accesos directos predeterminadas.

En el ejemplo siguiente se muestra la entrada del Registro necesaria. Tenga en cuenta que a la entrada no se le asigna un valor; su presencia es todo lo que se requiere. Es un valor REG \_ NULL.

```
HKEY_CLASSES_ROOT
   Applications
      example.exe
         IsHostApp
```

Si el propio proceso o el archivo de acceso directo usado para iniciar el proceso tienen un AppUserModelID explícito, la lista de procesos host se omite y la barra de tareas trata la aplicación como una aplicación normal. Las ventanas en ejecución de la aplicación se agrupan en un solo botón de la barra de tareas y la aplicación se puede anclar a la barra de tareas.

Si solo se conoce el nombre ejecutable del proceso en ejecución, sin un AppUserModelID explícito y ese ejecutable está en la lista de procesos de host, cada instancia del proceso se trata como una entidad independiente para la agrupación de la barra de tareas. El botón de la barra de tareas asociado a cualquier instancia específica del proceso no muestra una opción anclar o desanclar ni un icono de inicio para una nueva instancia del proceso. El proceso tampoco es apto para incluirse en la **lista** De uso más frecuente (MFU) del menú Inicio. Sin embargo, si el proceso se inició a través de un acceso directo que contiene argumentos de inicio (normalmente el contenido de destino que se va a hospedar como "aplicación"), el sistema puede determinar la identidad y la aplicación se puede anclar y volver a iniciar.

## <a name="exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists"></a>Listas de exclusión para anclar la barra de tareas y listas recientes o frecuentes

Las aplicaciones, los procesos y las ventanas pueden optar por no estar disponibles  para anclarse a la barra de tareas o para su inclusión en la lista MFU del menú Inicio. Hay tres mecanismos para lograrlo:

1.  Agregue la entrada NoStartPage al registro de la aplicación como se muestra aquí:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    Se omiten los datos asociados a la entrada NoStartPage. Solo se requiere la presencia de la entrada. Por lo tanto, el tipo ideal para NoStartPage es REG \_ NONE.

    Tenga en cuenta que cualquier uso de un AppUserModelID explícito invalida la entrada NoStartPage. Si se aplica un AppUserModelID explícito a un acceso directo, proceso o  ventana, se vuelve anclable y apto para la lista MFU del menú Inicio.

2.  Establezca la [propiedad System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) en ventanas y accesos directos. Esta propiedad debe establecerse en una ventana antes de la propiedad [ \_ AppUserModel \_ ID de PKEY.](../properties/props-system-appusermodel-id.md)
3.  Agregue un AppUserModelID explícito como un valor en la siguiente subclave del Registro, como se muestra aquí:

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

    Cada entrada es un valor REG \_ NULL con el nombre de AppUserModelID. Los AppUserModelID que se encuentran en esta lista no se pueden anclar y no se pueden incluir en la **lista** MFU del menú Inicio.

Tenga en cuenta que determinados archivos ejecutables, así como accesos directos que contienen determinadas cadenas en su nombre, se excluyen automáticamente de la anclar y la inclusión en la lista de MFU.

> [!Note]  
> Esta exclusión automática se puede invalidar aplicando un AppUserModelID explícito.

 

Si alguna de las cadenas siguientes, independientemente de las mayúsculas y minúsculas, se incluye en el nombre del acceso directo, el programa no se puede anclar y no se muestra en la lista de uso más frecuente (no se aplica a Windows 10):

-   Documentación
-   Ayuda
-   Instalar
-   Más información
-   Léame
-   Leer primero
-   Léame
-   Quitar
-   Configuración
-   Soporte técnico
-   What's New

La siguiente lista de programas no se puede anclar y se excluye de la lista de uso más frecuente.

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

Las listas anteriores se almacenan en los siguientes valores del Registro.

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

 

 
