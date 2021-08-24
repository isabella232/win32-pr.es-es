---
description: El valor de la propiedad Resumen del número de revisión del flujo de información de resumen debe cambiarse a un nuevo valor único al localizar una base de datos, porque se está cambiando la base de datos de instalación. Consulte Códigos de paquete.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Actualizar un flujo de información de resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d95e6a0cf09af5d4a024f707c0694d89def47abf8f731f394c55a11232bc07f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039285"
---
# <a name="updating-a-summary-information-stream"></a>Actualizar un flujo de información de resumen

El valor de la propiedad [**Resumen**](revision-number-summary.md) del número de revisión del flujo de información de resumen debe cambiarse a un nuevo valor único al localizar una base de datos, porque se está cambiando la base de datos de instalación. [](summary-information-stream.md) Vea [Códigos de paquete](package-codes.md).

El valor de la [**propiedad Resumen de**](template-summary.md) plantilla del flujo de información de resumen debe cambiarse al identificador numérico de idioma (LANGID) del nuevo idioma.

Si las cadenas de texto descriptivo del flujo de información de resumen están localizadas en el nuevo idioma, la propiedad [**Resumen**](codepage-summary.md) de página de códigos debe establecerse en la página de códigos correcta para el nuevo idioma.

Puede modificar el flujo de información de resumen del paquete localizado por el mismo procedimiento que en [Agregar información de resumen](adding-summary-information.md). También se proporciona un ejemplo que muestra el uso de los métodos de información de resumen de base de datos en el SDK del instalador de Windows como la utilidad WiSumInf.vbs. Para obtener más información sobre WiSumInf.vbs, vea [Administrar información de resumen](manage-summary-information.md).

[Continuar](adding-localized-resources.md)

 

 



