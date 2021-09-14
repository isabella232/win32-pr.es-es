---
description: Las constantes de marca de bits LINEGENERATETERM describen las condiciones en las que se termina la generación \_ de dígitos o tono.
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: LINEGENERATETERM_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6804b09879471a77780a95ca4ed35b7aaa5b6e1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068743"
---
# <a name="linegenerateterm_-constants"></a>LINEGENERATETERM \_ (Constantes)

Las constantes de marca de bits **LINEGENERATETERM \_** describen las condiciones en las que se termina la generación de dígitos o tono.

<dl> <dt>

<span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM \_ CANCEL**
</dt> <dd> <dl> <dt>



La solicitud de generación de dígitos o tono fue cancelada por esta aplicación, por otra aplicación o porque la llamada finalizó. Este valor también se puede devolver cuando no se puede completar la generación de dígitos o tono debido a un error interno del proveedor de servicios.


</dt> </dl> </dd> <dt>

<span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM \_ LISTO**
</dt> <dd> <dl> <dt>



El número solicitado de dígitos o los tonos solicitados se han generado durante la duración solicitada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




