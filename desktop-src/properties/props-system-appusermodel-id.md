---
description: Identificador de modelo de usuario de aplicación explícito (AppUserModelID) que se usa para asociar procesos, archivos y ventanas a una aplicación determinada.
ms.assetid: 07858b3c-e601-40ec-a87a-d66612d5473a
title: System.AppUserModel.ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd60b64598a620221ec2b610b10cbc05002f38aaf633e51e788b24797620cab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033743"
---
# <a name="systemappusermodelid"></a>System.AppUserModel.ID

Identificador de modelo de usuario de aplicación explícito (AppUserModelID) que se usa para asociar procesos, archivos y ventanas a una aplicación determinada. En algunos casos, es suficiente confiar en el AppUserModelID interno asignado a un proceso por el sistema. Sin embargo, una aplicación que posee varios procesos o una aplicación que se ejecuta en un proceso host podría necesitar identificarse explícitamente a través de esta propiedad para que pueda agrupar sus ventanas dispares en un solo botón de la barra de tareas y controlar el contenido de la aplicación Lista de accesos directos.

Para establecer esta propiedad en una ventana, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar el almacén de propiedades de la ventana y use los métodos de ese objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperado para establecer la propiedad [System.AppUserModel.ID]() de esa ventana.

Para obtener más información, [vea Application User Model IDs (AppUserModelIDs) ( Id. de modelo de usuario de aplicación [AppUserModelID]).](../shell/appids.md)

En el momento en [System.AppUserModel.ID]() se establece la propiedad , se notifica a la barra de tareas que actualice su información en la ventana o acceso directo dado que AppUserModelID.

Se pueden usar otras propiedades de ventana y acceso directo junto con un AppUserModelID explícito para controlar aún más la agrupación y el anclar asociados a una ventana, el nombre para mostrar y el icono que se usa para ella en la barra de tareas y el comando para iniciar una aplicación anclada a la barra de tareas o una nueva instancia de la aplicación a través del Lista de accesos directos de esa aplicación. Estas propiedades deben establecerse antes de establecer la [System.AppUserModel.ID]() propiedad . Para obtener más información, vea los temas siguientes:

-   [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md)
-   [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)
-   [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [System.AppUserModel.RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.ID
   shellPKey = PKEY_AppUserModel_ID
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 5
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

[**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
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

 

 
