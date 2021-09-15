---
description: El nombre para mostrar &\# formulario 0034;most complete&\# 0034;.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf735935ee7971acad7d11ee91636e18a6542252
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466283"
---
# <a name="systemitemnamedisplay"></a>System.ItemNameDisplay

Nombre para mostrar en formato "más completo". Es la representación única del nombre del elemento más adecuada para los usuarios finales.

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

Los valores PKEY se definen en Propkey.h.

Este valor es la concatentación de [System.ItemNamePrefix](./props-system-itemnameprefix.md) y [System.ItemName](./props-system-itemname.md).

Si el elemento es un archivo, esta propiedad incluye el nombre para mostrar como se muestra en Explorador de archivos. Hay casos aceptables cuando [se proporciona System.FileName,](./props-system-filename.md) pero el valor de esta propiedad es completamente diferente. Los mensajes de correo electrónico son un buen ejemplo. Si el elemento es un mensaje de correo electrónico, el nombre del elemento suele ser el asunto. En ese caso, el valor debe ser la concatenación de [System.ItemNamePrefix](./props-system-itemnameprefix.md) y [System.ItemName](./props-system-itemname.md). Puesto que el valor de System.ItemNamePrefix excluye los espacios finales, la concatenación debe incluir un espacio al generar [System.ItemNameDisplay](). Tenga en cuenta que no se garantiza que esta propiedad sea única, pero está diseñada para promover el candidato más probable que puede ser único y también tiene sentido para los usuarios finales.

Por ejemplo, para los documentos, [System.Title](./props-system-title.md) podría usarse como [System.ItemNameDisplay](), pero en la práctica el título de los documentos puede no ser útil o lo suficientemente único como para funcionar como el único System.ItemNameDisplay. En su lugar, [proporcionar System.FileName](./props-system-filename.md) como valor de System.ItemNameDisplay es una mejor opción. En Windows, el correo electrónico se almacena en el sistema de archivos como archivos .eml. Los valores System.FileName de esos archivos no son fáciles de usar, ya que son GUID. En este ejemplo, la promoción de [System.Subject](./props-system-subject.md) como System.ItemNameDisplay tiene más sentido.

**Notas de compatibilidad:**

-   Implementaciones de carpetas de shell en Windows Vista: use PKEY ItemNameDisplay para la columna name cuando desee que Windows Explorer llame \_ a [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN NORMAL) para obtener el valor del \_ nombre. Use otro PKEY, como PKEY ItemName, cuando desee que Windows Explorer llame al almacén de propiedades de la carpeta o a \_ [**IShellFolder2::GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) para obtener el valor del nombre.
-   Implementaciones de carpetas de shell en Windows XP: la primera columna debe ser la columna name y Windows Explorer llama a [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para obtener el valor del nombre. PKEY/SCID no importa.



| Tipo de elemento     | Ejemplo                   |
|---------------|---------------------------|
| Archivo          | hello.txt                 |
| Message       | Re: ¿Dónde está la reunión? |
| Carpeta del dispositivo | song.wma                  |
| Carpeta        | Documentos                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

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

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
