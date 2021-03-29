---
description: Las \_ constantes LINEDIGITMODE describen distintos tipos de generación de dígitos en banda.
ms.assetid: d603ea28-2b93-4548-bb16-78e93087f828
title: Constantes de LINEDIGITMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bedd7f508368a84ab2fa70fac37c316dcc6c85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679019"
---
# <a name="linedigitmode_-constants"></a>Constantes de LINEDIGITMODE \_

Las **constantes \_ LINEDIGITMODE** describen distintos tipos de generación de dígitos en banda.

<dl> <dt>

<span id="LINEDIGITMODE_DTMF"></span><span id="linedigitmode_dtmf"></span>**LINEDIGITMODE \_ DTMF**
</dt> <dd> <dl> <dt>



Utiliza tonos DTMF para indicar dígitos. Los dígitos válidos son de 0 a 9, ' \* ', ' \# ', ' A ', ' B ', ' C ' y ' d '.


</dt> </dl> </dd> <dt>

<span id="LINEDIGITMODE_DTMFEND"></span><span id="linedigitmode_dtmfend"></span>**LINEDIGITMODE \_ DTMFEND**
</dt> <dd> <dl> <dt>



Utiliza tonos DTMF para indicar dígitos y detectar los bordes inactivos. Los dígitos válidos son de 0 a 9, ' \* ', ' \# ', ' A ', ' B ', ' C ' y ' d '.


</dt> </dl> </dd> <dt>

<span id="LINEDIGITMODE_PULSE"></span><span id="linedigitmode_pulse"></span>**\_pulso LINEDIGITMODE**
</dt> <dd> <dl> <dt>



Utiliza secuencias de impulsos giratorio para indicar los dígitos. Los dígitos válidos son de 0 a 9.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Se puede especificar un modo de dígito al generar o detectar dígitos. Tenga en cuenta que los dígitos de pulsos se generan mediante la creación y la interrupción del circuito de bucle local. El conmutador absorbe estos impulsos. El extremo remoto simplemente lo observa como una serie de clics de audio en banda. Por lo tanto, la detección de dígitos enviados como impulsos debe ser capaz de detectar estas secuencias de 1 a 10 clics auditivos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




