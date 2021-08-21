---
description: Las constantes LINECALLFEATURE2 enumera las características complementarias disponibles para las \_ llamadas de conferencia, transferencia y aparcamiento.
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: LINECALLFEATURE2_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b1ef95c5427c70455466fdc4e44424a8d7bc92f768698bd3356f28256b4dbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003143"
---
# <a name="linecallfeature2_-constants"></a>LineCALLFEATURE2 \_ Constantes

Las **constantes LINECALLFEATURE2 \_** enumera las características complementarias disponibles para las llamadas de conferencia, transferencia y aparcamiento.

<dl> <dt>

<span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2 \_ COMPLCALLBACK**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede invocar la característica de "devolución de llamada" mediante la opción LINECOMPLMODE \_ CALLBACK [**con lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). El bit LINECALLFEATURE \_ COMPLETECALL también estará en en el **miembro dwCallFeatures.**


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2 \_ COMPLCAMPON**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede invocar la característica "campo en" mediante la opción LINECOMPLMODE \_ CAMPON [**con lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). El bit LINECALLFEATURE \_ COMPLETECALL también estará en en el **miembro dwCallFeatures.**


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2 \_ COMPLINTRUDE**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede invocar la característica "intrude" mediante la opción LINECOMPLMODE \_ INTRUDE [**con lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). El bit LINECALLFEATURE \_ COMPLETECALL también estará en en el **miembro dwCallFeatures.**


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2 \_ COMPLMESSAGE**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede invocar la característica "leave message" mediante la opción LINECOMPLMODE \_ MESSAGE con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). El bit LINECALLFEATURE \_ COMPLETECALL también estará en en el **miembro dwCallFeatures.**


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2 \_ NOHOLDCONFERENCE**
</dt> <dd> <dl> <dt>



Si este bit está en, se puede crear una "conferencia sin espera" mediante la opción LINECALLPARAMFLAGS \_ NOHOLDCONFERENCE [**con lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference). El bit LINECALLFEATURE \_ SETUPCONF también estará en en el **miembro dwCallFeatures.**


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2 \_ ONESTEPTRANSFER**
</dt> <dd> <dl> <dt>



Si este bit está en, se puede crear "transferencia de un paso" mediante la opción LINECALLPARAMFLAGS \_ ONESTEPTRANSFER [**con lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer). El bit LINECALLFEATURE \_ SETUPTRANSFER también estará en en el **miembro dwCallFeatures.**

> [!Note]  
> Si no se especifica ninguno de los bits "COMPL" en el miembro **dwCallFeatures2** en [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) pero se especifica LINECALLFEATURE COMPLETECALL, es posible que cualquiera de ellos funcione, pero el proveedor de servicios no ha especificado \_ cuál.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2 \_ TRANSFERCONF**
</dt> <dd> <dl> <dt>



Si este bit está activado, la [**función lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) se puede usar para resolver la transferencia como una conferencia triple. El bit LINECALLFEATURE \_ COMPLETETRANSF también estará en en el **miembro dwCallFeatures.**


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2 \_ TRANSFERNORM**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede usar [**la función lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) para resolver la transferencia como una transferencia normal. El bit LINECALLFEATURE \_ COMPLETETRANSF también estará en en el **miembro dwCallFeatures.**

> [!Note]  
> Si no se especifica TRANSFERNORM ni TRANSFERCONF en el miembro **dwCallFeatures2** en [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) pero se especifica LINECALLFEATURE COMPLETETRANSF, es posible que cualquiera de ellos funcione, pero el proveedor de servicios no ha especificado \_ cuál.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2 \_ PARKDIRECT**
</dt> <dd> <dl> <dt>



Si este bit está on, la característica "directedpark" se puede invocar mediante la opción LINEPARKMODE \_ DIRECTED con [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark). El bit LINECALLFEATURE \_ PARK también estará en en el miembro **dwCallFeatures.**


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2 \_ PARKNONDIRECT**
</dt> <dd> <dl> <dt>



Si este bit está on, la característica "non-directedpark" se puede invocar mediante la opción LINEPARKMODE \_ NONDIRECTED con [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark). El bit LINECALLFEATURE \_ PARK también estará en en el miembro **dwCallFeatures.**

> [!Note]  
> Si no se especifica NI PARKDIRECT ni PARKNONDIRECT en el miembro **dwCallFeatures2** en [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) pero se especifica LINECALLFEATURE PARK, es posible que cualquiera de ellos funcione, pero el proveedor de servicios no ha especificado \_ cuál.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark)
</dt> <dt>

[**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




