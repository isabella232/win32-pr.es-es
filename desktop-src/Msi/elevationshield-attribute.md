---
description: Este atributo agrega el icono de elevación Control de cuentas de usuario (UAC) (icono de escudo) al control PushButton.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Atributo ElevationShield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c580beefd1d2c0a80b0ee63b7a44e58a2a2fae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158501"
---
# <a name="elevationshield-attribute"></a>Atributo ElevationShield

Este atributo agrega el [*icono de elevación control*](u-gly.md) de cuentas de usuario (UAC) (icono de escudo) al control [PushButton](pushbutton-control.md).

Si se establece este bit y la [](e-gly.md) instalación aún no se está ejecutando con privilegios elevados, el control de botón de inserción se crea mediante el icono de elevación control de cuentas de usuario [](u-gly.md) (UAC) (icono de escudo).

Si se establece este bit y la [](e-gly.md) instalación ya se está ejecutando con privilegios elevados, el control de botón de inserción se crea con los otros atributos de icono.

Si no se establece este bit, el control de botón de inserción se crea con los otros atributos de icono.

## <a name="valid-controls"></a>Controles válidos

[Pulsador](pushbutton-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                                  |
|---------|-------------|-------------------------------------------|
| 8388608 | 0x00800000  | **msidbControlAttributesEentaciónShield** |



 

 

 



