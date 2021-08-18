---
title: WINBIO_FLAG constantes (Winbio \_ types.h)
description: Especifique la configuración de la unidad biométrica y las características de acceso para la nueva sesión.
ms.assetid: 82b57023-6c27-433d-bf13-f136f501fc60
topic_type:
- apiref
api_name:
- WINBIO_FLAG_DEFAULT
- WINBIO_FLAG_BASIC
- WINBIO_FLAG_ADVANCED
- WINBIO_FLAG_RAW
- WINBIO_FLAG_MAINTENANCE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e018b1d810e3a57b4adea1116aa9bebc7b82dd44888b2d720e018329d31acf4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910315"
---
# <a name="winbio_flag-constants"></a>Constantes DE \_ MARCA WINBIO

Las siguientes constantes se pueden usar en la función [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para especificar la configuración de unidades biométricas y las características de acceso para la nueva sesión.



| Constante                                                                                                                                                                                     | Descripción                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <dt>**WINBIO \_ FLAG \_ DEFAULT**</dt> </dl>             | Marca de configuración del sensor. Las unidades biométricas funcionan de la manera especificada durante la instalación.<br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <dt>**WINBIO \_ FLAG \_ BASIC**</dt> </dl>                   | Marca de configuración del sensor. Las unidades biométricas solo funcionan como dispositivos de captura básicos.<br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <dt>**WINBIO \_ FLAG \_ ADVANCED**</dt> </dl>          | Marca de configuración del sensor. Las unidades biométricas usan funcionalidades de almacenamiento y procesamiento interno.<br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <dt>**WINBIO \_ FLAG \_ RAW**</dt> </dl>                         | Marca de acceso deseado. La aplicación cliente captura datos biométricos sin procesar [**mediante WinBioCaptureSample.**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample)<br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <dt>**MANTENIMIENTO DE \_ LA MARCA \_ WINBIO**</dt> </dl> | Marca de acceso deseado. El cliente realiza operaciones de control definidas por el proveedor en una unidad biométrica llamando a [**WinBioControlUnitPrivileged.**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged)<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





