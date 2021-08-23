---
description: Especifica el icono que se usa para el acceso directo creado en la barra de tareas cuando el usuario decide anclar una aplicación a la barra de tareas o iniciar una nueva instancia a través del botón Lista de accesos directos.
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: System.AppUserModel.RelaunchIconResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b43394bd5ee7dca6084526224dac268500f6881317215d63d6fc0e9a126c5b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970844"
---
# <a name="systemappusermodelrelaunchiconresource"></a>System.AppUserModel.RelaunchIconResource

Especifica el icono que se usa para el acceso directo creado en la barra de tareas cuando el usuario decide anclar una aplicación a la barra de tareas o iniciar una nueva instancia a través del botón Lista de accesos directos. Este es el icono que se usa para el grupo de la barra de tareas y se muestra para una aplicación anclada independientemente de si esa aplicación se está ejecutando o no. Debe especificarse en uno de los siguientes formatos:

-   Formato de recurso estándar, como "%systemdir% \\ system32 \\shell32.dll,-128". Carácter "-" antes de que se requiera el identificador de recurso. No use el carácter '@' al frente de la cadena de ruta de acceso.
-   Ruta de acceso directa a un archivo de icono, como "%programfiles% \\ Microsoft \\ Bloc de notas \\ Bloc de notas.ico,0". Tenga en cuenta que, dado que los archivos .ico pueden contener varios recursos de icono, se requiere un identificador de recurso en la cadena. Si el archivo .ico es una sola imagen, use "0" (sin el carácter "-") como identificador de recurso.

[System.AppUserModel.RelaunchIconResource]() es una propiedad opcional. Si no se establece, se usa el icono del destino del comando relaunch ([System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)). Sin embargo, dado que esto puede dar lugar a resultados no deseados, le recomendamos encarecidamente que proporcione un icono explícitamente a través de esta propiedad.

Esta propiedad solo se usa si una ventana tiene un identificador de modelo de usuario de aplicación explícito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), establecido a través de [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Si la ventana no tiene un AppUserModelID explícito (System.AppUserModel.ID), esta propiedad se omite y la ventana se agrupa y ancla como si formara parte de su proceso de propietario. Para obtener más información sobre la aplicación de appUserModelID explícitos y su efecto en la anclación de la barra de tareas, vea Id. de modelo de usuario de aplicación [(AppUserModelIDs).](../shell/appids.md) Esta propiedad está pensada para que la utilicen las aplicaciones o ventanas que desean proporcionar información de reinició no predeterminada. Para obtener más información, [vea System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).

Si se establece un AppUserModelID explícito en la ventana, pero esta propiedad no está establecida, el sistema intenta encontrar un acceso directo con el mismo AppUserModelID y ancla ese acceso directo a la barra de tareas para representar la ventana. Si no se puede encontrar ningún acceso directo de este tipo, se usa el ejecutable de respaldo del proceso que lo posee.

> [!Note]  
> Esta propiedad se omite si [se establece System.AppUserModel.PreventPinning.](./props-system-appusermodel-preventpinning.md) Esto permite que una aplicación controle la agrupación de sus ventanas asignándolos appUserModelID explícitos, pero evitando que esas ventanas se anclaran.

 

Para establecer esta propiedad en una ventana, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar el almacén de propiedades de la ventana y use los métodos de ese objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperado para establecer la propiedad [System.AppUserModel.RelaunchIconResource]() de esa ventana.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="windows-8-windows-7"></a>Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

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

 

 
