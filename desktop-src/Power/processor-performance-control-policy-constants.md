---
description: Las constantes de la Directiva de control de rendimiento de procesador indican el algoritmo de control de rendimiento de procesador aplicado a un plan de energía.
ms.assetid: 928ba485-f767-47df-8b57-7630c68068a7
title: Constantes de directiva de control de rendimiento de procesador (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9597750f37d9efda80d4bb2bfff7bc121982e7d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545502"
---
# <a name="processor-performance-control-policy-constants"></a>Constantes de directiva de control de rendimiento de procesador

Las constantes de la Directiva de control de rendimiento de procesador indican el algoritmo de control de rendimiento de procesador aplicado a un plan de energía.



| Constante o valor                                                                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PO_THROTTLE_ADAPTIVE"></span><span id="po_throttle_adaptive"></span><dl> <dt>**Pedido de compra \_ LIMITAR \_ Adaptive**</dt> <dt>3</dt> </dl> | Intenta hacer coincidir el rendimiento del procesador con la demanda actual. Esta directiva usará los Estados alto y bajo de voltaje y frecuencia. Esta directiva reducirá el rendimiento del procesador al voltaje más bajo disponible siempre que no haya demanda suficiente para justificar una mayor tensión. Esta directiva interactuará sobre la limitación del reloj del procesador si no se utiliza el estado C3 y en respuesta a los eventos térmicos.<br/> |
| <span id="PO_THROTTLE_CONSTANT"></span><span id="po_throttle_constant"></span><dl> <dt>**Pedido de compra \_ LIMITAR \_ constante**</dt> <dt>1</dt> </dl> | No permite que el procesador utilice ningún estado de rendimiento de voltaje alto. Esta Directiva no interpondrá la limitación del reloj del procesador, excepto en respuesta a los eventos térmicos.<br/>                                                                                                                                                                                                                                                                 |
| <span id="PO_THROTTLE_DEGRADE"></span><span id="po_throttle_degrade"></span><dl> <dt>**Pedido de compra \_ \_Disminución del límite**</dt> <dt>2</dt> </dl>    | No permite que el procesador utilice ningún estado de rendimiento de voltaje alto. Esta directiva interactuará sobre la limitación del reloj del procesador cuando la batería esté por debajo de un umbral determinado, si no se está usando el estado C3 o en respuesta a los eventos térmicos.<br/>                                                                                                                                                                                    |
| <span id="PO_THROTTLE_NONE"></span><span id="po_throttle_none"></span><dl> <dt>**Pedido de compra \_ LIMITAR \_ ninguno**</dt> <dt>0</dt> </dl>             | No se aplica ningún control de rendimiento de procesador. Esta Directiva siempre ejecuta el procesador con el nivel de rendimiento más alto posible. Esta Directiva no interpondrá la limitación del reloj del procesador, excepto en respuesta a los eventos térmicos.<br/>                                                                                                                                                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Winnt. h (incluye Windows. h)</dt> </dl> |



 

 




