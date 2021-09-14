---
description: Las constantes de marca de bits LINESPECIALINFO describen las señales de información especiales que la red puede usar para notificar varias operaciones de informes y \_ observación de red.
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: LINESPECIALINFO_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78154757515ebd5bfa36778795c26ef9fdc96db1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374799"
---
# <a name="linespecialinfo_-constants"></a>LineSPECIALINFO \_ (Constantes)

Las constantes de marca de bits **LINESPECIALINFO \_** describen las señales de información especiales que la red puede usar para notificar varias operaciones de informes y observación de red. Son secuencias de tono codificadas especiales que se transmiten al principio de los anuncios registrados de aviso de red.

<dl> <dt>

<span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO \_ CUSTIRREG**
</dt> <dd> <dl> <dt>



Este tono de información especial precede a un número vacío, AIS, cambio de número de Centrex y estación que no es de trabajo, código de acceso no marcado o marcado por error, o mensaje de operador de interceptación manual (categoría de irregularidad del cliente). LINESPECIALINFO CUSTIRREG también se notifica cuando se rechaza la información de facturación y cuando la dirección telefónica \_ está bloqueada en el conmutador.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO \_ NOCIRCUIT**
</dt> <dd> <dl> <dt>



Este tono de información especial precede a un anuncio sin circuito o de emergencia (categoría de bloqueo de tronco).


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**LINESPECIALINFO \_ REORDER**
</dt> <dd> <dl> <dt>



Este tono de información especial precede a un anuncio de reordenación (categoría de irregularidad del equipo). LINESPECIALINFO REORDER también se notifica cuando el teléfono se mantiene \_ fuera de servicio demasiado tiempo.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO \_ UNAVAIL**
</dt> <dd> <dl> <dt>



Los detalles sobre el tono de información especial no están disponibles y no se conocerán.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO \_ UNKNOWN**
</dt> <dd> <dl> <dt>



Actualmente se desconocen detalles sobre el tono de información especial, pero puede que se conozcan más adelante.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

Los tonos de información especiales se definen para los mensajes de asesoramiento y no se usan normalmente con fines de facturación o supervisión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




