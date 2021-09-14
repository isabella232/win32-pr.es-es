---
description: ICE89 valida que el valor de la columna Progid Parent de la tabla ProgId es una clave externa válida en la columna \_ ProgId de la tabla ProgId. Cada elemento primario ProgId debe tener un registro en la tabla ProgId.
ms.assetid: 3f5c1720-d90f-4af7-9162-520b846efbb6
title: ICE89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d14ec5b17a20b9046625feb464865bd0c08419e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074514"
---
# <a name="ice89"></a>ICE89

ICE89 valida que el valor de la columna Progid Parent de la tabla ProgId es una clave externa válida en la columna \_ ProgId de la tabla ProgId. [](progid-table.md) Cada elemento primario ProgId debe tener un registro en la tabla ProgId.

## <a name="result"></a>Resultado

ICE89 publica los siguientes errores.



| Error ice89                                                           | Descripción                                                                |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------|
| El elemento primario ProgId \_ ' \[ 1 \] ' de la tabla ProgId no es un ProgId válido. | Hay un elemento primario ProgId especificado que no aparece en la tabla ProgId. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



