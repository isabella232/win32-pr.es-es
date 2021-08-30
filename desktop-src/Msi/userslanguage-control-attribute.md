---
description: Si se establece esta marca de bits, las fuentes se crean mediante la página de códigos predeterminada de la interfaz de usuario del usuario. Si no se establece la marca de bits, las fuentes se crean mediante la página de códigos de la base de datos.
ms.assetid: 6a3dbabe-6a14-4401-b46c-e8a0bd0cbe63
title: Atributo de control UsersLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120e39dfc9ba80c8d58910a3fbfcf144b4e8dec764abb12dc9df7933ba402914
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809125"
---
# <a name="userslanguage-control-attribute"></a>Atributo de control UsersLanguage

Si se establece esta marca de bits, las fuentes se crean mediante la página de códigos predeterminada de la interfaz de usuario del usuario. Si no se establece la marca de bits, las fuentes se crean mediante la página de códigos de la base de datos.

## <a name="valid-controls"></a>Controles válidos

[Texto](text-control.md)

 

[ListBox](listbox-control.md)

 

[ComboBox](combobox-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                                |
|---------|-------------|-----------------------------------------|
| 1 048 576 | 0x00100000  | **msidbControlAttributesUsersLanguage** |



 

## <a name="remarks"></a>Comentarios

Este atributo de control se puede usar para mostrar el texto que el usuario ha escrito en un [control Edit](edit-control.md) [o PathEdit.](pathedit-control.md)

El control Editar, el control PathEdit, el [control DirectoryList](directorylist-control.md) y el [control DirectoryCombo](directorycombo-control.md) siempre usan las fuentes creadas en la página de códigos de la interfaz de usuario predeterminada del usuario. Esto puede causar problemas si se han instalado idiomas adicionales en el sistema operativo. En este caso, es posible que las fuentes del equipo no puedan representar todos los caracteres en los idiomas agregados. Para determinar qué fuentes se pueden usar, busque los valores en **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ FontLink \\ SystemLink**.

Para obtener más información, vea [Controlar atributos](control-attributes.md) y [controles](controls.md).

 

 



