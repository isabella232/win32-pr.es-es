---
title: Usar ADO para la recuperación por intervalos
description: Si se utiliza un lenguaje de automatización, los objetos de directorio ActiveX (ADO) deben usarse para recuperar un intervalo de valores de propiedad. Cuando se usa ADO para la recuperación por intervalos, hay un problema que se debe solucionar de forma específica.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Usar ADO para la recuperación de intervalos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb8950a71708bd9c824c90842f043808c897554
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772901"
---
# <a name="using-ado-for-range-retrieval"></a>Usar ADO para la recuperación por intervalos

Si se utiliza un lenguaje de automatización, los objetos de directorio ActiveX (ADO) deben usarse para recuperar un intervalo de valores de propiedad.

Cuando se usa ADO para la recuperación por intervalos, hay un problema que se debe solucionar de forma específica. Al consultar el grupo final de valores de propiedad, el objeto ADO recuperará cero objetos, aunque se mantenga más. Para recuperar los valores restantes, use el carácter comodín de intervalo ' \* '. Por ejemplo, si un grupo contiene 150 miembros, los valores de miembro 0-100 se pueden recuperar normalmente mediante la recuperación por intervalos. Si se solicita el intervalo 101-200, el objeto ADO devolverá cero objetos. En este punto, es necesario modificar la consulta para que el intervalo de solicitud sea 101- \* . Se recuperarán los valores de 101 a 150. Para obtener más información y un ejemplo de código, vea [ejemplo de código para usar el intervalo para recuperar miembros de un grupo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).

Para obtener más información sobre el uso de ADO para la recuperación de intervalos, vea:

-   [Lenguaje de dialecto de ADO LDAP](ado-ldap-ranging-dialect.md)
-   [Dialecto SQL de ADO](ado-sql-ranging-dialect.md)
-   [Código de ejemplo para utilizar el intervalo para recuperar miembros de un grupo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




