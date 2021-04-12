---
title: D1104 posible fuga
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: El generador se liberó pero la interfaz creada a partir de ella todavía está activa. Aunque es válido liberar recursos después de liberar el generador, esta condición podría indicar una fuga de memoria.
keywords:
- D1104 posible fuga Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 71ccbee152d60a73fbea5ebac2a1074534b69c3a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104357992"
---
# <a name="d1104-possible-leak"></a>D1104: posible fuga

\[  \] Se liberó el generador de fábrica pero la \[ *interfaz* \] de interfaz creada a partir de ella todavía está activa. Aunque es válido liberar recursos después de liberar el generador, esta condición podría indicar una fuga de memoria.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="factory"></span><span id="FACTORY"></span>*Factory*
</dt> <dd>

Dirección del generador que se liberó.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interfaz*
</dt> <dd>

Dirección de la interfaz que se creó en el *generador*.

</dd> </dl> 

|             |             |
|-------------|-------------|
| Nivel de error | Información |



 

## <a name="possible-causes"></a>Causas posibles

El generador se liberó pero la interfaz creada a partir de ella todavía está activa.

 

 




