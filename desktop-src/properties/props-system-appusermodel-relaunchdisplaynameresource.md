---
description: Especifica el nombre para mostrar utilizado para el acceso directo creado en la barra de tareas cuando el usuario elige anclar una aplicación a la barra de tareas o iniciar una nueva instancia a través de la Jump List del botón.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System. AppUserModel. RelaunchDisplayNameResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79c22d0ccecb8bac86fe5ca3636ed10ed2ca50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276904"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a>System. AppUserModel. RelaunchDisplayNameResource

Especifica el nombre para mostrar utilizado para el acceso directo creado en la barra de tareas cuando el usuario elige anclar una aplicación a la barra de tareas o iniciar una nueva instancia a través de la Jump List del botón. El valor de esta propiedad debe ser uno de los siguientes:

-   Cadena de recursos indirecta como "@% systemdir% \\ system32 \\shell32.dll,-19263". Tenga en cuenta que el carácter ' @ ' es necesario para distinguir una cadena indirecta de una cadena de texto sin formato (descrita en el párrafo siguiente con viñetas). Esta cadena indirecta se compone de un archivo binario y un identificador de recurso de la cadena contenida en ese binario. Se recomienda encarecidamente que utilice esta forma de cadena indirecta, lo que garantiza que el nombre para mostrar cambie correctamente cuando se cambie el idioma del sistema a través de la interfaz de usuario multilingüe (MUI). El carácter "-" antes del identificador de recurso es obligatorio.
-   Cadena de texto sin formato que no señala a un recurso. Solo se debe usar cuando el nombre para mostrar se calcula o se obtiene dinámicamente a partir de un origen de datos que no admite MUI. Por ejemplo, la cadena podría ser el nombre de un dispositivo, como "Microsoft Zune", en los casos en los que la aplicación aparece cuando el dispositivo está conectado al equipo.

> [!Note]  
> [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) y [System. AppUserModel. RelaunchDisplayNameResource]() siempre se deben establecer juntos. Si no se establece una de esas propiedades, no se utiliza ninguna.

 

Esta propiedad solo se usa si una ventana tiene un identificador de modelo de usuario de aplicación explícito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), establecido a través de [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Si la ventana no tiene un AppUserModelID explícito, esta propiedad se omite y la ventana se agrupa y se ancla como si formara parte del proceso que la posee. Para obtener más información sobre la aplicación de AppUserModelIDs explícitos y su efecto en el anclaje de la barra de tareas, vea [identificadores de modelo de usuario de la aplicación (AppUserModelIDs)](../shell/appids.md). Esta propiedad está pensada para ser utilizada por aplicaciones o ventanas que deseen proporcionar información de reinicio no predeterminada. Para obtener más información, vea [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).

> [!Note]  
> Esta propiedad se omite si se establece [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) . Esto permite que una aplicación controle la agrupación de sus ventanas asignándoles explícitamente AppUserModelIDs, pero evitando que esas ventanas se anclen.

 

Para establecer esta propiedad en una ventana, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar el almacén de propiedades de la ventana y use los métodos de ese objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperado para establecer la propiedad [System. AppUserModel. RelaunchDisplayNameResource]() de esa ventana.

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

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)](../shell/appids.md)
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

[Requerida](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[aliasInfo](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[Numérico](./propdesc-schema-numberformat.md)
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

[Consulta](./propdesc-schema-querycontrol.md)
</dt> <dt>

[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[relatedProperty](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
