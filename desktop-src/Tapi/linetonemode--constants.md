---
description: Las \_ constantes LINETONEMODE describen diferentes selecciones que se usan al generar tonos de línea.
ms.assetid: 7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263
title: Constantes de LINETONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e1b5a8d49c927dfa3d5ec87f9a4830a91d79d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690090"
---
# <a name="linetonemode_-constants"></a>Constantes de LINETONEMODE \_

Las **\_ constantes LINETONEMODE** describen diferentes selecciones que se usan al generar tonos de línea.

<dl> <dt>

<span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**LINETONEMODE \_ beep**
</dt> <dd> <dl> <dt>



El tono es un bip, como el que se usa para anunciar el principio de una grabación. La definición exacta es el proveedor de servicio definido.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**facturación de LINETONEMODE \_**
</dt> <dd> <dl> <dt>



El tono es un tono de información de facturación como un tono de solicitud de tarjeta de crédito. La definición exacta es el proveedor de servicio definido.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE \_ ocupado**
</dt> <dd> <dl> <dt>



El tono es un tono ocupado. La definición exacta es el proveedor de servicio definido.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE \_ personalizado**
</dt> <dd> <dl> <dt>



El tono es un tono personalizado definido por sus frecuencias de componentes, de tipo [**LINEGENERATETONE**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**\_timbre LINETONEMODE**
</dt> <dd> <dl> <dt>



El tono es el tono de la timbre. La definición exacta es el proveedor de servicio definido.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

Estas constantes se utilizan para definir los tonos que se van a generar en banda en una llamada a la parte remota. Tenga en cuenta que la detección de tonos de los tonos no personalizados no utiliza estas constantes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




