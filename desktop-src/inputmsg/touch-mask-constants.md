---
title: Máscara táctil
description: Valores que pueden aparecer en el campo touchMask de la POINTER_TOUCH_INFO estructura.
ms.assetid: 23AD50C8-C769-48D6-9F27-DB2755C03D5C
topic_type:
- apiref
api_name:
- TOUCH_MASK_NONE
- TOUCH_MASK_CONTACTAREA
- TOUCH_MASK_ORIENTATION
- TOUCH_MASK_PRESSURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5ac389894d9096b389af127685feb9a2d81756ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569089"
---
# <a name="touch-mask"></a>Máscara táctil

Valores que pueden aparecer en el **campo touchMask** de la [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) estructura.

<dl> <dt>

<span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE** 
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Predeterminada. Ninguno de los campos opcionales es válido.


</dt> </dl> </dd> <dt>

<span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



**rcContact** de la [**estructura POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) es válida.


</dt> </dl> </dd> <dt>

<span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



**la** orientación de [**la POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) estructura es válida.


</dt> </dl> </dd> <dt>

<span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



**la** presión de la [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) estructura es válida.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





