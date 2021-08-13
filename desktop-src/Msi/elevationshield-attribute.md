---
description: Este atributo agrega el icono de elevación Control de cuentas de usuario (UAC) (icono de escudo) al control PushButton.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Atributo ElevationShield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4c5da7133a7216386be56328c0e21e2e365129caa185e045984cb5e89b7d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637495"
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
| 8388608 | 0x00800000  | **msidbControlAttributesExiaShield** |



 

 

 



