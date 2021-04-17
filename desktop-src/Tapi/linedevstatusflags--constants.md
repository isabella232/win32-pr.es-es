---
description: Las \_ constantes de marcador de bits LINEDEVSTATUSFLAGS describen una colección de elementos de estado de dispositivo de línea booleanos.
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: Constantes de LINEDEVSTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70745b1a84119af2305cadabd0a39ab5954e5b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679020"
---
# <a name="linedevstatusflags_-constants"></a>Constantes de LINEDEVSTATUSFLAGS \_

Las constantes de marcador de bits **LINEDEVSTATUSFLAGS \_** describen una colección de elementos de estado de dispositivo de línea booleanos.

<dl> <dt>

<span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS \_ conectado**
</dt> <dd> <dl> <dt>



Especifica si la línea está conectada a TAPI. Si es **true**, la línea está conectada y TAPI puede operar en el dispositivo de línea. Si es **false**, la línea está desconectada y la aplicación no puede controlar el dispositivo de línea a través de TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**SERVICIO de LINEDEVSTATUSFLAGS \_**
</dt> <dd> <dl> <dt>



Indica si la línea está en el servicio. Si es **true**, la línea está en servicio; Si es **false**, la línea está fuera de servicio.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS \_ bloqueado**
</dt> <dd> <dl> <dt>



Indica si la línea está bloqueada o desbloqueada. Este bit se usa con más frecuencia con dispositivos de línea asociados a teléfonos móviles. Muchos teléfonos móviles tienen un mecanismo de seguridad que requiere la entrada de una contraseña para permitir que el teléfono realice llamadas. Este bit se puede usar para indicar a las aplicaciones que el teléfono está bloqueado y no puede realizar llamadas hasta que la contraseña se escriba en la interfaz de usuario del teléfono para que la aplicación pueda presentar una alerta adecuada al usuario.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS \_ MSGWAIT**
</dt> <dd> <dl> <dt>



Indica si la línea tiene un mensaje en espera. Si es **true**, un mensaje está esperando; Si es **false**, no hay ningún mensaje en espera.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

\_Las constantes LINEDEVSTATUSFLAGS se usan en el miembro **dwDevStatusFlags** de la estructura de datos [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




