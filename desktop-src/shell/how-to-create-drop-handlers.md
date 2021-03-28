---
description: Cómo implementar y registrar un controlador de colocación.
title: Cómo crear controladores de colocación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b4349ba36a12670458a453b0622475d59d755
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276750"
---
# <a name="how-to-create-drop-handlers"></a>Cómo crear controladores de colocación

De forma predeterminada, los archivos no son destinos de colocación. Puede convertir los miembros de un [tipo de archivo](fa-file-types.md) en destinos de colocación implementando y registrando un *controlador de colocación*.

Si se registra un controlador de colocación para un tipo de archivo, se llama a este método cada vez que se arrastra un objeto o se coloca en un miembro del tipo de archivo. El shell administra la operación mediante una llamada a los métodos adecuados en la interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) del controlador.

Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se explican en [crear controladores de extensión de Shell](handlers.md). Este documento se centra en los aspectos de implementación que son específicos de los controladores de destino.

## <a name="instructions"></a>Instrucciones

### <a name="step-1-implementing-drop-handlers"></a>Paso 1: implementar controladores de colocación

Al igual que todos los controladores de extensión de Shell, los controladores de colocación son objetos de modelo de objetos componentes (COM) en proceso implementados como archivos dll. Exportan dos interfaces además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) y [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

El shell inicializa el controlador a través de su interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Utiliza esta interfaz para solicitar el identificador de clase (CLSID) del controlador y proporciona el nombre del archivo. Para obtener información general sobre cómo implementar controladores de extensión de Shell, incluida la interfaz **IPersistFile** , vea [crear controladores de extensión de Shell](handlers.md).

Una vez inicializado el controlador de colocación, el shell llama al método adecuado en la interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) del controlador.

### <a name="step-2-registering-drop-handlers"></a>Paso 2: registrar controladores de colocación

Los controladores de colocación se registran en la subclave de este tipo de archivo.

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

Cree una subclave de **DropHandler** denominada para el controlador y establezca el valor predeterminado de la subclave en la forma de cadena del GUID de CLSID del controlador. Para obtener información general sobre cómo registrar controladores de extensión de Shell, vea [crear controladores de extensión de Shell](handlers.md).

En el ejemplo siguiente se muestran las entradas del registro que habilitan un controlador de colocación para un tipo de archivo. MYP de ejemplo.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         DropHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de controladores de extensiones de shell](handlers.md)
</dt> <dt>

[**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
