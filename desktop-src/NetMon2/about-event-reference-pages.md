---
description: Una página de referencia de eventos (ERP) es un documento HTML que proporciona información Monitor de red sobre los eventos detectados durante la operación de supervisión o experto.
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: Acerca de las páginas de referencia de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f277e2fc31050c5702c1f3cbb3a9b188515386f0b30522fd511771c0b9f3a69e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744875"
---
# <a name="about-event-reference-pages"></a>Acerca de las páginas de referencia de eventos

Una página de referencia de eventos (ERP) es un documento HTML que proporciona información Monitor de red sobre los eventos detectados durante la operación de supervisión o experto.

Puede ver los ERP en la Visor de eventos de Monitor de red, la herramienta de control de supervisión o en cualquier explorador que admita las características HTML de Microsoft Internet Explorer versión 4.01 o posterior. Es decir, puede agregar controles admitidos o lenguajes con script a erp.

Sin embargo, los ERP solo aparecen si el experto designa el documento HTML por nombre. Cuando se designa correctamente, el ERP aparece en el panel inferior cuando se selecciona el evento Visor de eventos la configuración. En la ilustración siguiente se muestra un ERP asociado al monitor de intervalo de protocolos de Internet (IP).

![un erp asociado al monitor de intervalo ip](images/exview2.png)

## <a name="expert-events"></a>Eventos expertos

El miembro **EventIdent** de una estructura [**NMEVENTDATA**](nmeventdata.md) identifica los eventos expertos. Al escribir un experto, se determinan los valores **de EventIdent,** que normalmente se numeran como 1, 2, 3, y así sucesivamente. Por ejemplo, suponga que un experto genera dos eventos **(EventIdent1** y **EventIdent2).** Si desea que el Visor de eventos muestre los eventos por separado, debe crear dos documentos ERP independientes.

 

 



