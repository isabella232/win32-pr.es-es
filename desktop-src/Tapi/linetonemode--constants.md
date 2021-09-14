---
description: Las constantes LINETONEMODE \_ describen las distintas selecciones que se usan al generar los tonos de línea.
ms.assetid: 7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263
title: LINETONEMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e1b5a8d49c927dfa3d5ec87f9a4830a91d79d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374786"
---
# <a name="linetonemode_-constants"></a>Constantes \_ LINETONEMODE

Las **constantes LINETONEMODE \_** describen las distintas selecciones que se usan al generar los tonos de línea.

<dl> <dt>

<span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**LINETONEMODE \_ BEEP**
</dt> <dd> <dl> <dt>



El tono es un pitido, como el que se usa para anunciar el principio de una grabación. La definición exacta está definida por el proveedor de servicios.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**FACTURACIÓN DE \_ LINETONEMODE**
</dt> <dd> <dl> <dt>



El tono es un tono de información de facturación, como un tono de aviso de tarjeta de crédito. La definición exacta está definida por el proveedor de servicios.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE \_ BUSY**
</dt> <dd> <dl> <dt>



El tono es un tono ocupado. La definición exacta está definida por el proveedor de servicios.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE \_ CUSTOM**
</dt> <dd> <dl> <dt>



El tono es un tono personalizado definido por sus frecuencias de componente, de tipo [**LINEGENERATETONE.**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone)


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**LINETONEMODE \_ RINGBACK**
</dt> <dd> <dl> <dt>



El tono es el tono de anillo. La definición exacta está definida por el proveedor de servicios.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los 16 bits de orden alto se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

Estas constantes se usan para definir los tonos que se van a generar en la banda a través de una llamada a la parte remota. Tenga en cuenta que la detección de tono de los tonos no personalizados no usa estas constantes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




