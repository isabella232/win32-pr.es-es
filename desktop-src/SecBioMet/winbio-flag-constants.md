---
title: Constantes de WINBIO_FLAG (Winbio \_ Types. h)
description: Especifique la configuración de unidades biométricas y las características de acceso para la nueva sesión.
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
ms.openlocfilehash: 9ed632b5f15cc3d6a7ac6b0c6c70a2b3431b73db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422041"
---
# <a name="winbio_flag-constants"></a>\_Constantes de marca WINBIO

Se pueden usar las siguientes constantes en la función [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para especificar la configuración de unidad biométrica y las características de acceso para la nueva sesión.



| Constante                                                                                                                                                                                     | Descripción                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <dt>**WINBIO \_ marca \_ predeterminada**</dt> </dl>             | Marca de configuración del sensor. Las unidades biométricas funcionan de la manera especificada durante la instalación.<br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <dt>**marca de WINBIO \_ \_ básica**</dt> </dl>                   | Marca de configuración del sensor. Las unidades biométricas funcionan solo como dispositivos de captura básicos.<br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <dt>**\_marca WINBIO \_ avanzada**</dt> </dl>          | Marca de configuración del sensor. Las unidades biométricas usan funciones internas de procesamiento y almacenamiento.<br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <dt>**marca de WINBIO \_ \_ sin formato**</dt> </dl>                         | Marca de acceso deseada. La aplicación cliente captura datos biométricos sin procesar mediante [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).<br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <dt>**mantenimiento de la \_ marca WINBIO \_**</dt> </dl> | Marca de acceso deseada. El cliente realiza operaciones de control definidas por el proveedor en una unidad biométrica mediante una llamada a [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





