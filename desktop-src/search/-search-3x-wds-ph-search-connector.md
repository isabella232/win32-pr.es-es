---
description: El explorador de Windows controla la creación de un conector de búsqueda para un controlador de protocolo a través de entradas de clave del registro. A través del registro, tanto los implementadores como los de terceros pueden permitir que los controladores de protocolos nuevos y heredados participen en la búsqueda de Windows 7.
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: Crear un conector de búsqueda para un controlador de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b43fd7eac53ca2c89d6c8b0d2cd36fd813e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153986"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a>Crear un conector de búsqueda para un controlador de protocolo

El explorador de Windows controla la creación de un conector de búsqueda para un controlador de protocolo a través de entradas de clave del registro. A través del registro, tanto los implementadores como los de terceros pueden permitir que los controladores de protocolos nuevos y heredados participen en la búsqueda de Windows 7.

Este tema se organiza de la siguiente manera:

-   [Acerca de los conectores de búsqueda para los controladores de protocolo en Windows 7](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [Habilitar los controladores de protocolo para participar en la búsqueda](#enabling-protocol-handlers-to-participate-in-search)
    -   [Deshabilitando la creación del conector de búsqueda del controlador de protocolo](#disabling-protocol-handler-search-connector-creation)
    -   [Personalización del nombre, la descripción o el FolderType para un conector de búsqueda de controlador de protocolo](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [Usar el redireccionamiento de cadenas del registro](#using-registry-string-redirection)
    -   [Restaurar un conector de búsqueda de controlador de protocolo eliminado](#restoring-a-deleted-protocol-handler-search-connector)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a>Acerca de los conectores de búsqueda para los controladores de protocolo en Windows 7

En Windows 7, las búsquedas desde el menú **Inicio** o el explorador de Windows incluyen solo archivos en ubicaciones indizadas y elementos del sistema que no son de archivos como los almacenes de datos remotos o los elementos de controlador de protocolo que tienen un conector de búsqueda. Además de incluir los elementos de controlador de protocolo en el ámbito del menú **Inicio** y las búsquedas de Shell, el conector de búsqueda permite que el menú **Inicio** agrupe los elementos del controlador de protocolo en los resultados del menú **Inicio** , con la ventaja resultante de que el usuario puede hacer clic en el encabezado de grupo y ver los resultados solo desde el controlador de protocolo. Como alternativa, el usuario puede ir a la carpeta **búsquedas** , abrir el archivo del conector de búsqueda y realizar una búsqueda que incluya solo los elementos del controlador de protocolo específico asociado a ese conector de búsqueda.

Cuando un usuario inicia por primera vez una aplicación que registra un controlador de protocolo, el explorador de Windows genera un archivo de conector de búsqueda (. searchConnector-MS) para el controlador de protocolo en la carpeta **búsquedas** del usuario. Las aplicaciones con controladores de protocolo pueden optar por deshabilitar este comportamiento o personalizar el nombre y la descripción del conector de búsqueda del controlador de protocolo.

> [!Note]  
> La ubicación de la carpeta **búsquedas** del usuario es% userprofile% \\ búsquedas o FOLDERID \_ SavedSearches. El GUID para FOLDERID \_ SavedSearches es {7d1d3a04-Debb-4115-95cF-2f29da2920da}.

 

El explorador de Windows controla la creación de un conector de búsqueda para un controlador de protocolo a través de las entradas de clave del registro descritas en las siguientes secciones:

-   [Habilitar los controladores de protocolo para participar en la búsqueda](#enabling-protocol-handlers-to-participate-in-search)
-   [Deshabilitando la creación del conector de búsqueda del controlador de protocolo](#disabling-protocol-handler-search-connector-creation)
-   [Personalización del nombre, la descripción o el FolderType para un conector de búsqueda de controlador de protocolo](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [Restaurar un conector de búsqueda de controlador de protocolo eliminado](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> No hay ningún medio de programación para crear un conector de búsqueda para un controlador de protocolo. Deben configurarse a través del registro.

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a>Habilitar los controladores de protocolo para participar en la búsqueda

Las claves del registro y sus valores posibles se describen en la tabla siguiente. Un controlador de protocolo puede rellenar algunas o todas estas claves del registro <protocol> , donde se reemplaza por el nombre real de su Protocolo, como MAPI, archivo o CSC, por ejemplo.



| Clave del Registro                                                                                                                 | Valores posibles                                                                                                                     | Tipo       | Comentarios                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ versión                     | No existe (valor predeterminado). De lo contrario, es 1 o superior.                                                                               | \_valor DWORD reg | Este valor se usa para detectar los cambios en los registros de la plantilla de ubicación para las raíces de búsqueda que ya se han procesado. Si no existe, use 0 como valor predeterminado. También puede incrementar la versión para informar al explorador de Windows de que el conector de búsqueda debe volver a generarse porque se ha instalado una versión más reciente del controlador de protocolo. |
| HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ DoNotCreateSearchConnectors | No existe (valor predeterminado). De lo contrario, se establece en 1.                                                                                         | \_valor DWORD reg | Si no existe, cree un archivo. searchconnector-MS en la carpeta búsquedas. Si es 1, marcar como procesado y no hacer nada.                                                                                                                                                                                                                                   |
| HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ default \\ Description        | Una cadena localizable que contiene la descripción del conector de búsqueda.                                                              | Registro \_ SZ    | Opcional. Se usa en el elemento Description del archivo. searchconnector-ms.                                                                                                                                                                                                                                                                          |
| HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ \\ nombre predeterminado               | Una cadena localizada para asignar un nombre al conector de búsqueda. Se usa como nombre del archivo. searchconnector-ms.                                    | Registro \_ SZ    | Cada ubicación debe tener un nombre único. En ausencia de este valor, se usará el nombre para mostrar proporcionado por la [interfaz IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) del controlador de protocolo.                                                                                                                             |
| HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ default \\ FolderType         | GUID que identifica el [FOLDERTYPEID](../shell/foldertypeid.md) que se va a aplicar al conector de búsqueda. | Registro \_ SZ    | Opcional. Se usa en el elemento folderType del archivo. searchconnector-ms para indicar qué plantillas deben usarse para mostrar los resultados. Por ejemplo, el valor GUID de FOLDERTYPEID \_ Documents.                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a>Deshabilitando la creación del conector de búsqueda del controlador de protocolo

Si la aplicación expone elementos a través de un controlador de protocolo para su uso en la propia aplicación y no desea exponer los elementos a través del shell (en el menú **Inicio** y búsquedas del explorador de Windows), debe deshabilitar la creación de un conector de búsqueda para el controlador de protocolo.

Para deshabilitar la creación del conector de búsqueda, establezca DoNotCreateSearchConnectors en 0x00000001 (1), tal y como se muestra en el siguiente ejemplo de clave del registro.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

Si DoNotCreateSearchConnectors se establece en 1, se recomienda que exponga la propiedad [System. Shell. OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) en cada elemento expuesto por el controlador de protocolo y establezca el valor de esta propiedad en **true**. Esto impedirá que los elementos del controlador de protocolo aparezcan en el grupo **archivos** del menú **Inicio** .

Si DoNotCreateSearchConnectors está presente y se establece en cero, el explorador de Windows creará un conector de búsqueda para el controlador de protocolo y los elementos del controlador de protocolo se devolverán en el menú **Inicio** y las búsquedas del explorador de Windows.

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a>Personalización del nombre, la descripción o el FolderType para un conector de búsqueda de controlador de protocolo

El nombre del conector de búsqueda se usa no solo para identificar el conector de búsqueda en la carpeta **búsquedas** , sino como el encabezado de grupo de los resultados en las búsquedas en el menú **Inicio** . Por lo tanto, es importante proporcionar un nombre descriptivo para el conector de búsqueda. Si no se proporciona un nombre en la clave del registro, de forma predeterminada el explorador de Windows utiliza el nombre proporcionado por la [interfaz IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) para la raíz de búsqueda del controlador de protocolo y la descripción en blanco. Puede invalidar el nombre predeterminado a través de una entrada de clave del registro sin tener que cambiar el nombre de la interfaz IShellFolder. Aunque no es tan visible como el nombre del conector de búsqueda, también puede invalidar la descripción del conector de búsqueda proporcionando su propia descripción.

Para reemplazar el nombre o la descripción predeterminados, establezca las entradas tal como se muestra en el siguiente ejemplo del registro.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     Name
                     Description
```

Además, la entrada FolderType se puede establecer en uno de los GUID de [FOLDERTYPEID](../shell/foldertypeid.md) . El valor debe ser el GUID real, no su nombre. Por ejemplo, {94d6ddcc-4a68-4175-A374-bd584a510b78} en lugar de FOLDERTYPEID \_ Music. El GUID de una FOLDERTYPEID se puede obtener en el archivo de encabezado Shlguid. h en el [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     FolderType = {94d6ddcc-4a68-4175-a374-bd584a510b78}
```

### <a name="using-registry-string-redirection"></a>Usar el redireccionamiento de cadenas del registro

Puede usar una [cadena redirigida](../intl/using-registry-string-redirection.md) para asegurarse de que se puede localizar el nombre proporcionado para el conector de búsqueda. Puede incluir cadenas localizables para las claves del registro Name y Description en lugar de escribir la cadena real en el registro.

Para incluir una cadena localizable para los valores de nombre o descripción, establezca el valor como se muestra en el siguiente ejemplo de clave del registro.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Name = @dllname.dll,-resourceID
```

La cadena traducible tiene el siguiente formato:

-   @dllname.dll,-resourceID, donde:
    -   @dllname.dll es la ruta de acceso al archivo DLL que contiene el recurso de cadena.
    -   resourceID es el identificador de recurso entero del recurso de cadena

El formato de una cadena indirecta y una cadena indirecta anexada con un modificador de versión se describen en la [función SHLoadIndirectString](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a>Restaurar un conector de búsqueda de controlador de protocolo eliminado

Dado que los conectores de búsqueda son archivos en el equipo del usuario, se pueden eliminar por error. Para restaurar todos los conectores de búsqueda del controlador de protocolo eliminados, restaure las bibliotecas predeterminadas. Para ello, abra el explorador de Windows, haga clic con el botón secundario en la carpeta **bibliotecas** y, a continuación, seleccione **restaurar bibliotecas predeterminadas**.

![captura de pantalla que muestra la opción de menú restaurar bibliotecas predeterminadas](images/libraries.png)

## <a name="additional-resources"></a>Recursos adicionales

-   [IShellItem:: GetDisplayName](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [SIGDN \_ NORMALDISPLAY](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Descripción de los controladores de protocolo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Desarrollar controladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Notificar el índice de cambios](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Agregar iconos y menús contextuales](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Código de ejemplo: extensiones de Shell para controladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Instalar y registrar controladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Controladores de protocolo de depuración](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
