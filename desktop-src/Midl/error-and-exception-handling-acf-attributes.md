---
title: Atributos ACF de control de errores y excepciones
description: Use los atributos siguientes para el control de errores.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- MIDL de ACF, atributos, control de errores y excepciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f780145854a463da9a983c7dccbb24b01c2eca16437bf1254f93ec34def5395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384431"
---
# <a name="error-and-exception-handling-acf-attributes"></a>Atributos ACF de control de errores y excepciones

Use los atributos siguientes para el control de errores.



| Atributo                                                                | Uso                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**estado de \_ error de**](comm-status.md)[**\_ comm**](fault-status.md) | Permita que la aplicación cliente controle las excepciones correctamente al provocar errores de comunicación y de servidor que se devuelvan al cliente como valores de parámetro. A continuación, la aplicación cliente puede llamar a la función en tiempo de ejecución RPC [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) para retransmitir un mensaje de error al usuario. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Importar archivos y bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> </dl>

 

 