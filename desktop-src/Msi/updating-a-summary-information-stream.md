---
description: El valor de la propiedad Resumen del número de revisión en el flujo de información de resumen se debe cambiar a un nuevo valor único al localizar una base de datos, porque la base de datos de instalación se está cambiando. Vea códigos de paquete.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Actualizar una secuencia de información de Resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c022023f79d8f4d3999db6e11e4cf65b73e1ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424040"
---
# <a name="updating-a-summary-information-stream"></a>Actualizar una secuencia de información de Resumen

El valor de la propiedad [**Resumen del número de revisión**](revision-number-summary.md) en el flujo de información de [Resumen](summary-information-stream.md) se debe cambiar a un nuevo valor único al localizar una base de datos, porque la base de datos de instalación se está cambiando. Vea [códigos de paquete](package-codes.md).

El valor de la propiedad de [**Resumen de plantilla**](template-summary.md) en la secuencia de información de resumen se debe cambiar al identificador de idioma numérico (LANGID) del nuevo lenguaje.

Si las cadenas de texto descriptivos de la secuencia de información de resumen se localizan en el nuevo idioma, la propiedad de Resumen de página de [**códigos**](codepage-summary.md) debe establecerse en la página de códigos correcta para el nuevo lenguaje.

Puede modificar la secuencia de información de resumen del paquete localizado siguiendo el mismo procedimiento que en [Agregar información de Resumen](adding-summary-information.md). También se proporciona un ejemplo en el que se muestra el uso de los métodos de información de Resumen de la base de datos en el SDK de Windows Installer como la utilidad WiSumInf.vbs. Para obtener más información acerca de WiSumInf.vbs, vea [administrar información de Resumen](manage-summary-information.md).

[Continuar](adding-localized-resources.md)

 

 



