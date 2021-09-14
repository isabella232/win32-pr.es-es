---
title: Uso de ADO para la recuperación de intervalos
description: Si se usa un lenguaje de automatización, se ActiveX objetos de directorio (ADO) para recuperar un intervalo de valores de propiedad. Cuando se usa ADO para la recuperación de intervalos, hay un problema que se debe solucionar específicamente.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Uso de ADO para ADSI de recuperación de intervalos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb8950a71708bd9c824c90842f043808c897554
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255927"
---
# <a name="using-ado-for-range-retrieval"></a>Uso de ADO para la recuperación de intervalos

Si se usa un lenguaje de automatización, ActiveX Directory Objects (ADO) se debe usar para recuperar un intervalo de valores de propiedad.

Cuando se usa ADO para la recuperación de intervalos, hay un problema que se debe solucionar específicamente. Al consultar el grupo final de valores de propiedad, el objeto ADO recuperará cero objetos, aunque permanezcan más. Para recuperar los valores restantes, use el carácter comodín de intervalo ' \* '. Por ejemplo, si un grupo contiene 150 miembros, los valores de miembro 0-100 se pueden recuperar normalmente mediante la recuperación por intervalos. Si se solicita el intervalo 101-200, el objeto ADO devolverá cero objetos. En este momento, es necesario modificar la consulta para solicitar el intervalo 101- \* . Esto recuperará los valores de 101 a 150. Para obtener más información y un ejemplo de código, vea Ejemplo de código para [usar Ranging para recuperar miembros de un grupo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).

Para obtener más información sobre el uso de ADO para la recuperación de intervalos, consulte:

-   [Dialecto de rango LDAP de ADO](ado-ldap-ranging-dialect.md)
-   [Dialecto SQL ADO](ado-sql-ranging-dialect.md)
-   [Código de ejemplo para usar Ranging para recuperar miembros de un grupo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




