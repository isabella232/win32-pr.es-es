---
description: ICE86 emite una advertencia si el paquete usa la propiedad AdminUser en la columna de base de datos del tipo Condición. Los autores de paquetes deben usar la propiedad Privileged en instrucciones condicionales.
ms.assetid: c23c2920-3b8b-4cd1-a570-bdeabcf11436
title: ICE86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c96e572a99fc31fea540fa4fbaad4179d1e8f2ecadebfcd9222527ca6a4afac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894995"
---
# <a name="ice86"></a>ICE86

ICE86 emite una advertencia si el paquete usa la [**propiedad AdminUser**](adminuser.md) en la columna de base de datos del [tipo Condición.](condition.md) Los autores de paquetes deben usar [**la propiedad Privileged**](privileged.md) en instrucciones condicionales.

## <a name="result"></a>Resultado

ICE86 publica la advertencia siguiente.



| Advertencia de ICE86                                                                                               | Descripción                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| Propiedad \` %s \` encontrada en la \` columna %s \` . \` %s \` en la fila %s. \`La \` propiedad con privilegios suele ser más adecuada. | [**La propiedad AdminUser**](adminuser.md) se usó en un campo Condición. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



