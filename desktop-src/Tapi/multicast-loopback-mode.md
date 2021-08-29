---
description: La enumeración MULTICAST \_ LOOPBACK \_ MODE describe el modo de bucle recuperación de multidifusión.
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: MULTICAST_LOOPBACK_MODE enumeración (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f322f723d6e1dfa7a0819c661b13d02fdfda753738f7cdb9c304c394bffc2a40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002843"
---
# <a name="multicast_loopback_mode-enumeration"></a>Enumeración MULTICAST \_ LOOPBACK \_ MODE

\[**MULTIDIFUSIÓN \_ LOOPBACK \_ MODE no** está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **enumeración MULTICAST \_ LOOPBACK \_ MODE** describe el modo de bucle recuperación de multidifusión.

## <a name="syntax"></a>Syntax


```C++
} MULTICAST_LOOPBACK_MODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM \_ NO \_ LOOPBACK**
</dt> <dd>

El bucle de multidifusión está deshabilitado. Esto significa que dos aplicaciones de la misma máquina que se unen al mismo grupo de multidifusión pueden obtener paquetes entre sí.

</dd> <dt>

<span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**MM \_ FULL \_ LOOPBACK**
</dt> <dd>

Todos los paquetes enviados también se recorren en bucle. Este modo solo es útil para las pruebas.

</dd> <dt>

<span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**BUCLEBACK \_ \_ SELECTIVO MM**
</dt> <dd>

El bucleback selectivo está habilitado. Esto significa que varias aplicaciones habilitadas en un equipo pueden unirse al mismo grupo de multidifusión sin confusión. Los paquetes se recorren en bucle desde la pila y cada sesión RTP es responsable de filtrar los paquetes no deseados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMulticastControl::get \_ LoopbackMode**](imulticastcontrol-get-loopbackmode.md)
</dt> <dt>

[**IMulticastControl::put \_ LoopbackMode**](imulticastcontrol-put-loopbackmode.md)
</dt> </dl>

 

 




