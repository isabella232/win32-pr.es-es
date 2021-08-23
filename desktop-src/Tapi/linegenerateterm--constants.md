---
description: Las constantes de marca de bits LINEGENERATETERM describen las condiciones en las que se termina la generación \_ de dígitos o tono.
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: LINEGENERATETERM_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c34d119f503c677e5c251bb494c5ea991dbd0fccf0bfbdb3affecf4c4ff1914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518975"
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

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




