---
description: Las constantes LINEOPENOPTION \_ enumera las opciones disponibles para abrir una línea.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: LINEOPENOPTION_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dc6a4780b366b2dce08110ecce40c7140ab1d0956d788dce5a67d5d0501b6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739255"
---
# <a name="lineopenoption_-constants"></a>LINEOPENOPTION \_ (Constantes)

Las **constantes LINEOPENOPTION \_ enumera** las opciones disponibles para abrir una línea.

<dl> <dt>

<span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**LINEOPENOPTION \_ PROXY**
</dt> <dd> <dl> <dt>



La aplicación está dispuesto a controlar las solicitudes de otras aplicaciones que tienen abierta la línea.


</dt> </dl> </dd> <dt>

<span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION \_ SINGLEADDRESS**
</dt> <dd> <dl> <dt>



Solo se debe informar a la aplicación de las nuevas llamadas creadas en el dispositivo de línea si esas llamadas aparecen en la dirección especificada en el **miembro dwAddressID** en la estructura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) a la que apunta el parámetro *lpCallParams.*


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Consulte [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) para obtener más detalles sobre el funcionamiento de estas opciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




