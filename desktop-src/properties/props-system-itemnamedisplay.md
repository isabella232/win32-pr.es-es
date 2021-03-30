---
description: El nombre para mostrar en &\# 0034; el formulario más completo&\# 0034;.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf735935ee7971acad7d11ee91636e18a6542252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810982"
---
# <a name="systemitemnamedisplay"></a>System.ItemNameDisplay

El nombre para mostrar en el formulario "más completo". Es la representación única del nombre del elemento más adecuada para los usuarios finales.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemNameDisplay
   shellPKey = PKEY_ItemNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 10
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

Este valor es concatentation de [System. ItemNamePrefix](./props-system-itemnameprefix.md) y [System. itemname](./props-system-itemname.md).

Si el elemento es un archivo, esta propiedad incluye el nombre para mostrar tal como se muestra en el explorador de archivos. Hay casos aceptables cuando se proporciona [System. FileName](./props-system-filename.md) pero el valor de esta propiedad es completamente diferente. Los mensajes de correo electrónico son un buen ejemplo. Si el elemento es un mensaje de correo electrónico, el nombre del elemento es normalmente el asunto. En ese caso, el valor debe ser la concatenación de [System. ItemNamePrefix](./props-system-itemnameprefix.md) y [System. itemname](./props-system-itemname.md). Dado que el valor de System. ItemNamePrefix excluye los espacios finales, la concatenación debe incluir un espacio al generar [System. ItemNameDisplay](). Tenga en cuenta que no se garantiza que esta propiedad sea única, sino que está diseñada para promocionar el candidato más probable que puede ser único y que también tenga sentido para los usuarios finales.

Por ejemplo, para los documentos, el [nombre System. title](./props-system-title.md) podría usarse como [System. ItemNameDisplay](), pero en la práctica el título de los documentos puede no ser útil o lo suficientemente exclusivo como para funcionar como System. ItemNameDisplay. En su lugar, proporcionar [System. FileName](./props-system-filename.md) como el valor de System. ItemNameDisplay es una opción mejor. En Windows Mail, el correo electrónico se almacena en el sistema de archivos como archivos. eml. Los valores System. FileName para esos archivos no son descriptivos, ya que son GUID. En este ejemplo, la promoción de [System. Subject](./props-system-subject.md) como System. ItemNameDisplay tiene más sentido.

**Notas de compatibilidad:**

-   Implementaciones de carpetas de Shell en Windows Vista: Use PKEY \_ ItemNameDisplay para la columna nombre cuando desee que el explorador de Windows llame a [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN \_ normal) para obtener el valor del nombre. Use otro PKEY, como PKEY \_ itemname, cuando desee que el explorador de Windows llame al almacén de propiedades de la carpeta o [**IShellFolder2:: GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) para obtener el valor del nombre.
-   Implementaciones de carpetas de Shell en Windows XP: la primera columna debe ser la columna Name y el explorador de Windows llama a [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para obtener el valor del nombre. PKEY/SCID no importa.



| Tipo de elemento     | Ejemplo                   |
|---------------|---------------------------|
| Archivo          | hello.txt                 |
| Message       | Re: ¿Dónde está la reunión? |
| Carpeta de dispositivo | Song. WMA                  |
| Carpeta        | Documentos                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

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

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[Consulta](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
