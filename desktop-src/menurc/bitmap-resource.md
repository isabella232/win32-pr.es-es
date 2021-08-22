---
title: Recurso BITMAP
description: Define un mapa de bits que una aplicación usa en su pantalla o como elemento en un menú o control.
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- Menús de recursos BITMAP y otros recursos
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff75f235e8aa1787e93f9420b4d7ed27f440cdc09510547295ebced4ec494bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734903"
---
# <a name="bitmap-resource"></a>Recurso BITMAP

Define un mapa de bits que una aplicación usa en su pantalla o como elemento en un menú o control.

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nombre único o un valor entero de 16 bits sin signo que identifica el recurso.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Nombre*
</dt> <dd>

Nombre del archivo que contiene el recurso. El nombre debe ser un nombre de archivo válido; debe ser una ruta de acceso completa si el archivo no está en el directorio de trabajo actual. La ruta de acceso debe ser una cadena entre comillas.

</dd> </dl>

Algunos atributos también se admiten para la compatibilidad con versiones anteriores. Para obtener más información, vea [Atributos de recursos comunes](common-resource-attributes.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se definen dos recursos de mapa de bits:

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de mapas de bits](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 