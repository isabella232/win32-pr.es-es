---
description: Este atributo es la cadena de texto que se muestra en el control.
ms.assetid: 0c4b7183-a43a-4c91-b01e-9f377500ba38
title: Atributo de control de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3f4eb83f6f796180d3125025afedbc08d956d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276501"
---
# <a name="text-control-attribute"></a>Atributo de control de texto

Este atributo es la cadena de texto que se muestra en el control. Si el valor del campo 0 del registro no es null, se aplica formato al registro mediante FormatText. Si el campo 0 es null, el primer campo del registro define el texto. Al obtener el valor, siempre se devuelve en el primer campo. Para algunos controles, es posible que este texto no esté visible. En Windows, la tecla de aceleración de un control se define colocando una "&" delante del carácter deseado en esta cadena.

## <a name="valid-controls"></a>Controles válidos

Todos los controles excepto el [control de línea](line-control.md).

## <a name="associated-bit-flags"></a>Marcas de bits asociadas

Ninguno.

## <a name="remarks"></a>Observaciones

Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).

 

 



