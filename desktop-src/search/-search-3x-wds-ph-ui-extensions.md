---
description: Para asegurarse de que los datos se indizan y presentan correctamente al usuario durante las búsquedas, debe implementar los almacenes de datos de Shell (también conocidos como extensiones de espacio de nombres de Shell) y los controladores de tipo de archivo (también conocidos como extensiones de Shell, controladores de extensión o controladores de extensión de Shell).
ms.assetid: 38cebb3c-51bf-439c-8d4e-445344f6cb66
title: Agregar iconos, vistas previas y menús contextuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501006227f6192b7d81a2a88ba915c368a9cc398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540734"
---
# <a name="adding-icons-previews-and-shortcut-menus"></a>Agregar iconos, vistas previas y menús contextuales

Para asegurarse de que los datos se indizan y presentan correctamente al usuario durante las búsquedas, debe implementar los almacenes de datos de Shell (también conocidos como [extensiones de espacio de nombres de Shell](../shell/nse-works.md)) y los controladores de tipo de archivo (también conocidos como extensiones de Shell, controladores de [extensión](../shell/handlers.md)o controladores de extensión de Shell).

En este tema se describen las siguientes interfaces:

-   [Implementar controladores de tipo de archivo](#implementing-file-type-handlers)
    -   [IPersist](#ipersist)
    -   [IPersistFolder](#ipersistfolder)
    -   [IShellFolder](#ishellfolder)
    -   [IContextMenu](#icontextmenu)
    -   [IExtractIcon](#iextracticon)
    -   [IPreviewHandler](#ipreviewhandler)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="implementing-file-type-handlers"></a>Implementar controladores de tipo de archivo

Estas extensiones de shell o controladores de tipo de archivo proporcionan a los usuarios las siguientes experiencias de Shell:

-   La vista de resultados muestra un icono específico para el tipo de elemento.
-   La vista de resultados muestra una vista previa del elemento cuando el usuario selecciona el elemento.
-   Los usuarios pueden hacer doble clic en los elementos para iniciar eventos, como abrir el archivo.
-   Los usuarios pueden hacer clic con el botón secundario en los elementos para tener acceso a un menú contextual.
-   Los usuarios pueden arrastrar y colocar elementos.

Al igual que todos los objetos del modelo de objetos componentes (COM), los controladores de tipo de archivo deben implementar una interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) y un generador de clases.

En Windows XP o versiones anteriores, los controladores también deben implementar:

-   Una [interfaz IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   O [IShellExtInit (interfaz](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) )

En Windows Vista, la interfaz [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) y la [interfaz IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) se reemplazaron por las tres interfaces siguientes para que Shell inicialice el controlador:

-   [Interfaz IInitializeWithStream](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [Interfaz IInitializeWithItem](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [Interfaz IInitializeWithFile](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)

Para proporcionar una experiencia de usuario razonable, debe proporcionar un almacén de datos de Shell con el controlador de protocolo. A continuación, ese almacén de datos sirve como "fábrica" para los controladores de iconos, los controladores de menús contextuales, los controladores de vista previa, etc. Las implementaciones mínimas de la interfaz [IPersist](/windows/desktop/api/objidl/nn-objidl-ipersist) y la interfaz [IPersistFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) son necesarias para la [interfaz IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), y se requiere una implementación mínima de la interfaz IShellFolder para [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) y [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).

> [!Note]  
> Se debe implementar el mismo identificador de clase (CLSID) para **IPersist**, **IPersistFolder** y **IShellFolder**.

 

Para obtener más información sobre cómo crear un almacén de datos de Shell para admitir un controlador de protocolo, vea [implementar las interfaces de objeto de carpeta básicas](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

### <a name="ipersist"></a>IPersist

La interfaz **IPersist** define el único método **GetClassID**, que está diseñado para proporcionar el CLSID de un objeto que se puede almacenar de forma persistente en el sistema.



| Método     | Descripción                                      |
|------------|--------------------------------------------------|
| GetClassID | Devuelve el CLSID del objeto de almacén de datos de Shell. |



 

### <a name="ipersistfolder"></a>IPersistFolder

La interfaz **IPersistFolder** se usa para inicializar los objetos de la carpeta de Shell. La implementación de esta interfaz, que se deriva de **IPersist**, es cómo se indica a la carpeta dónde se encuentra en el espacio de nombres del shell. No utilice esta interfaz directamente. Lo usa la implementación del sistema de archivos del [método IShellFolder:: BindToObject](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) cuando Inicializa un objeto de carpeta de Shell.



| Método     | Descripción                                                                                            |
|------------|--------------------------------------------------------------------------------------------------------|
| Inicialización | Indica a un objeto de carpeta de Shell que se inicialice a sí mismo basándose en la información que se pasa y devuelve S \_ correctos. |



 

### <a name="ishellfolder"></a>IShellFolder

La interfaz de la [interfaz IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) se usa para administrar carpetas y se requiere una implementación parcial para que el icono y las interfaces de contexto implementadas para un controlador de protocolo se comporten correctamente en la interfaz de usuario de los resultados de Windows Search. La mayor parte de la funcionalidad requerida se expone a través del método **GetUIObjectOf** . Este método permite que un complemento consulte las interfaces **IExtractIcon** y **IContextMenu** .

La interfaz de la [interfaz IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) utiliza PIDL en lugar de direcciones URL. A diferencia de los requisitos de un almacén de datos de Shell completo, los complementos pueden usar una estructura IDL simple que solo contiene la dirección URL.

Se deben implementar los siguientes métodos de la [interfaz IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Cinco de estos métodos requieren una implementación mínima.



| Método           | Descripción                                                                                                                                                                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BindToObject     | Devuelve E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| BindToStorage    | Devuelve E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| CreateViewObject | Devuelve E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| SetNameOf        | Devuelve E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| ParseDisplayName | Convierte una dirección URL en la estructura PIDL                                                                                                                                                                                                                                          |
| CompareIDs       | Compara dos valores de PIDL                                                                                                                                                                                                                                                      |
| GetDisplayNameOf | Devuelve la dirección URL de un PIDL                                                                                                                                                                                                                                                    |
| GetUIObjectOf    | Este método es similar al [método IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Si se solicita un icono, el autor de la llamada solicita el IID \_ IExtractIcon; si se solicita un menú contextual, el autor de la llamada solicita el IID \_ IContextMenu |



 

**IShellFolder** no se utiliza para enumerar carpetas. Esto significa que el nombre para mostrar de una carpeta será la dirección URL física. Esto puede cambiar en el futuro.

### <a name="icontextmenu"></a>IContextMenu

Cuando Windows Search muestra los resultados al usuario, puede hacer clic con el botón secundario en un elemento y ver un menú contextual definido por la interfaz **IContextMenu** . Los menús contextuales también se conocen como menús contextuales.

La acción predeterminada en el menú contextual es la misma acción que se realiza cuando se hace doble clic en el elemento. Sin las interfaces de **IShellFolder** o **IContextMenu** correspondientes para el elemento, el comportamiento predeterminado para un evento de doble clic es pasar la dirección URL como un argumento a la función de [función ShellExecute](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) .

Consulte [creación de controladores de menús contextuales](../shell/context-menu-handlers.md) para obtener más información sobre cómo crear controladores de menús contextuales y [ejemplos: extensiones de Shell para controladores de protocolo](-search-3x-wds-ph-ui-samplecode.md) para el código de ejemplo.

### <a name="iextracticon"></a>IExtractIcon

**IExtractIcon** recupera un icono para la interfaz de usuario de búsqueda de Windows basado en la dirección URL en el PIDL proporcionado por el controlador de protocolo.

Consulte [crear controladores de iconos](../shell/how-to-create-icon-handlers.md) para obtener más información sobre cómo crear controladores de iconos y [ejemplos: extensiones de Shell para controladores de protocolo](-search-3x-wds-ph-ui-samplecode.md) para el código de ejemplo.

### <a name="ipreviewhandler"></a>IPreviewHandler

[IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) representa una vista previa enriquecida de un elemento seleccionado en el explorador de Windows. Las versiones preliminares están disponibles en Windows Search 4,0 o en Windows Vista con Windows Desktop Search 3. x.

Para crear un controlador de vista previa personalizado:

1.  Implemente un [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) que tome una [IStream](/windows/win32/api/objidl/nn-objidl-istream), siguiendo las instrucciones proporcionadas en los [controladores de vista previa](../shell/preview-handlers.md).
2.  Registre el controlador de vista previa:

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx\{8895b1c6-b41f-4c1c-a562-0d564250836f}
       @ = {<Your_PreviewHandler_GUID>}
    ```

3.  Complete los dos pasos siguientes para implementar una carpeta de Shell para su dirección URL:
    1.  En el [método IShellFolder:: GetUIObjectOf](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), controle [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) y devuelva la Asociación para los elementos de Shell, tal como se muestra en el ejemplo de código siguiente.

        ```
        CComPtr<IQueryAssociations> spqa;
        AssocCreate(CLSID_QueryAssociations, __uuidof(IQueryAssociations), &spqa);
        spqa->Init(0, L"Your_Object_Type", NULL, NULL);
        spqa->QueryInterface(riid, ppvReturn);
        ```

        

    2.  Una vez que el shell consulta la carpeta de Shell para que el flujo de datos inicialice el controlador de vista previa, vaya al método [IShellFolder:: BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) , controle el IID \_ IStream y devuelva una [IStream](/windows/win32/api/objidl/nn-objidl-istream) a la dirección URL.

Para volver a usar un controlador de vista previa existente para el tipo de archivo, siga estos dos pasos:

1.  Registre el controlador de vista previa para el tipo de archivo mediante el CLSID del controlador de vista previa existente en lugar de <el \_ GUID de PreviewHandler \_>.
2.  Implemente una carpeta de Shell.

Para obtener más información sobre la creación de controladores de vista previa, vea [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) y [controladores de vista previa](../shell/preview-handlers.md).

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).
-   Para obtener información sobre cómo crear controladores, vea [registrar extensiones de Shell](../shell/reg-shell-exts.md), [crear controladores de extensiones de Shell](../shell/handlers.md), [menú contextual](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [extensiones de espacio de nombres de Shell](../shell/nse-works.md) y [controladores de vista previa](../shell/preview-handlers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Desarrollar controladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Descripción de los controladores de protocolo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Notificar el índice de cambios](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Código de ejemplo: extensiones de Shell para controladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Instalar y registrar controladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Crear un conector de búsqueda para un controlador de protocolo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Controladores de protocolo de depuración](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
