---
title: Recurso de mapa de bits
description: Define un mapa de bits que utiliza una aplicación en su presentación en pantalla o como un elemento de un menú o control.
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- Menús de recursos de mapa de bits y otros recursos
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5bed33fb66d9deb85e1f25165f3f7a0f664961
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420608"
---
# <a name="bitmap-resource"></a>Recurso de mapa de bits

Define un mapa de bits que utiliza una aplicación en su presentación en pantalla o como un elemento de un menú o control.

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nombre único o un valor entero sin signo de 16 bits que identifica el recurso.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extensión*
</dt> <dd>

Nombre del archivo que contiene el recurso. El nombre debe ser un nombre de archivo válido. debe ser una ruta de acceso completa si el archivo no está en el directorio de trabajo actual. La ruta de acceso debe ser una cadena entre comillas.

</dd> </dl>

Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores. Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se definen dos recursos de mapa de bits:

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar mapas de bits](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 