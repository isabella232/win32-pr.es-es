---
title: D1104 Posible pérdida
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: Se lanzó el generador, pero la interfaz creada a partir de ella sigue estando activo. Aunque es válido liberar recursos después de liberar el generador, esta condición podría indicar una pérdida de memoria.
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
ms.openlocfilehash: b6629a0da2b89e13feebc33fe5742e3459fc082b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548680"
---
# <a name="d1104-possible-leak"></a>D1104: posible pérdida

Se lanzó \[ *el generador* \] de fábrica, pero la interfaz \[ *creada* a partir de ella \] sigue estando activo. Aunque es válido liberar recursos después de liberar el generador, esta condición podría indicar una pérdida de memoria.

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

 

 




