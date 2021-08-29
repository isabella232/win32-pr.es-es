---
description: Deshabilita la capacidad de anclar un acceso directo o una ventana a la barra de tareas o al menú Inicio. Esta propiedad también hace que el elemento no sea apto para su inclusión en la lista de menú Inicio la lista De uso más frecuente (MFU).
ms.assetid: 86239BF8-BCFC-4e76-BF94-5ABA4639562C
title: System.AppUserModel.PreventPinning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd697ac59980601e3f7389b9d42c8a01dc63dabe0354ca09795f8ec913a4def5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938655"
---
# <a name="systemappusermodelpreventpinning"></a>System.AppUserModel.PreventPinning

Deshabilita la capacidad de anclar un acceso directo o una ventana a la barra de tareas o **al menú** Inicio. Esta propiedad también hace que el elemento  no sea apto para su inclusión en la lista De uso más frecuente (MFU) del menú Inicio.

Esta propiedad debe establecerse en una ventana antes de la [propiedad \_ AppUserModel \_ ID de PKEY.](./props-system-appusermodel-id.md) Una vez establecida la propiedad AppUserModel ID de PKEY, se omiten los cambios en \_ \_ [PKEY \_ AppUserModel \_ PreventPinning.]()

Para obtener más información sobre los id. de modelo de usuario de aplicación (AppUserModelID) y otros métodos para excluir un elemento de que se ancló a la barra de tareas y de la inclusión de MFU, vea Id. de modelo de usuario de aplicación [(AppUserModelIDs).](../shell/appids.md)

Para establecer esta propiedad en una ventana, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar el almacén de propiedades de la ventana y use los métodos de ese objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperado para establecer la propiedad [System.AppUserModel.PreventPinning]() de esa ventana.

Si establece esta propiedad, se omitirán las siguientes propiedades:

-   [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)
-   [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [System.AppUserModel.RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.PreventPinning
   shellPKey = PKEY_AppUserModel_PreventPinning
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
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

 

 
