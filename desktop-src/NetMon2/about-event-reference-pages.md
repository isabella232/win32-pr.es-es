---
description: Una página de referencia de eventos (ERP) es un documento HTML que proporciona Monitor de red información acerca de los eventos detectados durante la operación de experto o de supervisión.
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: Páginas de referencia de eventos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e989e3e1d4ab0c41dc78c567c662e8a3090906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910086"
---
# <a name="about-event-reference-pages"></a>Páginas de referencia de eventos, acerca de

Una página de referencia de eventos (ERP) es un documento HTML que proporciona Monitor de red información acerca de los eventos detectados durante la operación de experto o de supervisión.

Puede ver O ERP e en el Visor de eventos de Monitor de red, herramienta de control de supervisión o en cualquier explorador que admita las características HTML de Microsoft Internet Explorer versión 4,01 o posterior. Es decir, puede Agregar controles admitidos o lenguajes con scripts en el ERP.

Sin embargo, O ERP e solo aparece si el experto designa el documento HTML por nombre. Cuando se designa correctamente, el ERP aparece en el panel inferior cuando se selecciona el evento en el Visor de eventos. En la ilustración siguiente se muestra un ERP asociado al monitor de intervalo del Protocolo de Internet (IP).

![un ERP asociado con el monitor de intervalo de IP](images/exview2.png)

## <a name="expert-events"></a>Eventos de expertos

El miembro **EventIdent** de una estructura [**NMEVENTDATA**](nmeventdata.md) identifica los eventos de expertos. Al escribir un experto, se determinan los valores de **EventIdent** , que normalmente se numeran como 1, 2, 3, etc. Por ejemplo, supongamos que un experto genera dos eventos (**EventIdent1** y **EventIdent2**). Si desea que el Visor de eventos muestre los eventos por separado, debe crear dos documentos ERP independientes.

 

 



