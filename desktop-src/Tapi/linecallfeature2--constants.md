---
description: En las \_ constantes LINECALLFEATURE2 se enumeran las características complementarias disponibles para las conferencias, la transferencia y las llamadas de estacionamiento.
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: Constantes de LINECALLFEATURE2_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977e71f722fba34da6b2ecbd6a3e914c34a0aae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690370"
---
# <a name="linecallfeature2_-constants"></a>Constantes de LINECALLFEATURE2 \_

En las constantes **LINECALLFEATURE2 \_** se enumeran las características complementarias disponibles para las conferencias, la transferencia y las llamadas de estacionamiento.

<dl> <dt>

<span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2 \_ COMPLCALLBACK**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede invocar la característica de "devolución de llamada" mediante la \_ opción de devolución de llamada LINECOMPLMODE con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). El \_ bit LINECALLFEATURE COMPLETECALL también estará activado en el miembro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2 \_ COMPLCAMPON**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede invocar la característica "Camp on" mediante la opción LINECOMPLMODE \_ campoN con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). El \_ bit LINECALLFEATURE COMPLETECALL también estará activado en el miembro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2 \_ COMPLINTRUDE**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede invocar la característica "intrusión" mediante la opción de \_ intrusión LINECOMPLMODE con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). El \_ bit LINECALLFEATURE COMPLETECALL también estará activado en el miembro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2 \_ COMPLMESSAGE**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede invocar la característica "dejar mensaje" mediante la opción de \_ mensaje LINECOMPLMODE con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). El \_ bit LINECALLFEATURE COMPLETECALL también estará activado en el miembro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2 \_ NOHOLDCONFERENCE**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede crear una "Conferencia sin celebrar" mediante la \_ opción NOHOLDCONFERENCE de LINECALLPARAMFLAGS con [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference). El \_ bit LINECALLFEATURE SETUPCONF también estará activado en el miembro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2 \_ ONESTEPTRANSFER**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede crear una transferencia de un solo paso mediante la \_ opción ONESTEPTRANSFER de LINECALLPARAMFLAGS con [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer). El \_ bit LINECALLFEATURE SETUPTRANSFER también estará activado en el miembro **dwCallFeatures** .

> [!Note]  
> Si no se especifica ninguno de los bits "COMPl" en el miembro **dwCallFeatures2** de [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , pero se \_ especifica LINECALLFEATURE COMPLETECALL, es posible que cualquiera de ellos funcione, pero el proveedor de servicios no ha especificado cuál.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2 \_ TRANSFERCONF**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede usar la función [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) para resolver la transferencia como una conferencia de tres vías. El \_ bit LINECALLFEATURE COMPLETETRANSF también estará activado en el miembro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2 \_ TRANSFERNORM**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede usar la función [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) para resolver la transferencia como una transferencia normal. El \_ bit LINECALLFEATURE COMPLETETRANSF también estará activado en el miembro **dwCallFeatures** .

> [!Note]  
> Si no se especifica TRANSFERNORM ni TRANSFERCONF en el miembro **dwCallFeatures2** de [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) pero \_ se especifica LINECALLFEATURE COMPLETETRANSF, es posible que funcione, pero el proveedor de servicios no ha especificado cuál.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2 \_ PARKDIRECT**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede invocar la característica "estacionamiento dirigido" mediante la \_ opción dirigida LINEPARKMODE con [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark). El bit de estacionamiento de LINECALLFEATURE \_ también estará activado en el miembro de **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2 \_ PARKNONDIRECT**
</dt> <dd> <dl> <dt>



Si este bit está activado, se puede invocar la característica "estacionamiento no dirigido" mediante la opción LINEPARKMODE no \_ Directed con [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark). El bit de estacionamiento de LINECALLFEATURE \_ también estará activado en el miembro de **dwCallFeatures** .

> [!Note]  
> Si no se especifica PARKDIRECT ni PARKNONDIRECT en el miembro **dwCallFeatures2** de [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) pero \_ se especifica LINECALLFEATURE Park, es posible que funcione, pero el proveedor de servicios no ha especificado cuál.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



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

 

 




