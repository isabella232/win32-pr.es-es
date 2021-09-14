---
description: Especifica un comando que se puede ejecutar a través de ShellExecute para iniciar una aplicación cuando se ancla a la barra de tareas o cuando se inicia una nueva instancia de la aplicación a través de la aplicación Lista de accesos directos.
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: System.AppUserModel.RelaunchCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84049f605896ba5e99a98f33557e6ee4dea37df5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360672"
---
# <a name="systemappusermodelrelaunchcommand"></a>System.AppUserModel.RelaunchCommand

Especifica un comando que se puede ejecutar a través de [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) para iniciar una aplicación cuando se ancla a la barra de tareas o cuando se inicia una nueva instancia de la aplicación a través de la aplicación Lista de accesos directos.

Entre otros, se incluyen los siguientes ejemplos:


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



Esta propiedad solo se usa si una ventana tiene un identificador de modelo de usuario de aplicación explícito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), establecido a través de [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Si la ventana no tiene un AppUserModelID explícito, esta propiedad se omite y la ventana se agrupa y ancla como si formara parte del proceso que la posee. Para obtener más información sobre la aplicación de appUserModelID explícitos y su efecto en la anclación de la barra de tareas, vea Application [User Model IDs (AppUserModelIDs)](../shell/appids.md)( Id. de modelo de usuario de aplicación [AppUserModelID]).

Esta propiedad está pensada para que la utilicen las aplicaciones o ventanas que desean proporcionar información de reinició no predeterminada.

> [!Note]  
> [System.AppUserModel.RelaunchCommand]() y [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) siempre deben establecerse juntos. Si no se establece ninguna de esas propiedades, no se usa ninguna.

 

Esta propiedad, junto con [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) y [System.AppUserModel.RelaunchIconResource,](./props-system-appusermodel-relaunchiconresource.md) se puede usar para definir visualmente una ventana como una aplicación para el usuario. Esto es útil para escenarios de aplicación host, donde una única instancia de host ejecuta varias aplicaciones secundarias. Por ejemplo, una máquina virtual que hospeda varias aplicaciones virtualizadas podría querer que esas aplicaciones virtualizadas aparezcan como aplicaciones individuales para el usuario. La máquina virtual podría etiquetar cada ventana con un AppUserModelID explícito y las propiedades de reinició adecuadas para que aparezcan como aplicaciones. A continuación, el usuario podría anclarlos a la barra de tareas y "volver a iniciar" la instancia anclada.

> [!Note]  
> Esta propiedad se omite si [se establece System.AppUserModel.PreventPinning.](./props-system-appusermodel-preventpinning.md) Esto permite que una aplicación controle la agrupación de sus ventanas asignándolos appUserModelID explícitos, pero evitando que esas ventanas se anclaran.

 

Para establecer esta propiedad en una ventana, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar el almacén de propiedades de la ventana y use los métodos de ese objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperado para establecer la propiedad [System.AppUserModel.RelaunchCommand]() de esa ventana.

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

 

 
