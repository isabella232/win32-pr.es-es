---
description: Las \_ constantes de marcador de bits LINECALLCOMPLMODE describen diferentes maneras en las que se puede completar una llamada.
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: Constantes de LINECALLCOMPLMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373a66b6ce13b7bfba00303bea824f542bf0016a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690306"
---
# <a name="linecallcomplmode_-constants"></a>Constantes de LINECALLCOMPLMODE \_

Las constantes de marcador de bits **LINECALLCOMPLMODE \_** describen diferentes maneras en las que se puede completar una llamada.

<dl> <dt>

<span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**\_devolución de llamada LINECALLCOMPLMODE**
</dt> <dd> <dl> <dt>



Solicita a la estación llamada que devuelva la llamada cuando vuelva a estar inactiva.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE \_ campoN**
</dt> <dd> <dl> <dt>



Pone en cola la llamada hasta que se puede completar la llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE \_ intrusión**
</dt> <dd> <dl> <dt>



Agrega la aplicación a la llamada existente en la estación llamada (Barge en).


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**\_mensaje LINECALLCOMPLMODE**
</dt> <dd> <dl> <dt>



Deja un breve mensaje predefinido para la estación llamada (deje la llamada de Word). El mensaje que se va a enviar se especifica por separado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




