---
description: En este tema se explica cómo crear nuevos tipos de archivo y cómo asociar la aplicación con el tipo de archivo y otros tipos de archivo bien definidos.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Tipos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 541e6068237b504ea8c9faf06e2083986ed5bb48a7c16dabb82e5096569d9f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094210"
---
# <a name="file-types"></a>Tipos de archivo

En este tema se explica cómo crear nuevos tipos de archivo y cómo asociar la aplicación con el tipo de archivo y otros tipos de archivo bien definidos. Los archivos con una extensión de nombre de archivo común compartido (.doc, .html, y así sucesivamente) son del mismo *tipo.* Por ejemplo, si crea un nuevo editor de texto, puede usar el tipo de archivo .txt existente. En otros casos, es posible que tenga que crear un nuevo tipo de archivo.

Este tema se organiza de la siguiente manera:

-   [Tipos de archivo públicos y privados](#public-and-private-file-types)
-   [Registrar un tipo de archivo](#registering-a-file-type)
    -   [Establecer subclaves opcionales y atributos de extensión de tipo de archivo](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [Eliminar información del Registro durante la desinstalación](#deleting-registry-information-during-uninstallation)
-   [Tipos de archivo que admiten metadatos abiertos](#file-types-that-support-open-metadata)
-   [Temas relacionados](#related-topics)

Puede encontrar información adicional en los temas siguientes:

-   [Cómo elegir una extensión de tipo de archivo](how-to-choose-a-file-type-extension.md)
-   [Definición de atributos de tipo de archivo](./how-to-define-file-type-attributes.md)
-   [Cómo incluir una aplicación en el cuadro de diálogo Abrir con archivo](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Cómo excluir una aplicación del cuadro de diálogo Abrir con para tipos de archivo no asociados](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a>Tipos de archivo públicos y privados

Los tipos de archivo públicos también se conocen como tipos populares o contenciosos, ya que es posible que las aplicaciones de la competencia quieran asociarse a estos tipos de archivo. Entre las características de los tipos de archivo públicos se incluyen:

-   Normalmente, se definen mediante los organismos de estándares o se promueven mediante la definición de organizaciones como formatos de intercambio.
-   A menudo se intercambian entre equipos y usuarios para diversos propósitos.
-   Deben ser compatibles con muchas plataformas diferentes.
-   Es probable que las aplicaciones de varios proveedores las controlen.

Algunos ejemplos de tipos de archivo que se consideran públicos son los tipos de archivo de imagen .png, .gif, .jpg y .bmp, y los tipos de audio .wav, .mp3 y .au.

A diferencia de los tipos de archivo públicos, los tipos de archivo privados o propietarios suelen tener un formato que solo una aplicación o proveedor implementa y entiende. Como resultado, los tipos de archivo privados no suelen ser propensos a conflictos entre aplicaciones. Algunos tipos de archivo se pueden iniciar como tipos de archivo privados, pero más adelante se convierten en tipos de archivo públicos.

> [!Note]  
> Windows no diferencia entre los tipos de archivo público y privado. La distinción solo es relevante para tomar decisiones sobre la elección del registro de tipo de archivo.

 

## <a name="registering-a-file-type"></a>Registrar un tipo de archivo

Para asociar el tipo de archivo a una aplicación existente, busque la aplicación ProgID en el Registro. Para asociar el tipo de archivo a una nueva aplicación, defina un ProgID para la aplicación. Para obtener información sobre cómo definir un nuevo ProgID, vea [Identificadores de programación](fa-progids.md).

Las subclaves de extensión de nombre de archivo tienen el siguiente formato general: *extension* = *ProgID*. Las subclaves de extensión de nombre de archivo se almacenan en el **subárbol RAÍZ \_ \_ HKEY CLASSES.**

Es importante incluir el punto inicial (.) al crear subclaves de tipo de archivo en el Registro. Por ejemplo, si desea que un tipo de archivo con la extensión corta .myp y la extensión larga .myp-file se abran con una aplicación denominada MyProgram, use la sintaxis siguiente:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

Como se muestra en el ejemplo anterior, si también registra una extensión de nombre de archivo corto (.myp), también debe crear una subclave para la extensión long (.myp-file). Para obtener más información, vea [Controladores de tipos de archivo](fa-file-extensions.md).

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a>Establecer subclaves opcionales y atributos de extensión de tipo de archivo

Las entradas de extensión de tipo de archivo en el Registro tienen varias subclaves y atributos opcionales.

Las entradas de extensión de tipo de archivo que usan las asociaciones de archivo se describen en la tabla siguiente. Todos los valores son del **tipo REG \_ SZ.**



| Entrada del Registro  | Acción                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor predeterminado         | Establezca el valor predeterminado de la subclave de extensión en el ProgID al que está vinculada.                                                                                                                                                                                                                                                 |
| Tipo de contenido    | Establezca el valor de Tipo de contenido en el tipo de contenido MIME del tipo de archivo.                                                                                                                                                                                                                                                                   |
| OpenWithList    | No debe usarse. Esta subclave contiene una o varias subclaves de aplicación para las aplicaciones que aparecen en la entrada del cuadro de diálogo Abrir con para el tipo de archivo y solo está pensada para aplicaciones .exe en sistemas operativos anteriores **Windows** XP. En su lugar, use OpenWithProgIds.                                                            |
| OpenWithProgIds | Esta subclave contiene una lista de ProgID alternativos para este tipo de archivo. Los programas de estos ProgID  aparecen en el menú Abrir con y están disponibles de forma predeterminada en Windows Store para el tipo de archivo. Cada vez que una aplicación toma el control de este tipo de archivo cambiando el valor predeterminado, también debe agregar una entrada a esta lista. |
| PerceivedType   | Establezca el valor de PerceivedType en perceivedType al que pertenece el archivo, si lo hay. Esta cadena no se usa en Windows versiones anteriores a Windows Vista. Para obtener más información, vea [Perceived Types and Application Registration](fa-perceivedtypes.md).                                                                           |



 

La forma general de una subclave de extensión de nombre de archivo es la siguiente. Todos los tipos de entrada son del **tipo REG \_ SZ.**

```
HKEY_CLASSES_ROOT
   .ext
      (Default) = ProgID.ext.1
      Content Type = MIME content type
      PerceivedType = PerceivedType
      OpenWithProgids
         ProgID2.ext.1
         ProgID3.ext.1
      ProgID.ext.1
         shellnew
```

Entre las consideraciones importantes sobre los tipos de archivo se incluyen:

-   El **subárbol RAÍZ \_ \_ HKEY CLASSES es** una vista formada por la combinación de clases de software **HKEY CURRENT \_ \_ USER** \\  \\ **y** **HKEY LOCAL \_ \_ MACHINE** \\ **Software** \\ **Classes**
-   En general, **HKEY \_ CLASSES \_ ROOT** está pensado para leerse, pero no para escribirse en él. Para obtener más información, vea el [artículo raíz HKEY \_ CLASSES. \_ ](../sysinfo/hkey-classes-root-key.md)
-   Para registrar un tipo de archivo globalmente en un equipo determinado, cree una entrada para el tipo de archivo en la subclave clases de software **HKEY \_ LOCAL \_ MACHINE.** \\  \\ 
-   Para que un registro de tipo de archivo solo sea visible para el usuario actual, cree una entrada para el tipo de archivo en la subclave clases de software **HKEY \_ CURRENT \_ USER.** \\  \\ 
-   Una aplicación puede proporcionar su propia implementación de un verbo, como abrir o reproducir, como se muestra en el siguiente ejemplo del Registro.

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    Las subclaves de la subclave de verbo incluyen la línea de comandos y el método drop target: **command** y **DropTarget.**

-   Al crear o cambiar una asociación de archivos, es importante notificar al sistema que ha realizado un cambio. Para ello, llame a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) y especifique el evento **\_ ASSOCCHANGED de SHCNE.** Si no llama a **SHChangeNotify,** es posible que el cambio no se reconozca hasta después de reiniciar el sistema.
-   Para recuperar información del Registro relativa a una asociación de archivos, use la [**interfaz IQueryAssociations.**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) Para ver un escenario que ilustra este procedimiento, vea [Escenario de ejemplo de asociación de archivos](fa-sample-scenarios.md).

> [!Note]  
> Las **subclaves del** Registro Rutas de acceso de la aplicación y Aplicaciones se usan para registrar y controlar el comportamiento del sistema en nombre de las aplicaciones.  Para obtener información más detallada sobre esta funcionalidad, vea [Registro de aplicaciones.](app-registration.md)

 

### <a name="deleting-registry-information-during-uninstallation"></a>Eliminar información del Registro durante la desinstalación

Al desinstalar una aplicación, los ProgID y la mayoría de la información del Registro asociada a esa aplicación deben eliminarse como parte de la desinstalación. Sin embargo, las aplicaciones que han tomado posesión de un tipo de archivo (estableciendo el valor predeterminado de la subclave .extension raíz **HKEY \_ CLASSES \_ ROOT** del tipo de archivo en el ProgID de la aplicación) no deben intentar quitar ese valor al \\  desinstalar. Dejar los datos en su lugar para el valor Predeterminado evita la dificultad de determinar si otra aplicación ha tomado posesión del tipo de archivo y ha sobrescrito el valor Predeterminado después de instalar la aplicación original. Windows respeta el valor Predeterminado solo si el ProgID encontró que hay un ProgID registrado. Si el ProgID no está registrado, se omite.

Tenga en cuenta que otra información de propiedad de tipo de archivo se almacena en el subárbol **HKEY \_ CURRENT \_ USER** y también se usa solo cuando se registra la aplicación a la que hace referencia. Por lo tanto, no es necesario quitar estos datos al desinstalar una aplicación.

Por ejemplo, a continuación se muestra el estado del registro antes de desinstalar una aplicación:

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID
      shell
         open
            command
               (Default) = yourapp.exe %1
```

A continuación se muestra el estado de esas mismas entradas del Registro después de desinstalar la aplicación.

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a>Tipos de archivo que admiten metadatos abiertos

En Windows 7 y versiones posteriores, los siguientes tipos de archivo admiten metadatos abiertos.



| Tipo de archivo                                                               | Extensiones de nombre de archivo                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| Office documentos de 2007                                                   | .docx, .xlsx, .pptx                                           |
| Office documentos 97-2003                                                | .doc, .xls, .ppt                                              |
| Búsqueda guardada                                                            | .search-ms                                                    |
| Windows Contenedor de formatos basados en medios (formato de streaming avanzado [ASF]) | .wmv, .wma                                                    |
| MP4 (controlador de propiedades)                                                  | .mp4, .m4a, .m4v, .mp4v, .m4p, .m4b, .3gp, .3gpp, .3gp2, .mov |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones](app-registration.md)
</dt> <dt>

[Cómo funcionan las asociaciones de archivos](fa-how-work.md)
</dt> <dt>

[Vista de contenido por tipo de archivo o tipo](prophand-content-view.md)
</dt> <dt>

[Comprobador de tipo de archivo](file-type-verifier.md)
</dt> <dt>

[Controladores de tipos de archivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores de programación](fa-progids.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrices de asociación](fa-associationarray.md)
</dt> </dl>

 

 
