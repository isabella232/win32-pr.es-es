---
description: Si las reglas de selección predeterminada no satisfacen las necesidades de la aplicación, la aplicación tiene la opción de seleccionar el terminal manualmente.
ms.assetid: 12d7781e-a27d-4cbe-b7c4-6c0dfef11074
title: Selección manual de terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6eaa1e0a5b8b53b1037c51b0e628d7a27ece0be65a0f9a7e86e882c722360f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514645"
---
# <a name="manual-terminal-selection"></a>Selección manual de terminal

Si las reglas de selección predeterminada no satisfacen las necesidades de la aplicación, la aplicación tiene la opción de seleccionar el terminal como siempre lo tiene: es decir, puede usar [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) para enumerar las secuencias presentes en la llamada y seleccionar el terminal en las secuencias adecuadas (o, en el caso de terminales de varios pasos, crear pistas para las secuencias y seleccionar pistas creadas en las secuencias).

 

 
