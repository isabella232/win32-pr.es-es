---
description: Este atributo agrega el icono de elevación de control de cuentas de usuario (UAC) al control PushButton.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Atributo ElevationShield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c580beefd1d2c0a80b0ee63b7a44e58a2a2fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156636"
---
# <a name="elevationshield-attribute"></a>Atributo ElevationShield

Este atributo agrega el icono de elevación de [*control de cuentas de usuario*](u-gly.md) (UAC) al [control Pushbutton](pushbutton-control.md).

Si se establece este bit y la instalación todavía no se ejecuta con privilegios [*elevados*](e-gly.md) , el control Pushbutton se crea con el icono de elevación de [*control de cuentas de usuario*](u-gly.md) (UAC) (icono de escudo).

Si se establece este bit y la instalación ya se está ejecutando con privilegios [*elevados*](e-gly.md) , el control Pushbutton se crea con los demás atributos de icono.

Si no se establece este bit, el control Pushbutton se crea con los demás atributos de icono.

## <a name="valid-controls"></a>Controles válidos

[Botones](pushbutton-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                                  |
|---------|-------------|-------------------------------------------|
| 8388608 | 0x00800000  | **msidbControlAttributesElevationShield** |



 

 

 



