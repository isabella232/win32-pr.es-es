---
description: Cómo implementar y registrar un controlador de colocación.
title: Cómo crear controladores de colocación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34c06aa3eae1892b5b86ce3a0f3b1198be41cd2f9dda5c9bd0956b40a53146e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223589"
---
# <a name="how-to-create-drop-handlers"></a>Cómo crear controladores de colocación

De forma predeterminada, los archivos no son destinos de colocación. Puede convertir los miembros de un tipo [de archivo](fa-file-types.md) en destinos de colocación implementando y registrando un controlador *de colocación*.

Si se registra un controlador de colocación para un tipo de archivo, se llama a él cada vez que se arrastra o se coloca un objeto en un miembro del tipo de archivo. Shell administra la operación llamando a los métodos adecuados en la [**interfaz IDropTarget del**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) controlador.

Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se de abordan en [Crear controladores de extensión de shell](handlers.md). Este documento se centra en los aspectos de implementación específicos de los controladores de colocación.

## <a name="instructions"></a>Instrucciones

### <a name="step-1-implementing-drop-handlers"></a>Paso 1: Implementar controladores de eliminación

Al igual que todos los controladores de extensión de Shell, los controladores de colocación son objetos del Modelo de objetos componentes (COM) en proceso implementados como archivos DLL. Exportan dos interfaces además de [**IUnknown:**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

El shell inicializa el controlador a través de su [**interfaz IPersistFile.**](/windows/win32/api/objidl/nn-objidl-ipersistfile) Usa esta interfaz para solicitar el identificador de clase (CLSID) del controlador y le proporciona el nombre del archivo. Para obtener una explicación general de cómo implementar controladores de extensión de Shell, incluida la **interfaz IPersistFile,** vea [Creating Shell Extension Handlers](handlers.md).

Una vez inicializado el controlador de colocación, el Shell llama al método adecuado en la [**interfaz IDropTarget del**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) controlador.

### <a name="step-2-registering-drop-handlers"></a>Paso 2: Registrar controladores de eliminación

Los controladores de colocación se registran en la subclave de este tipo de archivo.

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

Cree una subclave de **DropHandler** denominada para el controlador y establezca el valor predeterminado de la subclave en el formato de cadena del GUID de CLSID del controlador. Para obtener una explicación general de cómo registrar controladores de extensión de Shell, vea [Creating Shell Extension Handlers](handlers.md).

En el ejemplo siguiente se muestran las entradas del Registro que habilitan un controlador de colocación para un tipo de archivo .myp de ejemplo.

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

 

 
