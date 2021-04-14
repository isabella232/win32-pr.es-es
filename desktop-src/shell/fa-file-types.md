---
description: En este tema se explica cómo crear nuevos tipos de archivo y cómo asociar la aplicación con el tipo de archivo y otros tipos de archivo bien definidos.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Tipos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d697c42626c6e1ab3e0b5cc0b88bd065523d53a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985531"
---
# <a name="file-types"></a>Tipos de archivo

En este tema se explica cómo crear nuevos tipos de archivo y cómo asociar la aplicación con el tipo de archivo y otros tipos de archivo bien definidos. Los archivos con una extensión de nombre de archivo común compartida (. doc,. html, etc.) son del mismo *tipo*. Por ejemplo, si crea un nuevo editor de texto, puede usar el tipo de archivo. txt existente. En otros casos, puede que tenga que crear un nuevo tipo de archivo.

Este tema se organiza de la siguiente manera:

-   [Tipos de archivo públicos y privados](#public-and-private-file-types)
-   [Registro de un tipo de archivo](#registering-a-file-type)
    -   [Establecer subclaves opcionales y atributos de extensión de tipo de archivo](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [Eliminar información del registro durante la desinstalación](#deleting-registry-information-during-uninstallation)
-   [Tipos de archivo que admiten metadatos abiertos](#file-types-that-support-open-metadata)
-   [Temas relacionados](#related-topics)

Puede encontrar información adicional en los temas siguientes:

-   [Cómo elegir una extensión de tipo de archivo](how-to-choose-a-file-type-extension.md)
-   [Cómo definir atributos de tipo de archivo](./how-to-define-file-type-attributes.md)
-   [Cómo incluir una aplicación en el cuadro de diálogo Abrir con](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Cómo excluir una aplicación del cuadro de diálogo Abrir con para tipos de archivo no asociados](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a>Tipos de archivo públicos y privados

Los tipos de archivo públicos también se conocen como tipos populares o polémicos porque es posible que las aplicaciones competidoras quieran estar asociadas con estos tipos de archivo. Las características de los tipos de archivo públicos incluyen:

-   Normalmente, se definen mediante cuerpos de estándares o se promocionan por sus organizaciones que la definen como formatos de intercambio.
-   A menudo se intercambian entre equipos y usuarios para distintos fines.
-   Deben admitirse en muchas plataformas diferentes.
-   Es probable que las aplicaciones de varios proveedores las controlen.

Algunos ejemplos de tipos de archivo que se consideran públicos son los tipos de archivo de imagen. png,. gif,. jpg y. bmp, y los tipos de audio. wav,. mp3 y. au.

A diferencia de los tipos de archivo públicos, los tipos de archivos privados o propietarios suelen tener un formato que solo una aplicación o un proveedor comprenden. Como resultado, los tipos de archivo privados no suelen ser propensos a conflictos entre aplicaciones. Algunos tipos de archivo se pueden iniciar como tipos de archivo privados, pero posteriormente se convierten en tipos de archivo públicos.

> [!Note]  
> Windows no diferencia entre los tipos de archivo públicos y privados. La distinción solo es relevante para tomar decisiones sobre la elección del registro de tipo de archivo.

 

## <a name="registering-a-file-type"></a>Registro de un tipo de archivo

Para asociar el tipo de archivo a una aplicación existente, busque el ProgID de la aplicación en el registro. Para asociar el tipo de archivo a una nueva aplicación, defina un ProgID para la aplicación. Para obtener información sobre cómo definir un nuevo ProgID, vea [identificadores de programación](fa-progids.md).

Las subclaves de la extensión de nombre de archivo tienen el formato general siguiente: ProgID de *extensión* = . Las subclaves de extensión de nombre de archivo se almacenan en el subárbol **\_ \_ raíz de las clases HKEY** .

Es importante incluir el punto inicial (.) al crear subclaves de tipo de archivo en el registro. Por ejemplo, si desea que un tipo de archivo con la extensión abreviada. MYP y el archivo Long Extension. MYP se abra con una aplicación llamada, use la siguiente sintaxis:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

Como se muestra en el ejemplo anterior, si también registra una extensión de nombre de archivo corto (. MYP), debe crear una subclave para la extensión larga (. MYP-File) también. Para obtener más información, vea [controladores de tipo de archivo](fa-file-extensions.md).

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a>Establecer subclaves opcionales y atributos de extensión de tipo de archivo

Las entradas de extensión de tipo de archivo del registro tienen varias subclaves y atributos opcionales.

En la tabla siguiente se describen las entradas de extensión de tipo de archivo que se usan en las asociaciones de archivo. Todos los valores son del tipo **reg \_ SZ** .



| Entrada del Registro  | Acción                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor predeterminado         | Establezca el valor predeterminado de la subclave de extensión en el ProgID al que está vinculado.                                                                                                                                                                                                                                                 |
| Tipo de contenido    | Establezca el valor de tipo de contenido en el tipo de contenido MIME del tipo de archivo.                                                                                                                                                                                                                                                                   |
| OpenWithList    | No debe usarse. Esta subclave contiene una o más subclaves de aplicación para las aplicaciones que aparecen en la entrada del cuadro de diálogo **abrir con** para el tipo de archivo y se ha diseñado únicamente para aplicaciones. exe en sistemas operativos anteriores a Windows XP. Use OpenWithProgIds en su lugar.                                                            |
| OpenWithProgIds | Esta subclave contiene una lista de ProgID alternativos para este tipo de archivo. Los programas de estos ProgID aparecen en el menú **abrir con** y están disponibles como aplicaciones de la tienda Windows predeterminadas para el tipo de archivo. Cada vez que una aplicación usa este tipo de archivo cambiando el valor predeterminado, también debe agregar una entrada a esta lista. |
| PerceivedType   | Establezca el valor de PerceivedType en el PerceivedType al que pertenece el archivo, si existe. Las versiones de Windows anteriores a Windows Vista no utilizan esta cadena. Para obtener más información, vea [tipos percibidos y registro de aplicaciones](fa-perceivedtypes.md).                                                                           |



 

La forma general de una subclave de extensión de nombre de archivo es la siguiente. Todos los tipos de entrada son del tipo **reg \_ SZ** .

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

Las consideraciones importantes sobre los tipos de archivo incluyen:

-   El subárbol **\_ \_ raíz de las clases HKEY** es una vista formada mediante la combinación de las clases de software de **\_ \_ usuario actual** \\  \\  de HKEY y las clases de software de **\_ \_ máquina local HKEY** \\  \\ 
-   En general, **la \_ \_ raíz de las clases HKEY** está pensada para que se pueda leer, pero no se puede escribir en ella. Para obtener más información, consulte el artículo [ \_ \_ raíz de clases HKEY](../sysinfo/hkey-classes-root-key.md) .
-   Para registrar un tipo de archivo globalmente en un equipo determinado, cree una entrada para el tipo de archivo en la subclave **HKEY \_ local \_ Machine** \\ **software** \\ **classes** .
-   Para que un registro de tipo de archivo sea visible solo para el usuario actual, cree una entrada para el tipo de archivo en la subclave de clases de software del **\_ \_ usuario actual de HKEY** \\  \\  .
-   Una aplicación puede proporcionar su propia implementación de un verbo, como Open o Play, como se muestra en el siguiente ejemplo del registro.

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    Las subclaves de la subclave Verb incluyen la línea de comandos y el método de destino de colocación: **Command** y **DropTarget**.

-   Al crear o cambiar una asociación de archivo, es importante notificar al sistema que ha realizado un cambio. Para ello, llame a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) y especifique el **evento \_ ASSOCCHANGED de SHCNE** . Si no llama a **SHChangeNotify**, es posible que no se reconozca el cambio hasta que se reinicie el sistema.
-   Para recuperar información del registro relativa a una asociación de archivo, use la interfaz [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) . Para ver un escenario que ilustra este procedimiento, consulte el [escenario de ejemplo de Asociación de archivos](fa-sample-scenarios.md).

> [!Note]  
> Las subclaves del registro de **aplicaciones** y rutas de acceso de la **aplicación** se usan para registrar y controlar el comportamiento del sistema en nombre de las aplicaciones. Para obtener información más detallada sobre esta funcionalidad, consulte [registro de aplicaciones](app-registration.md).

 

### <a name="deleting-registry-information-during-uninstallation"></a>Eliminar información del registro durante la desinstalación

Al desinstalar una aplicación, los ProgID y la mayoría de la información del registro asociada a esa aplicación deben eliminarse como parte de la desinstalación. Sin embargo, las aplicaciones que han tomado posesión de un tipo de archivo (estableciendo el valor predeterminado de la subclave **\_ \_ raíz**. Extension del tipo de archivo \\  en el identificador de programa de la aplicación) no deben intentar quitar ese valor al desinstalar. Si se dejan los datos en su lugar para el valor predeterminado, se evita la dificultad de determinar si otra aplicación ha tomado posesión del tipo de archivo y se ha sobrescrito el valor predeterminado después de instalar la aplicación original. Windows respeta el valor predeterminado solo si el identificador de programa (ProgID) encuentra un ProgID registrado. Si se anula el registro del ProgID, se omite.

Tenga en cuenta que la información de propiedad de tipo de archivo se almacena en el subárbol de **\_ \_ usuario de HKEY actual** y que también se usa solo cuando se registra la aplicación a la que hace referencia. Por lo tanto, no es necesario quitar estos datos al desinstalar una aplicación.

Como ejemplo, a continuación se muestra el estado del registro antes de que se desinstale una aplicación:

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

A continuación se muestra el estado de las mismas entradas del registro después de desinstalar la aplicación.

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
| Documentos de Office 2007                                                   | . docx,. xlsx y. pptx                                           |
| Documentos de Office 97-2003                                                | . doc,. xls,. ppt                                              |
| Búsqueda guardada                                                            | . Search-MS                                                    |
| Formatos basados en Windows Media (contenedor ASF) | . wmv,. WMA                                                    |
| MP4 (controlador de propiedades)                                                  | . MP4,. m4a,. M4V,. MP4V,. M4P,. M4B,. 3GP,. 3GPP,. 3GP2,. mov |



 

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

[Controladores de tipo de archivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores de programación](fa-progids.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrices de asociación](fa-associationarray.md)
</dt> </dl>

 

 
