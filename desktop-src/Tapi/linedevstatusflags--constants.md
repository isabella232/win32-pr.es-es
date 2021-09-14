---
description: Las constantes de marca de bits LINEDEVSTATUSFLAGS describen una colección de elementos de estado de \_ dispositivo de línea booleana.
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: LINEDEVSTATUSFLAGS_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70745b1a84119af2305cadabd0a39ab5954e5b7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160625"
---
# <a name="linedevstatusflags_-constants"></a>Constantes LINEDEVSTATUSFLAGS \_

Las constantes de marca de bits **LINEDEVSTATUSFLAGS \_** describen una colección de elementos de estado de dispositivo de línea booleana.

<dl> <dt>

<span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS \_ CONECTADO**
</dt> <dd> <dl> <dt>



Especifica si la línea está conectada a TAPI. Si **es TRUE,** la línea está conectada y TAPI puede funcionar en el dispositivo de línea. Si **es FALSE,** la línea está desconectada y la aplicación no puede controlar el dispositivo de línea a través de TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS \_ INSERVICE**
</dt> <dd> <dl> <dt>



Indica si la línea está en servicio. Si **es TRUE,** la línea está en servicio; si **es FALSE**, la línea está fuera de servicio.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS \_ BLOQUEADO**
</dt> <dd> <dl> <dt>



Indica si la línea está bloqueada o desbloqueada. Este bit se suele usar con dispositivos de línea asociados a teléfonos móviles. Muchos teléfonos móviles tienen un mecanismo de seguridad que requiere la entrada de una contraseña para permitir que el teléfono haga llamadas. Este bit se puede usar para indicar a las aplicaciones que el teléfono está bloqueado y no puede realizar llamadas hasta que se introduce la contraseña en la interfaz de usuario del teléfono para que la aplicación pueda presentar una alerta adecuada al usuario.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS \_ MSGWAIT**
</dt> <dd> <dl> <dt>



Indica si la línea tiene un mensaje en espera. Si **es TRUE,** hay un mensaje en espera; si **es FALSE,** no hay ningún mensaje en espera.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Los 32 bits están reservados.

Las constantes LINEDEVSTATUSFLAGS \_ se usan dentro del miembro **dwDevStatusFlags** de la [**estructura de datos LINEDEVSTATUS.**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




