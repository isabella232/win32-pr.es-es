---
description: Las \_ constantes de marcador de bits PHONEBUTTONMODE describen las clases de botón.
ms.assetid: 7bf337ee-acda-42fe-b50b-370aad50dc03
title: Constantes de PHONEBUTTONMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a4ee5e9835b7df06773bc1429641c91597c15e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681295"
---
# <a name="phonebuttonmode_-constants"></a>Constantes de PHONEBUTTONMODE \_

Las constantes de marcador de bits **PHONEBUTTONMODE \_** describen las clases de botón.

<dl> <dt>

<span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**\_llamada a PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



El botón se asigna a una apariencia de llamada.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**PHONEBUTTONMODE \_ Mostrar**
</dt> <dd> <dl> <dt>



El botón es un botón "soft" asociado a la pantalla del teléfono. Un conjunto de teléfonos puede tener cero o más botones de presentación.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**\_dummy PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



Este valor se usa para describir una posición de botón/lámpara que no tiene un botón correspondiente pero que solo tiene una lámpara.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**\_característica PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



El botón se asigna a las características de solicitud del conmutador, como la retención, la Conferencia y la transferencia.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**\_teclado PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



El botón es uno de los doce botones del teclado, de 0 a 9, ' \* ' y ' \# '.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**PHONEBUTTONMODE \_ local**
</dt> <dd> <dl> <dt>



El botón es un botón de función local, como silenciar o control de volumen.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Este tipo de enumeración se usa en la estructura de datos [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) para describir el significado asociado a los botones del teléfono.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




