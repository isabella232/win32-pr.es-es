---
title: D1104 Posible pérdida
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: Se lanzó el generador, pero la interfaz creada a partir de ella sigue estando activo. Aunque es válido liberar recursos después de liberar la fábrica, esta condición podría indicar una pérdida de memoria.
keywords:
- D1104 Possible Leak Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b3c8b49256b3e7009985e9acf6d2b581e2fe436e50325c26f1f7de59cb3b0b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075569"
---
# <a name="d1104-possible-leak"></a>D1104: posible pérdida

Se lanzó \[ *el generador* \] de fábrica, pero la interfaz \[ *creada* a partir de ella \] sigue estando activo. Aunque es válido liberar recursos después de liberar la fábrica, esta condición podría indicar una pérdida de memoria.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="factory"></span><span id="FACTORY"></span>*Fábrica*
</dt> <dd>

Dirección del generador que se publicó.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interfaz*
</dt> <dd>

Dirección de la interfaz que se creó en el *generador*.

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Nivel de error | Information |



 

## <a name="possible-causes"></a>Causas posibles

Se lanzó el generador, pero la interfaz creada a partir de ella sigue estando activo.

 

 




