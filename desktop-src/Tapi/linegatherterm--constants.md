---
description: Las \_ constantes de marcador de bits LINEGATHERTERM describen las condiciones en las que se termina la recopilación de dígitos almacenados en búfer.
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: Constantes de LINEGATHERTERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968492a584024c7750b417a9fd03b68ac1df42ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681215"
---
# <a name="linegatherterm_-constants"></a>Constantes de LINEGATHERTERM \_

Las constantes de marcador de bits **LINEGATHERTERM \_** describen las condiciones en las que se termina la recopilación de dígitos almacenados en búfer.

<dl> <dt>

<span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM \_ BUFFERFULL**
</dt> <dd> <dl> <dt>



Se ha recopilado el número solicitado de dígitos. El búfer está lleno.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**\_Cancelar LINEGATHERTERM**
</dt> <dd> <dl> <dt>



La solicitud fue cancelada por esta aplicación, por otra aplicación o porque la llamada finalizó.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM \_ FIRSTTIMEOUT**
</dt> <dd> <dl> <dt>



El primer dígito agotó el tiempo de espera. El búfer no contiene dígitos.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM de \_ tiempo de espera**
</dt> <dd> <dl> <dt>



Expiró el tiempo de espera entre dígitos. El búfer contiene al menos un dígito.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM \_ TERMDIGIT**
</dt> <dd> <dl> <dt>



Uno de los dígitos de finalización coincidió con un dígito recibido. El dígito de finalización coincidente es el último dígito del búfer.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




