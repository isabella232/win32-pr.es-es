---
description: ICE86 emite una advertencia si el paquete usa la propiedad AdminUser en la columna Database del tipo condition. Los autores de paquetes deben usar la propiedad privileged en las instrucciones condicionales.
ms.assetid: c23c2920-3b8b-4cd1-a570-bdeabcf11436
title: ICE86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25df1e2a9c3ab610e78efd6f797cb916f0563e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361153"
---
# <a name="ice86"></a>ICE86

ICE86 emite una advertencia si el paquete usa la propiedad [**AdminUser**](adminuser.md) en la columna Database del tipo [Condition](condition.md) . Los autores de paquetes deben usar la propiedad [**privileged**](privileged.md) en las instrucciones condicionales.

## <a name="result"></a>Resultado

ICE86 envía la siguiente advertencia.



| ADVERTENCIA de ICE86                                                                                               | Descripción                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| \`Se encontró la propiedad% s \` en la columna \` % s \` . \` % s \` en la fila% s. \`La \` propiedad privilegiada suele ser más adecuada. | La propiedad [**AdminUser**](adminuser.md) se usó en un campo condition. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



