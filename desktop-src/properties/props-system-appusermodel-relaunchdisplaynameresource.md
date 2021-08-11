---
description: Especifica el nombre para mostrar que se usa para el acceso directo creado en la barra de tareas cuando el usuario decide anclar una aplicación a la barra de tareas o iniciar una nueva instancia a través del botón Lista de accesos directos.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System.AppUserModel.RelaunchDisplayNameResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b0af752fb345dd5dd5f1b091a22255e856031affaca266ff6307045f148cd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233027"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a>System.AppUserModel.RelaunchDisplayNameResource

Especifica el nombre para mostrar que se usa para el acceso directo creado en la barra de tareas cuando el usuario decide anclar una aplicación a la barra de tareas o iniciar una nueva instancia a través del botón Lista de accesos directos. El valor de esta propiedad debe ser uno de los siguientes:

-   Una cadena de recursos indirectos como "@%systemdir% \\ system32 \\shell32.dll,-19263". Tenga en cuenta que el carácter "@" es necesario para distinguir una cadena indirecta de una cadena de texto sin formato (que se describe en el siguiente párrafo con viñetas). Esta cadena indirecta consta de un archivo binario y un identificador de recurso de la cadena contenida en ese archivo binario. Se recomienda encarecidamente usar este formulario de cadena indirecta, que garantiza que el nombre para mostrar cambie correctamente cuando el idioma del sistema cambie a través del Interfaz de usuario multilingüe ( Carácter "-" antes de que se requiera el identificador de recurso.
-   Cadena de texto sin formato que no apunta a un recurso. Esto solo se debe usar cuando el nombre para mostrar se calcula u obtiene dinámicamente de un origen de datos que no es compatible con LAN. Por ejemplo, la cadena podría ser el nombre de un dispositivo, como "Microsoft Zune", en los casos en los que la aplicación aparece cuando ese dispositivo está conectado al equipo.

> [!Note]  
> [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) y [System.AppUserModel.RelaunchDisplayNameResource]() siempre deben establecerse juntos. Si no se establece ninguna de esas propiedades, no se usa ninguna.

 

Esta propiedad solo se usa si una ventana tiene un identificador de modelo de usuario de aplicación explícito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), establecido a través de [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Si la ventana no tiene un AppUserModelID explícito, esta propiedad se omite y la ventana se agrupa y ancla como si formara parte del proceso que la posee. Para obtener más información sobre la aplicación de appUserModelID explícitos y su efecto en la anclación de la barra de tareas, vea Id. de modelo de usuario de aplicación [(AppUserModelID).](../shell/appids.md) Esta propiedad está pensada para que la utilicen las aplicaciones o ventanas que desean proporcionar información de reinició no predeterminada. Para obtener más información, [vea System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).

> [!Note]  
> Esta propiedad se omite si [se establece System.AppUserModel.PreventPinning.](./props-system-appusermodel-preventpinning.md) Esto permite que una aplicación controle la agrupación de sus ventanas asignándolos appUserModelID explícitos, pero evitando que esas ventanas se anclaran.

 

Para establecer esta propiedad en una ventana, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar el almacén de propiedades de la ventana y use los métodos de ese objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperado para establecer la propiedad [System.AppUserModel.RelaunchDisplayNameResource]() de esa ventana.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchDisplayNameResource
   shellPKey = PKEY_AppUserModel_RelaunchDisplayNameResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a>Comentarios

Los valores PKEY se definen en Propkey.h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Id. de modelo de usuario de aplicación (AppUserModelID)](../shell/appids.md)
</dt> <dt>

[System.AppUserModel.ID](./props-system-appusermodel-id.md)
</dt> <dt>

[propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[aliasInfo](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[enum](./propdesc-schema-enum.md)
</dt> <dt>

[enumRange](./propdesc-schema-enumrange.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[relatedProperty](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
