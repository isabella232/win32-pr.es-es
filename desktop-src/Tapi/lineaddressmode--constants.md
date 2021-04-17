---
description: Las \_ constantes de marcador de bits LINEADDRESSMODE describen varias maneras de identificar una dirección en un dispositivo de línea.
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: Constantes de LINEADDRESSMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e926772c82a36865c7f3b95c1ca1321db5682
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690454"
---
# <a name="lineaddressmode_-constants"></a>Constantes de LINEADDRESSMODE \_

Las constantes de marcador de bits **LINEADDRESSMODE \_** describen varias maneras de identificar una dirección en un dispositivo de línea.

<dl> <dt>

<span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE \_ ADDRESSID**
</dt> <dd> <dl> <dt>



La dirección se especifica con un pequeño entero en el intervalo de 0 a *dwNumAddresses* menos uno, donde *dwNumAddresses* es el valor de las capacidades del dispositivo de la línea.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE \_ DIALABLEADDR**
</dt> <dd> <dl> <dt>



La dirección se especifica a través de su número de teléfono.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

Esta constante se utiliza para seleccionar una dirección en una línea en la que se origina una llamada. El modelo habitual seleccionaría la dirección por medio de su identificador de dirección. Los identificadores de dirección son el mecanismo que se usa para identificar direcciones en TAPI. Sin embargo, en algunos entornos, al efectuar una llamada, a menudo es más práctico identificar la dirección de origen de una llamada por el número de teléfono en lugar de por el identificador de dirección. Un ejemplo se encuentra en el posible modelado de un gran número de estaciones (de terceros) en el conmutador por medio de un dispositivo de línea con muchas direcciones. La línea representa el conjunto de todas las estaciones y cada estación se asigna a una dirección con su propio número de teléfono principal e identificador de dirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




