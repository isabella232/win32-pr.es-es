---
title: Constantes generales (Winbio \_ Types. h)
description: Especifique la longitud máxima del SID, los identificadores, los identificadores, la longitud máxima de la cadena y el tamaño máximo del búfer de muestra.
ms.assetid: 62e87bd8-a708-4d00-aaa8-9cac8e3736a7
topic_type:
- apiref
api_name:
- SECURITY_MAX_SID_SIZE
- WINBIO_UNIT_ID
- WINBIO_SESSION_HANDLE
- WINBIO_FRAMEWORK_HANDLE
- WINBIO_UUID
- WINBIO_STRING
- WINBIO_MAX_STRING_LEN
- WINBIO_MAX_SAMPLE_BUFFER_SIZE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e35aa4c2cc676935cfb80fdec8729daf64d5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996389"
---
# <a name="general-constants-winbio_typesh"></a>Constantes generales (Winbio \_ Types. h)

En el Plataforma de biometría de Windows se usan las siguientes constantes.



| Constante o valor                                                                                                                                                                                                                                                                   | Descripción                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <dt>**\_tamaño máximo de \_ SID \_ de seguridad**</dt> </dl>                                                                                          | La longitud máxima de un valor de identificador de seguridad (SID). Actualmente es 68.<br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <dt>**\_identificador de unidad de WINBIO \_**</dt> </dl>                                                                                                                | Número de identificación de una unidad biométrica.<br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <dt>**\_identificador de sesión de WINBIO \_**</dt> </dl>                                                                                           | Entero largo sin signo que contiene el identificador de una sesión biométrica abierta.<br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <dt>**\_identificador del marco de WINBIO \_**</dt> </dl>                                                                                     | Entero largo sin signo que contiene el identificador de una sesión de marco abierta.<br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <dt>**\_UUID WINBIO**</dt> </dl>                                                                                                                          | Un GUID.<br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <dt>**\_cadena WINBIO**</dt> </dl>                                                                                                                    | Matriz de bytes que contiene una cadena Unicode terminada en NULL.<br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <dt>**WINBIO \_ \_ \_ longitud máxima de cadena**</dt> </dl>                                                                                       | La longitud máxima de un valor de **\_ cadena de WINBIO** . Actualmente es 256.<br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <dt>**WINBIO \_ \_ \_ \_ Tamaño máximo de búfer de ejemplo**</dt> <dt>0x7FFFFFFF</dt> </dl> | Número máximo de bytes en una captura de datos biométricos única.<br/>                  |



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

 

 





