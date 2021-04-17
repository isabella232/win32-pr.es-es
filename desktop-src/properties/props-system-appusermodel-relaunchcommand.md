---
description: Especifica un comando que se puede ejecutar a través de ShellExecute para iniciar una aplicación cuando está anclada a la barra de tareas o cuando se inicia una nueva instancia de la aplicación a través de la Jump List de la aplicación.
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: System. AppUserModel. RelaunchCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84049f605896ba5e99a98f33557e6ee4dea37df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706111"
---
# <a name="systemappusermodelrelaunchcommand"></a>System. AppUserModel. RelaunchCommand

Especifica un comando que se puede ejecutar a través de [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) para iniciar una aplicación cuando está anclada a la barra de tareas o cuando se inicia una nueva instancia de la aplicación a través de la Jump List de la aplicación.

Entre otros, se incluyen los siguientes ejemplos:


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



Esta propiedad solo se usa si una ventana tiene un identificador de modelo de usuario de aplicación explícito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), establecido a través de [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Si la ventana no tiene un AppUserModelID explícito, esta propiedad se omite y la ventana se agrupa y se ancla como si formara parte del proceso que la posee. Para obtener más información sobre la aplicación de AppUserModelIDs explícitos y su efecto en el anclaje de la barra de tareas, vea [identificadores de modelo de usuario de la aplicación (AppUserModelIDs)](../shell/appids.md).

Esta propiedad está pensada para ser utilizada por aplicaciones o ventanas que deseen proporcionar información de reinicio no predeterminada.

> [!Note]  
> [System. AppUserModel. RelaunchCommand]() y [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) siempre se deben establecer juntos. Si no se establece una de esas propiedades, no se utiliza ninguna.

 

Esta propiedad, junto con [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) y [System. AppUserModel. RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) se puede usar para definir visualmente una ventana como una aplicación para el usuario. Esto resulta útil para escenarios de aplicaciones host, donde una sola instancia de host ejecuta varias aplicaciones secundarias. Por ejemplo, una máquina virtual que hospede varias aplicaciones virtualizadas podría querer que esas aplicaciones virtualizadas aparezcan como aplicaciones individuales para el usuario. La máquina virtual podría etiquetar cada ventana con un AppUserModelID explícito y las propiedades de reinicio adecuadas para que aparezcan como aplicaciones. Después, el usuario podría anclarlos a la barra de tareas y "volver a iniciar" la instancia anclada.

> [!Note]  
> Esta propiedad se omite si se establece [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) . Esto permite que una aplicación controle la agrupación de sus ventanas asignándoles explícitamente AppUserModelIDs, pero evitando que esas ventanas se anclen.

 

Para establecer esta propiedad en una ventana, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar el almacén de propiedades de la ventana y use los métodos de ese objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperado para establecer la propiedad [System. AppUserModel. RelaunchCommand]() de esa ventana.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchCommand
   shellPKey = PKEY_AppUserModel_RelaunchCommand
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 2
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

 

 
