---
description: La constante de marca de bits LINETRANSLATEOPTION \_ describe una opción utilizada por la traducción de direcciones.
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: LINETRANSLATEOPTION_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e103f2a93d30be5260b27c7bf5c0e97f3ce7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374774"
---
# <a name="linetranslateoption_-constants"></a>LINETRANSLATEOPTION \_ (Constantes)

La constante de marca de bits **LINETRANSLATEOPTION \_** describe una opción utilizada por la traducción de direcciones.

<dl> <dt>

<span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION \_ CANCELCALLWAITING**
</dt> <dd> <dl> <dt>



Si se define una cadena En espera de llamada de cancelación para la ubicación, al establecer este bit se insertará esa cadena al principio de la cadena que se puede marcar. Esto lo usan normalmente las aplicaciones de módem de datos y fax para evitar la interrupción de llamadas mediante pitidos de espera de llamada. Si no se define ninguna cadena de cancelación de llamada en espera para la ubicación, este bit no tiene ningún efecto. Tenga en cuenta que se recomienda que las aplicaciones que usan este bit también establezcan el bit LINECALLPARAMFLAGS SECURE en el \_ **miembro dwCallParamFlags** de la estructura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) que se pasa a [**lineMakeCall a**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) través del parámetro *lpCallParams,* de modo que si el dispositivo de línea usa un mecanismo distinto de los dígitos que se pueden marcar para suprimir las interrupciones de llamada, se invocará ese mecanismo.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION \_ CARDOVERRIDE**
</dt> <dd> <dl> <dt>



La tarjeta de llamada predeterminada se reemplazará por una especificada.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION \_ FORCELD**
</dt> <dd> <dl> <dt>



Esta opción obliga a que la dirección (número) se traduzca como distancia larga.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION \_ FORCELOCAL**
</dt> <dd> <dl> <dt>



Esta opción fuerza que el número (dirección) se traduzca como local.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**LINETRANSLATEOUTPUT**](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




