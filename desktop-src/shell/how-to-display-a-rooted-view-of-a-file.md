---
description: Puede usar una extensión de espacio de nombres para permitir a los usuarios examinar el contenido de un archivo en lugar de presentarlo como una carpeta. Las extensiones de este tipo se usan normalmente para mostrar el contenido de los miembros de un tipo de archivo.
title: Cómo mostrar una vista raíz de un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c91e17ef12393b1a95316c37a18d51876cf988293c330610a3638c7995ab12a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596585"
---
# <a name="how-to-display-a-rooted-view-of-a-file"></a>Cómo mostrar una vista raíz de un archivo

Puede usar una extensión de espacio de nombres para permitir a los usuarios examinar el contenido de un archivo en lugar de presentarlo como una carpeta. Las extensiones de este tipo se usan normalmente para mostrar el contenido de los miembros de un [tipo de archivo](fa-file-types.md). Por ejemplo, los miembros de un tipo de archivo pueden contener varios archivos comprimidos o imágenes, organizados en una jerarquía. En lugar de escribir una aplicación para permitir al usuario ver el contenido de un archivo de este tipo, en su lugar puede escribir una extensión de espacio de nombres y dejar que Windows Explorer controle la presentación.

Debe usar una vista con raíz para que una extensión muestre el contenido de un archivo. La manera más común de proporcionar una vista raíz de [](context.md) los miembros de un tipo de archivo es definir un verbo de menú contextual que inicie una instancia de Explorer.exe. Al convertir este verbo en el verbo predeterminado, al hacer doble clic también se abrirá una vista raíz del archivo. Puede definir un verbo para todos los miembros del tipo de archivo modificando el Registro [o](context.md)definir dinámicamente verbos de archivo [a](context-menu-handlers.md)archivo mediante la implementación de un controlador de menú contextual .

## <a name="instructions"></a>Instructions


En el ejemplo siguiente se muestra cómo usar el Registro para proporcionar una vista raíz de los miembros de un tipo de archivo modificando el registro. La entrada del Registro de ejemplo es una modificación de uno de los ejemplos de [Extensión de menús contextuales](context.md). Las entradas del Registro definen archivos con una extensión de nombre de archivo .myp como un tipo de archivo y usan el **verbo** examinar para iniciar una vista raíz de los miembros de ese tipo.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = browse
         browse
            command
               (Default) = %SYSTEMROOT%\explorer.exe /e,/root,{Extension CLSID}, "%1"
```

Puede usar el mismo verbo para iniciar mediante programación una vista raíz de un miembro del tipo de archivo llamando a la [**función ShellExecute.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificar la ubicación de una extensión de espacio de nombres](nse-junction.md)
</dt> <dt>

[Cómo abrir una vista con raíz de un punto de unión a través del Registro](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[Cómo abrir una vista raíz de un punto de unión a través de un archivo de acceso directo](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



