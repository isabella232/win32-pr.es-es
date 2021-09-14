---
description: Este atributo es la cadena de texto que se muestra en el control .
ms.assetid: 0c4b7183-a43a-4c91-b01e-9f377500ba38
title: Atributo de control de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3f4eb83f6f796180d3125025afedbc08d956d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169709"
---
# <a name="text-control-attribute"></a>Atributo de control de texto

Este atributo es la cadena de texto que se muestra en el control . En la configuración, si el campo 0 del registro no es NULL, el formato del registro se establece mediante FormatText. Si el campo 0 es NULL, el primer campo del registro define el texto. Al obtener el valor siempre se devuelve en el primer campo. Para algunos controles, es posible que este texto no esté visible. En Windows la tecla de aceleración de un control se define colocando un "&" delante del carácter deseado en esta cadena.

## <a name="valid-controls"></a>Controles válidos

Todos los controles excepto el [control Line](line-control.md).

## <a name="associated-bit-flags"></a>Marcas de bits asociadas

Ninguno.

## <a name="remarks"></a>Observaciones

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



