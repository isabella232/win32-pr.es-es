---
description: Extender el Portapapeles con controladores de formato de datos personalizados.
title: Cómo crear controladores de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ecc08769068d975c1fa16ef1385f362c67e43c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579569"
---
# <a name="how-to-create-data-handlers"></a>Cómo crear controladores de datos

Cuando un archivo se copia en el Portapapeles o se arrastra y se descarta, el Shell crea un objeto de datos que admite una variedad de formatos estándar [del Portapapeles.](dragdrop.md) Para los archivos que son de un tipo de archivo específico, puede ampliar los formatos de Portapapeles disponibles implementando y registrando un *controlador de datos*. Cuando se transfiere un archivo del tipo de archivo, shell delega las llamadas a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos al controlador de datos si se usa uno de los formatos personalizados.

Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se de abordan en [Creación de controladores de extensión de shell](handlers.md). Este documento se centra en los aspectos de implementación específicos de los controladores de datos.

-   [Implementar controladores de datos](#step-1-implementing-data-handlers)
-   [Registrar controladores de datos](#step-2-registering-data-handlers)
-   [Temas relacionados](#related-topics)

## <a name="instructions"></a>Instructions

### <a name="step-1-implementing-data-handlers"></a>Paso 1: Implementar controladores de datos

Al igual que todos los controladores de extensión de Shell, los controladores de datos son objetos del Modelo de objetos componentes (COM) en proceso implementados como archivos DLL. Exportan dos interfaces además de [**IUnknown:**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).

El shell inicializa el controlador a través de su [**interfaz IPersistFile.**](/windows/win32/api/objidl/nn-objidl-ipersistfile) Usa esta interfaz para solicitar el identificador de clase (CLSID) del controlador y le proporciona el nombre del archivo. Para obtener una explicación general de cómo implementar controladores de extensión de Shell, incluida la **interfaz IPersistFile,** vea [Creating Shell Extension Handlers](handlers.md).

Una vez inicializado el controlador de datos, el Shell delega las llamadas desde el objeto de datos a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del controlador si se usa uno de los formatos personalizados.

### <a name="step-2-registering-data-handlers"></a>Paso 2: Registrar controladores de datos

Los controladores de datos se registran en la subclave *ProgID* del tipo de archivo, como se muestra aquí: **HKEY \_ CLASSES \_ ROOT** \\ *ProgID* \\ **shellex** \\ **DataHandler**

Cree una subclave denominada para el controlador en **DataHandler** y establezca el valor predeterminado de la subclave de ese controlador en el formato de cadena del GUID de CLSID del controlador. Para obtener una explicación general sobre cómo registrar controladores de extensión de Shell, vea [Creating Shell Extension Handlers](handlers.md).

En el ejemplo siguiente se muestran las entradas del Registro que habilitan un controlador de datos para un tipo de archivo .myp de ejemplo.

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

 

 
