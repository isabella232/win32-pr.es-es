---
description: Las \_ constantes LINEOPENOPTION muestran las opciones disponibles para abrir una línea.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: Constantes de LINEOPENOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee9182ff7a28627eebd695ce5d9c0877460b15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680847"
---
# <a name="lineopenoption_-constants"></a>Constantes de LINEOPENOPTION \_

Las **\_ constantes LINEOPENOPTION** muestran las opciones disponibles para abrir una línea.

<dl> <dt>

<span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**\_proxy LINEOPENOPTION**
</dt> <dd> <dl> <dt>



La aplicación está dispuesta a controlar las solicitudes de otras aplicaciones que tienen la línea abierta.


</dt> </dl> </dd> <dt>

<span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION \_ SINGLEADDRESS**
</dt> <dd> <dl> <dt>



Se debe informar a la aplicación de las nuevas llamadas creadas en el dispositivo de línea solo si dichas llamadas aparecen en la dirección especificada en el miembro **dwAddressID** de la estructura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) señalada por el parámetro *lpCallParams* .


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Vea [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) para obtener más detalles sobre el funcionamiento de estas opciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




