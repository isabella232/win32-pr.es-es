---
description: Las constantes de marca de bits PHONEBUTTONMODE \_ describen las clases de botón.
ms.assetid: 7bf337ee-acda-42fe-b50b-370aad50dc03
title: PHONEBUTTONMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9424c23a9fe6497c657081dd9e197526dc5eb897ad773b1e03fb33c9f08113df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761307"
---
# <a name="phonebuttonmode_-constants"></a>Constantes \_ PHONEBUTTONMODE

Las constantes de marca de bits **PHONEBUTTONMODE \_** describen las clases de botón.

<dl> <dt>

<span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**PHONEBUTTONMODE \_ CALL**
</dt> <dd> <dl> <dt>



El botón se asigna a una apariencia de llamada.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**PANTALLA \_ PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



El botón es un botón "suave" asociado a la pantalla del teléfono. Un conjunto de teléfonos puede tener cero o más botones de presentación.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**PHONEBUTTONMODE \_ DUMMY**
</dt> <dd> <dl> <dt>



Este valor se usa para describir una posición de botón o bombilla que no tiene ningún botón correspondiente, pero que solo tiene una bombilla.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**CARACTERÍSTICA \_ PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



El botón se asigna a la solicitud de características del conmutador, como la retención, la conferencia y la transferencia.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**TECLADO \_ PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



El botón es uno de los doce botones del teclado, de 0 a 9, \* "" y \# "".


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**PHONEBUTTONMODE \_ LOCAL**
</dt> <dd> <dl> <dt>



El botón es un botón de función local, como la exclusión mutua o el control de volumen.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

Este tipo de enumeración se usa en la estructura de datos [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) para describir el significado asociado a los botones del teléfono.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




