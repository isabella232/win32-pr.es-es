---
description: Cómo excluir una aplicación del cuadro de diálogo Abrir con para el tipo de archivo no asociado.
title: Cómo excluir una aplicación del cuadro de diálogo Abrir con para tipos de archivo no asociados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9443416e95fca112623d487bf58f4fce1d51d13d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561121"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a>Cómo excluir una aplicación del cuadro de diálogo Abrir con para tipos de archivo no asociados

Cuando un usuario intenta abrir un archivo que no es miembro de ningún tipo de archivo registrado (es decir, un tipo de archivo desconocido) o cuando un usuario selecciona **abrir con** o **abrir con-> elegir programa predeterminado** en el menú contextual de un archivo, el shell presenta un submenú o un cuadro de diálogo que permite al usuario especificar el programa que se usa para abrir el archivo.

De forma predeterminada, todas las aplicaciones registradas como subclaves de las aplicaciones **\_ \_ raíz de clases HKEY** \\  se presentan en el cuadro de diálogo **abrir con** . Estas aplicaciones se presentan en **abierto con** independencia de si la aplicación está registrada para controlar el tipo de archivo.

Para evitar que una aplicación aparezca en el cuadro de diálogo **abrir con** cuando la aplicación no debe o no se puede usar para abrir determinados tipos de archivo, utilice una de las dos técnicas descritas en este tema.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Agregue una entrada NoOpenWith a la subclave de la aplicación. Cuando una aplicación utiliza un tipo de archivo, Windows registra esa información para generar la lista de **Programas recomendados** . Esta lista se presenta en el submenú **abrir con** , como se muestra en la siguiente captura de pantalla.

![captura de pantalla del menú contextual con el submenú abrir con mostrado](images/file-assoc/openwithsubmenu.png)

Estas aplicaciones recomendadas también se muestran en la parte **Programas recomendados** del cuadro de diálogo **abrir con** , como se muestra en la siguiente captura de pantalla.

![captura de pantalla del cuadro de diálogo Abrir con con los programas recomendados](images/file-assoc/openwithdialog.png)

> [!Note]  
> Si una aplicación se ha registrado en [OpenWithList](fa-file-types.md) o OpenWithProgIDs para el tipo de archivo, aparecerá en la lista de **Programas recomendados** aunque se establezca la entrada NoOpenWith. Además, recuerde que, independientemente de si una aplicación se ofrece en una lista de programas recomendados, un usuario puede examinar manualmente cualquier archivo ejecutable.

 

Las aplicaciones pueden deshabilitar este seguimiento especificando un valor de NoOpenWith en la subclave de la aplicación.

La entrada NoOpenWith es un valor **reg \_ SZ** vacío tal y como se muestra en el ejemplo siguiente.

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

La configuración de la entrada NoOpenWith también tiene estos efectos:

-   Impide anclar un archivo a la Jump List de la aplicación a través de la función de arrastrar y colocar, a menos que la aplicación se registre específicamente para controlar ese tipo de archivo.
-   Impide que el cuadro de diálogo archivo común y las llamadas a la función [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) agreguen cualquier archivo a la Jump List de la aplicación, a menos que la aplicación se registre específicamente para administrar ese tipo de archivo.

### <a name="step-2"></a>Paso 2:

La segunda manera de impedir que una aplicación aparezca en el cuadro de diálogo **abrir con** es usar la subclave **SupportedTypes** para enumerar explícitamente las extensiones de los tipos de archivo que la aplicación puede abrir. Esto evita que la aplicación aparezca en el cuadro de diálogo **abrir con** para los tipos de archivo que no se pueden abrir. También hace que la aplicación aparezca en la lista de **Programas recomendados** , tal como se explicó anteriormente.

Este método es especialmente útil si una aplicación puede guardar un archivo como un tipo de archivo determinado pero no puede abrir ese tipo de archivo. Una aplicación también debe establecer la marca de FOS \_ DONTADDTORECENT a través de [**IFileDialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) al llamar al cuadro de diálogo **Guardar** . Esto evita que se agregue el elemento a las partes **recientes** o **frecuentes** de una Jump List. También impide que se realice un seguimiento de la aplicación en [OpenWithList](fa-file-types.md).

Cada extensión admitida se agrega como una entrada en la subclave **SupportedTypes** , tal y como se muestra en el ejemplo siguiente. Las entradas son del tipo **reg \_ SZ** o **reg \_ null**, sin valores asociados.

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

Si se proporciona una subclave **SupportedTypes** , solo los archivos con esas extensiones son válidos para el anclaje a la Jump List de la aplicación o para que se realice el seguimiento en la lista de destinos **recientes** o **frecuentes** de una aplicación.

La entrada NoOpenWith invalida la subclave **SupportedTypes** y oculta la aplicación en el cuadro de diálogo **abrir con** .

 

 
