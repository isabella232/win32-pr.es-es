---
description: Extender el Portapapeles con controladores de formato de datos personalizados.
title: Cómo crear controladores de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ecc08769068d975c1fa16ef1385f362c67e43c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997709"
---
# <a name="how-to-create-data-handlers"></a>Cómo crear controladores de datos

Cuando un archivo se copia en el portapapeles o se arrastra y se coloca, el shell crea un objeto de datos que admite diversos formatos estándar del [portapapeles](dragdrop.md). En el caso de los archivos que son de un tipo de archivo específico, puede ampliar los formatos de Portapapeles disponibles implementando y registrando un *controlador de datos*. Cuando se transfiere un archivo del tipo de archivo, el shell delega las llamadas a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos al controlador de datos si se usa uno de los formatos personalizados.

Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se explican en [crear controladores de extensión de Shell](handlers.md). Este documento se centra en los aspectos de la implementación que son específicos de los controladores de datos.

-   [Implementar controladores de datos](#step-1-implementing-data-handlers)
-   [Registrar controladores de datos](#step-2-registering-data-handlers)
-   [Temas relacionados](#related-topics)

## <a name="instructions"></a>Instrucciones

### <a name="step-1-implementing-data-handlers"></a>Paso 1: implementación de controladores de datos

Al igual que todos los controladores de extensión de Shell, los controladores de datos son objetos del modelo de objetos componentes (COM) en proceso implementados como archivos dll. Exportan dos interfaces además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) y [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).

El shell inicializa el controlador a través de su interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Utiliza esta interfaz para solicitar el identificador de clase (CLSID) del controlador y proporciona el nombre del archivo. Para obtener información general sobre cómo implementar controladores de extensión de Shell, incluida la interfaz **IPersistFile** , vea [crear controladores de extensión de Shell](handlers.md).

Una vez inicializado el controlador de datos, el shell delega las llamadas desde el objeto de datos a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del controlador si se usa uno de los formatos personalizados.

### <a name="step-2-registering-data-handlers"></a>Paso 2: registrar controladores de datos

Los controladores de datos se registran en la subclave *ProgID* del tipo de archivo, como se muestra aquí: **HKEY \_ classes \_ root** \\ *ProgID* \\ **shellex** \\  .

Cree una subclave denominada para el controlador en el **identificador** de objeto y establezca el valor predeterminado de la subclave de ese controlador en la forma de cadena del GUID de CLSID del controlador. Para obtener información general sobre cómo registrar controladores de extensión de Shell, vea [crear controladores de extensión de Shell](handlers.md).

En el ejemplo siguiente se muestran las entradas del registro que habilitan un controlador de datos para un tipo de archivo. MYP de ejemplo.

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
      Shellex
         DataHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de controladores de extensiones de shell](handlers.md)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 
