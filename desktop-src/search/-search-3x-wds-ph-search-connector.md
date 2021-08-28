---
description: Windows El Explorador controla la creación de un conector de búsqueda para un controlador de protocolo a través de entradas de clave del Registro. A través del registro, tanto los implementadores como terceros pueden permitir que los controladores de protocolos nuevos y heredados participen en Windows 7 Search.
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: Crear un conector de búsqueda para un controlador de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec9c7830f61c0dcbf6682e6dfaea0feb30ebfa5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881690"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a>Crear un conector de búsqueda para un controlador de protocolo

Windows El Explorador controla la creación de un conector de búsqueda para un controlador de protocolo a través de entradas de clave del Registro. A través del registro, tanto los implementadores como terceros pueden permitir que los controladores de protocolos nuevos y heredados participen en Windows 7 Search.

Este tema se organiza de la siguiente manera:

-   [Acerca de los conectores de búsqueda para controladores de protocolo en Windows 7](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [Habilitar controladores de protocolo para participar en la búsqueda](#enabling-protocol-handlers-to-participate-in-search)
    -   [Deshabilitación de la creación del conector de búsqueda del controlador de protocolos](#disabling-protocol-handler-search-connector-creation)
    -   [Personalizar el nombre, la descripción o folderType para un conector de búsqueda de controlador de protocolos](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [Uso del redireccionamiento de cadenas del Registro](#using-registry-string-redirection)
    -   [Restaurar un conector de búsqueda de controladores de protocolos eliminados](#restoring-a-deleted-protocol-handler-search-connector)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a>Acerca de los conectores de búsqueda para controladores de protocolo en Windows 7

En Windows 7, las búsquedas desde el menú Inicio o el Explorador de Windows incluyen solo archivos en ubicaciones indizadas y elementos del sistema que no son de archivos, como almacenes de datos remotos o elementos de controlador de protocolo que tienen un conector de búsqueda.  Además de incluir los elementos de controlador de protocolo en el ámbito  del menú Inicio y  las búsquedas de Shell, el conector de búsqueda habilita el menú Inicio para agrupar los elementos del controlador de protocolo en los resultados del menú Inicio, con la ventaja resultante de que el usuario puede hacer clic en el encabezado del grupo y ver los resultados solo desde el controlador de protocolo.  Como alternativa, el usuario puede ir a la carpeta **Búsquedas,** abrir el archivo del conector de búsqueda y realizar una búsqueda que incluya solo elementos del controlador de protocolo específico asociado a ese conector de búsqueda.

Cuando un usuario inicia por primera vez una aplicación que registra un controlador de protocolo, Windows Explorer genera un archivo de conector de búsqueda (.searchConnector-ms) para el controlador de protocolos en la carpeta **Búsquedas** del usuario. Las aplicaciones con controladores de protocolo pueden optar por deshabilitar este comportamiento o personalizar el nombre y la descripción del conector de búsqueda del controlador de protocolos.

> [!Note]  
> La ubicación de la carpeta **Búsquedas** del usuario es %userprofile% \\ Searches o FOLDERID \_ SavedSearches. El GUID de FOLDERID \_ SavedSearches es {7d1d3a04-debb-4115-95cf-2f29da2920da}.

 

Windows El Explorador controla la creación de un conector de búsqueda para un controlador de protocolo mediante las entradas de clave del Registro que se describen en las secciones siguientes:

-   [Habilitar controladores de protocolo para participar en la búsqueda](#enabling-protocol-handlers-to-participate-in-search)
-   [Deshabilitación de la creación del conector de búsqueda del controlador de protocolos](#disabling-protocol-handler-search-connector-creation)
-   [Personalizar el nombre, la descripción o folderType para un conector de búsqueda de controlador de protocolos](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [Restaurar un conector de búsqueda de controladores de protocolos eliminados](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> No hay ningún medio de programación para crear un conector de búsqueda para un controlador de protocolo. Deben configurarse a través del Registro.

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a>Habilitar controladores de protocolo para participar en la búsqueda

Las claves del Registro y sus valores posibles se describen en la tabla siguiente. Un controlador de protocolo puede rellenar algunas o todas estas claves del Registro en las que el protocolo se reemplaza por el nombre real de su protocolo, por ejemplo, SMTP, archivo o &lt; &gt; csc.



| Clave del Registro                                                                                                                 | Valores posibles                                                                                                                     | Tipo       | Comentarios                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HKEY \_ LOCAL MACHINE Software Microsoft Windows Search \_ \\ \\ \\ \\ PHSearchConnectors \\ &lt; protocol &gt; \\ Version                     | No existe (valor predeterminado). De lo contrario, es 1 o superior.                                                                               | REG \_ DWORD | Este valor se usa para detectar cambios en los registros de la plantilla de ubicación de las raíces de búsqueda que ya se han procesado. Si no existe, use 0 como valor predeterminado. Como alternativa, incremente la versión para informar a Windows Explorer de que se debe volver a generar el conector de búsqueda porque se ha instalado una versión más reciente del controlador de protocolo. |
| HKEY \_ LOCAL MACHINE Software Microsoft Windows Search \_ \\ \\ \\ \\ PHSearchConnectors \\ &lt; protocol &gt; \\ DoNotCreateSearchConnectors | No existe (valor predeterminado). De lo contrario, establezca en 1.                                                                                         | REG \_ DWORD | Si no existe, cree un archivo .searchconnector-ms en la carpeta Búsquedas. Si es 1, marque como procesado y no haga nada.                                                                                                                                                                                                                                   |
| HKEY \_ LOCAL MACHINE Software Microsoft Windows Search \_ \\ \\ \\ \\ PHSearchConnectors \\ &lt; protocol Default &gt; \\ \\ Description        | Cadena localizable que contiene la descripción del conector de búsqueda.                                                              | REG \_ SZ    | Opcional. Se usa en el elemento Description del archivo .searchconnector-ms.                                                                                                                                                                                                                                                                          |
| HKEY \_ LOCAL MACHINE Software Microsoft Windows Search \_ \\ \\ \\ \\ PHSearchConnectors \\ &lt; protocol Default &gt; \\ \\ Name               | Cadena localizada para dar nombre al conector de búsqueda. Se usa como nombre del archivo .searchconnector-ms.                                    | REG \_ SZ    | Cada ubicación debe tener un nombre único. En ausencia de este valor, se usará el nombre para mostrar proporcionado por la interfaz [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) del controlador de protocolo.                                                                                                                             |
| HKEY \_ LOCAL MACHINE Software Microsoft Windows Search \_ \\ \\ \\ \\ PHSearchConnectors \\ &lt; protocol Default &gt; \\ \\ FolderType         | GUID que identifica el [FOLDERTYPEID que se](../shell/foldertypeid.md) aplicará al conector de búsqueda. | REG \_ SZ    | Opcional. Se usa en el elemento folderType del archivo .searchconnector-ms para indicar qué plantillas se deben usar para mostrar los resultados. Por ejemplo, el valor GUID de FOLDERTYPEID \_ Documents.                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a>Deshabilitación de la creación del conector de búsqueda del controlador de protocolos

Si la aplicación expone elementos a través de un controlador de protocolo para su uso  en la propia aplicación y no desea exponer los elementos a través del shell (en el menú Inicio y búsquedas del Explorador de Windows), debe deshabilitar la creación de un conector de búsqueda para el controlador de protocolo.

Para deshabilitar la creación del conector de búsqueda, establezca DoNotCreateSearchConnectors en 0x00000001(1), como se muestra en el siguiente ejemplo de clave del Registro.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

Si DoNotCreateSearchConnectors se establece en 1, se recomienda exponer la propiedad [System.Shell.OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) en cada elemento expuesto por el controlador de protocolo y establecer el valor de esta propiedad en **TRUE.** Si lo hace, impedirá que los elementos del controlador de protocolo aparezcan en el **grupo** Archivos **del menú** Inicio.

Si DoNotCreateSearchConnectors está presente y se establece en cero, el Explorador de Windows creará un conector de  búsqueda para el controlador de protocolos y los elementos del controlador de protocolo se devolverán en en el menú Inicio y Windows Explorer buscará.

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a>Personalizar el nombre, la descripción o folderType para un conector de búsqueda de controlador de protocolos

El nombre del conector de búsqueda se usa no solo para identificar el conector de búsqueda en la carpeta **Búsquedas,** sino como el encabezado de grupo de los resultados en las **búsquedas del** menú Inicio. Por lo tanto, es importante proporcionar un nombre descriptivo para el conector de búsqueda. Si no se proporciona un nombre en la clave del Registro, el Explorador de Windows usa de forma predeterminada el nombre proporcionado por la interfaz [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) para la raíz de búsqueda del controlador de protocolos y la descripción en blanco. Puede invalidar el nombre predeterminado a través de una entrada de clave del Registro sin tener que cambiar el nombre de la interfaz IShellFolder. Aunque no es tan visible como el nombre del conector de búsqueda, también puede invalidar la descripción del conector de búsqueda proporcionando su propia descripción.

Para invalidar el nombre o la descripción predeterminados, establezca las entradas como se muestra en el siguiente ejemplo del Registro.

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

Además, la entrada FolderType se puede establecer en uno de los GUID [de FOLDERTYPEID.](../shell/foldertypeid.md) El valor debe ser el GUID real y no su nombre. Por ejemplo, {94d6ddcc-4a68-4175-a374-bd584a510b78} en lugar de FOLDERTYPEID \_ Música. El GUID de un FOLDERTYPEID se puede obtener en el archivo de encabezado Shlguid.h del [SDK Windows .](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

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

### <a name="using-registry-string-redirection"></a>Uso del redireccionamiento de cadenas del Registro

Puede usar una cadena [redirigida](../intl/using-registry-string-redirection.md) para asegurarse de que el nombre que proporcione para el conector de búsqueda se pueda localizar. Puede incluir cadenas localizables para las claves del Registro de nombre y descripción en lugar de escribir la cadena real en el Registro.

Para incluir una cadena localizable para los valores Nombre o Descripción, establezca el valor como se muestra en el siguiente ejemplo de clave del Registro.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Name = @dllname.dll,-resourceID
```

La cadena localizable tiene el formato siguiente:

-   @dllname.dll,-resourceID, donde:
    -   @dllname.dll es la ruta de acceso al archivo DLL que contiene el recurso de cadena.
    -   resourceID es el identificador de recurso entero del recurso de cadena.

El formato de una cadena indirecta, y una cadena indirecta anexada con un modificador de versión, se describe en [FUNCIÓN SHLoadIndirectString](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a>Restaurar un conector de búsqueda de controladores de protocolos eliminados

Dado que los conectores de búsqueda son archivos en el equipo del usuario, se pueden eliminar por error. Para restaurar todos los conectores de búsqueda del controlador de protocolos eliminados, restaure las bibliotecas predeterminadas. Para ello, abra el Explorador Windows, haga clic con el botón derecho en la carpeta **Bibliotecas** y, a continuación, **seleccione Restaurar bibliotecas predeterminadas**.

![captura de pantalla que muestra la opción de menú restaurar bibliotecas predeterminadas](images/libraries.png)

## <a name="additional-resources"></a>Recursos adicionales

-   [IShellItem::GetDisplayName](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [SIGDN \_ NORMALDISPLAY](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Descripción de los controladores de protocolo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Desarrollar controladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Notificación al índice de cambios](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Agregar iconos y menús contextuales](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Ejemplo de código: Extensiones de shell para controladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Instalación y registro de controladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Depuración de controladores de protocolo](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
