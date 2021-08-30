---
description: Las constantes de directiva de control de rendimiento del procesador indican el algoritmo de control de rendimiento del procesador aplicado a un esquema de energía.
ms.assetid: 928ba485-f767-47df-8b57-7630c68068a7
title: Constantes de directiva de control de rendimiento del procesador (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d80b2a91e90047619e582c2e82f1c84d3003df960998bcc037677a8d6200b408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886945"
---
# <a name="processor-performance-control-policy-constants"></a>Constantes de directiva de control de rendimiento del procesador

Las constantes de directiva de control de rendimiento del procesador indican el algoritmo de control de rendimiento del procesador aplicado a un esquema de energía.



| Constante o valor                                                                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PO_THROTTLE_ADAPTIVE"></span><span id="po_throttle_adaptive"></span><dl> <dt>**Pedido de compra \_ LIMITACIÓN \_ ADAPTABLE**</dt> <dt>3</dt> </dl> | Intenta hacer coincidir el rendimiento del procesador con la demanda actual. Esta directiva usará los estados de alta y baja tensión y frecuencia. Esta directiva disminuirá el rendimiento del procesador al voltaje más bajo disponible siempre que no haya una demanda insuficiente para justificar un voltaje mayor. Esta directiva activará la limitación del reloj del procesador si no se utiliza el estado C3 y en respuesta a eventos térmicos.<br/> |
| <span id="PO_THROTTLE_CONSTANT"></span><span id="po_throttle_constant"></span><dl> <dt>**Pedido de compra \_ THROTTLE \_ CONSTANT**</dt> <dt>1</dt> </dl> | No permite que el procesador use estados de rendimiento de alto voltaje. Esta directiva no implicará la limitación del reloj del procesador, excepto en respuesta a eventos térmicos.<br/>                                                                                                                                                                                                                                                                 |
| <span id="PO_THROTTLE_DEGRADE"></span><span id="po_throttle_degrade"></span><dl> <dt>**Pedido de compra \_ DEGRADACIÓN \_ DE LIMITACIÓN**</dt> <dt>2</dt> </dl>    | No permite que el procesador use estados de rendimiento de alto voltaje. Esta directiva implicará la limitación del reloj del procesador cuando la batería esté por debajo de un umbral determinado, si no se está utilizando el estado C3 o en respuesta a eventos térmicos.<br/>                                                                                                                                                                                    |
| <span id="PO_THROTTLE_NONE"></span><span id="po_throttle_none"></span><dl> <dt>**Pedido de compra \_ LIMITE \_ NINGUNO**</dt> <dt>0</dt> </dl>             | No se aplica ningún control de rendimiento del procesador. Esta directiva siempre ejecuta el procesador en el nivel de rendimiento más alto posible. Esta directiva no implicará la limitación del reloj del procesador, excepto en respuesta a eventos térmicos.<br/>                                                                                                                                                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>WinNT.h (incluir Windows.h)</dt> </dl> |



 

 




