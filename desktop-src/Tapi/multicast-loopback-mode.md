---
description: La \_ enumeración de modo de bucle invertido de multidifusión \_ describe el modo de bucle invertido.
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: Enumeración MULTICAST_LOOPBACK_MODE (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a15505efcd1a9e399866b104da0582ccf846689
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691114"
---
# <a name="multicast_loopback_mode-enumeration"></a>\_Enumeración de modo de bucle invertido \_

\[**Multidifusión \_ El \_ modo de bucle invertido** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La enumeración de **\_ \_ modo de bucle invertido de multidifusión** describe el modo de bucle invertido.

## <a name="syntax"></a>Sintaxis


```C++
} MULTICAST_LOOPBACK_MODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM \_ sin \_ bucle invertido**
</dt> <dd>

Bucle invertido de multidifusión deshabilitado. Esto significa que dos aplicaciones en el mismo equipo que se unen al mismo grupo de multidifusión pueden obtener los paquetes de los demás.

</dd> <dt>

<span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**\_ \_ bucle invertido completo mm**
</dt> <dd>

También se recorren en bucle todos los paquetes enviados. Este modo solo es útil para realizar pruebas.

</dd> <dt>

<span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**\_ \_ bucle invertido de mm selectivo**
</dt> <dd>

El bucle invertido selectivo está habilitado. Esto significa que varias aplicaciones habilitadas en un equipo pueden unirse al mismo grupo de multidifusión sin confusión. Los paquetes se recorren en bucle desde la pila y cada sesión de RTP es responsable de filtrar los paquetes no deseados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMulticastControl:: get \_ LoopbackMode**](imulticastcontrol-get-loopbackmode.md)
</dt> <dt>

[**IMulticastControl::p UT \_ LoopbackMode**](imulticastcontrol-put-loopbackmode.md)
</dt> </dl>

 

 




