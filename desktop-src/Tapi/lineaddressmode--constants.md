---
description: Las constantes de marca de bits LINEADDRESSMODE \_ describen varias maneras de identificar una dirección en un dispositivo de línea.
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: LINEADDRESSMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4863b79c4527395f6ecb2d28c4d9ef718ff5a7fd99681185ba892bac2b4639ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761867"
---
# <a name="lineaddressmode_-constants"></a>Constantes \_ LINEADDRESSMODE

Las constantes de marca de bits **LINEADDRESSMODE \_** describen varias maneras de identificar una dirección en un dispositivo de línea.

<dl> <dt>

<span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE \_ ADDRESSID**
</dt> <dd> <dl> <dt>



La dirección se especifica con un pequeño entero en el intervalo de 0 a *dwNumAddresses* menos uno, donde *dwNumAddresses* es el valor de las funcionalidades del dispositivo de la línea.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE \_ DIALABLEADDR**
</dt> <dd> <dl> <dt>



La dirección se especifica a través de su número de teléfono.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

Esta constante se usa para seleccionar una dirección en una línea en la que se va a originar una llamada. El modelo habitual seleccionaría la dirección por medio de su identificador de dirección. Los identificadores de dirección son el mecanismo que se usa para identificar direcciones en TAPI. Sin embargo, en algunos entornos, al realizar una llamada, suele ser más práctico identificar la dirección de origen de una llamada por número de teléfono en lugar de por identificador de dirección. Un ejemplo es el posible modelado de un gran número de estaciones (de terceros) en el conmutador mediante un dispositivo de línea con muchas direcciones. La línea representa el conjunto de todas las estaciones y cada estación se asigna a una dirección con su propio número de teléfono principal y su identificador de dirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




