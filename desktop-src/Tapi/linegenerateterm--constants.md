---
description: Las \_ constantes de marcador de bits LINEGENERATETERM describen las condiciones en las que se termina la generación de dígitos o tono.
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: Constantes de LINEGENERATETERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6804b09879471a77780a95ca4ed35b7aaa5b6e1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691047"
---
# <a name="linegenerateterm_-constants"></a>Constantes de LINEGENERATETERM \_

Las constantes de marcador de bits **LINEGENERATETERM \_** describen las condiciones en las que se termina la generación de dígitos o tono.

<dl> <dt>

<span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**\_Cancelar LINEGENERATETERM**
</dt> <dd> <dl> <dt>



La solicitud de generación de dígitos o tono fue cancelada por esta aplicación, por otra aplicación o porque la llamada finalizó. Este valor también se puede devolver cuando no se puede completar la generación de dígitos o de tono debido a un error interno del proveedor de servicios.


</dt> </dl> </dd> <dt>

<span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM \_ completado**
</dt> <dd> <dl> <dt>



Se han generado el número solicitado de dígitos o los tonos solicitados para la duración solicitada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




