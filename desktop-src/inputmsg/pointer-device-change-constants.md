---
title: Cambio de puntero de dispositivo
description: Valores que se pueden pasar en el parámetro wParam del mensaje de WM_POINTERDEVICECHANGE.
ms.assetid: B95191D7-820B-445A-A3A4-811F9F1A8C4F
topic_type:
- apiref
api_name:
- PDC_ARRIVAL
- PDC_REMOVAL
- PDC_ORIENTATION_0
- PDC_ORIENTATION_90
- PDC_ORIENTATION_180
- PDC_ORIENTATION_270
- PDC_MODE_DEFAULT
- PDC_MODE_CENTERED
- PDC_MAPPING_CHANGE
- PDC_RESOLUTION
- PDC_ORIGIN
- PDC_MODE_ASPECTRATIOPRESERVED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5e4b85c17adcd2db7c0f2f672e27ca467b346b0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996762"
---
# <a name="pointer-device-change"></a>Cambio de puntero de dispositivo

Valores que se pueden pasar en el parámetro *wParam* del mensaje de [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) .

<dl> <dt>

<span id="PDC_ARRIVAL"></span><span id="pdc_arrival"></span>**PDC_ARRIVAL**
</dt> <dd> <dl> <dt>

0x001
</dt> <dt>



Se adjunta un nuevo dispositivo.


</dt> </dl> </dd> <dt>

<span id="PDC_REMOVAL"></span><span id="pdc_removal"></span>**PDC_REMOVAL**
</dt> <dd> <dl> <dt>

0x002
</dt> <dt>



Se ha desasociado un dispositivo.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIENTATION_0"></span><span id="pdc_orientation_0"></span>**PDC_ORIENTATION_0**
</dt> <dd> <dl> <dt>

0x004
</dt> <dt>



Orientación del dispositivo.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIENTATION_90"></span><span id="pdc_orientation_90"></span>**PDC_ORIENTATION_90**
</dt> <dd> <dl> <dt>

0x008
</dt> <dt>



Orientación del dispositivo.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIENTATION_180"></span><span id="pdc_orientation_180"></span>**PDC_ORIENTATION_180**
</dt> <dd> <dl> <dt>

0x010
</dt> <dt>



Orientación del dispositivo.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIENTATION_270"></span><span id="pdc_orientation_270"></span>**PDC_ORIENTATION_270**
</dt> <dd> <dl> <dt>

0x020
</dt> <dt>



Orientación del dispositivo.


</dt> </dl> </dd> <dt>

<span id="PDC_MODE_DEFAULT"></span><span id="pdc_mode_default"></span>**PDC_MODE_DEFAULT**
</dt> <dd> <dl> <dt>

0x040
</dt> <dt>



Modo de presentación predeterminado.


</dt> </dl> </dd> <dt>

<span id="PDC_MODE_CENTERED"></span><span id="pdc_mode_centered"></span>**PDC_MODE_CENTERED**
</dt> <dd> <dl> <dt>

0x080
</dt> <dt>



Modo de presentación centrado.


</dt> </dl> </dd> <dt>

<span id="PDC_MAPPING_CHANGE"></span><span id="pdc_mapping_change"></span>**PDC_MAPPING_CHANGE**
</dt> <dd> <dl> <dt>

0x100
</dt> <dt>



Cambio en la presentación en la asignación del digitalizador.


</dt> </dl> </dd> <dt>

<span id="PDC_RESOLUTION"></span><span id="pdc_resolution"></span>**PDC_RESOLUTION**
</dt> <dd> <dl> <dt>

0x200
</dt> <dt>



Resolución de pantalla.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIGIN"></span><span id="pdc_origin"></span>**PDC_ORIGIN**
</dt> <dd> <dl> <dt>

0x400
</dt> <dt>



El origen de la presentación.


</dt> </dl> </dd> <dt>

<span id="PDC_MODE_ASPECTRATIOPRESERVED"></span><span id="pdc_mode_aspectratiopreserved"></span>**PDC_MODE_ASPECTRATIOPRESERVED**
</dt> <dd> <dl> <dt>

0x800
</dt> <dt>



La relación de aspecto de la pantalla.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





