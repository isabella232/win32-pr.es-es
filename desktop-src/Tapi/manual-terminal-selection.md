---
description: Si las reglas de la selección predeterminada no satisfacen las necesidades de la aplicación, la aplicación tiene la opción de seleccionar el terminal manualmente.
ms.assetid: 12d7781e-a27d-4cbe-b7c4-6c0dfef11074
title: Selección de terminal manual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95335402690c57cc3f564f5d238ca031df4b3549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812487"
---
# <a name="manual-terminal-selection"></a>Selección de terminal manual

Si las reglas de la selección predeterminada no satisfacen las necesidades de la aplicación, la aplicación tiene la opción de seleccionar el terminal como siempre, es decir, puede usar [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) para enumerar las secuencias presentes en la llamada y seleccionar el terminal en las secuencias correspondientes (o, en el caso de los terminales Multipista, crear pistas para las secuencias y seleccionar pistas creadas en las secuencias).

 

 
