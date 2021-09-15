---
description: Cómo excluir una aplicación del cuadro de diálogo Abrir con para el tipo de archivo no asociado.
title: Cómo excluir una aplicación del cuadro de diálogo Abrir con para tipos de archivo no asociados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9443416e95fca112623d487bf58f4fce1d51d13d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468203"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a>Cómo excluir una aplicación del cuadro de diálogo Abrir con para tipos de archivo no asociados

Cuando un usuario intenta abrir un archivo que no es miembro de ningún tipo de archivo registrado (es decir, un tipo de archivo desconocido) o cuando un usuario selecciona **Abrir con** o **Abrir con -> Elegir** programa predeterminado en el menú contextual de un archivo, el Shell presenta un submenú o cuadro de diálogo que permite al usuario especificar el programa utilizado para abrir el archivo.

De forma predeterminada, cualquier aplicación registrada como subclave de **HKEY \_ CLASSES \_ ROOT** Applications se presenta en el \\  **Abrir con** de diálogo. Estas aplicaciones se presentan en **Abrir con** independientemente de si la aplicación está registrada para controlar el tipo de archivo.

Para evitar que una aplicación aparezca en el cuadro de diálogo **Abrir con** cuando la aplicación no se debe o no se puede usar para abrir determinados tipos de archivo, use una de las dos técnicas descritas en este tema.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

Agregue una entrada NoOpenWith a la subclave de la aplicación. Cuando una aplicación usa un tipo de archivo, Windows esa información para compilar la **lista Programas recomendados.** Esta lista se presenta en el **submenú Abrir con** como se muestra en la siguiente captura de pantalla.

![captura de pantalla del menú contextual con el menú abierto con el submenú mostrado](images/file-assoc/openwithsubmenu.png)

Estas aplicaciones recomendadas también se muestran en la parte **Programas** recomendados del **Abrir con** cuadro de diálogo, como se muestra en la siguiente captura de pantalla.

![captura de pantalla del cuadro de diálogo Abrir con programas recomendados](images/file-assoc/openwithdialog.png)

> [!Note]  
> Si una aplicación se ha registrado en [OpenWithList](fa-file-types.md) o OpenWithProgIDs para  el tipo de archivo, aparecerá en la lista Programas recomendados incluso si se establece la entrada NoOpenWith. Además, recuerde que, independientemente de si una aplicación se ofrece en una lista de programas recomendados, un usuario puede examinar manualmente cualquier archivo ejecutable.

 

Las aplicaciones pueden deshabilitar este seguimiento especificando un valor NoOpenWith en la subclave de la aplicación.

La entrada NoOpenWith es un valor **REG \_ SZ** vacío, como se muestra en el ejemplo siguiente.

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

Establecer la entrada NoOpenWith también tiene estos efectos:

-   Impide anclar un archivo al archivo de Lista de accesos directos mediante arrastrar y colocar, a menos que la aplicación esté registrada específicamente para controlar ese tipo de archivo.
-   Impide que el cuadro de diálogo de archivo común y cualquier llamada a la función [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) agreguen cualquier archivo al Lista de accesos directos de la aplicación, a menos que la aplicación esté registrada específicamente para controlar ese tipo de archivo.

### <a name="step-2"></a>Paso 2:

La segunda manera de evitar que una aplicación aparezca en el cuadro de diálogo **Abrir con** es usar la subclave **SupportedTypes** para enumerar explícitamente las extensiones de tipos de archivo que la aplicación puede abrir. Esto evita que la aplicación aparezca en el cuadro **Abrir con** de diálogo para los tipos de archivo que no puede abrir. También hace que la aplicación aparezca en la **lista Programas recomendados** como se ha indicado anteriormente.

Este método es especialmente útil si una aplicación puede guardar un archivo como un tipo de archivo determinado, pero no puede abrir ese tipo de archivo. Una aplicación también debe establecer la marca \_ FOS DONTADDTORECENT a [**través de IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) al llamar al **cuadro de** diálogo Guardar. Esto evita que el elemento se agrega a **las partes** **Recientes** o Frecuentes de un Lista de accesos directos. También impide que se realice un seguimiento de la aplicación [en OpenWithList.](fa-file-types.md)

Cada extensión admitida se agrega como una entrada en la subclave **SupportedTypes,** como se muestra en el ejemplo siguiente. Las entradas son de tipo **REG \_ SZ** o **REG \_ NULL,** sin valores asociados.

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

Si se proporciona una subclave **SupportedTypes,** solo los archivos con esas extensiones son aptos para anclarse al  Lista de accesos directos  de la aplicación o para que se realice un seguimiento en la lista De destinos recientes o frecuentes de una aplicación.

La entrada NoOpenWith invalida la subclave **SupportedTypes** y oculta la aplicación en el **Abrir con** diálogo.

 

 
