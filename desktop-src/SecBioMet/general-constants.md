---
title: Constantes generales (Winbio \_ types.h)
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
ms.openlocfilehash: 686e94c936855d3b5466071fba7d8b629a492579de11a53a62d8b23345707c53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119740455"
---
# <a name="general-constants-winbio_typesh"></a>Constantes generales (Winbio \_ types.h)

Las siguientes constantes se usan en todo el Windows Biometric Framework.



| Constante o valor                                                                                                                                                                                                                                                                   | Descripción                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <dt>**TAMAÑO \_ MÁXIMO \_ DE SID DE \_ SEGURIDAD**</dt> </dl>                                                                                          | Longitud máxima de un valor de identificador de seguridad (SID). Actualmente es 68.<br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <dt>**IDENTIFICADOR DE \_ UNIDAD \_ WINBIO**</dt> </dl>                                                                                                                | Número de identificador de una unidad biométrica.<br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <dt>**IDENTIFICADOR DE \_ SESIÓN DE \_ WINBIO**</dt> </dl>                                                                                           | Entero largo sin signo que contiene el identificador de una sesión biométrica abierta.<br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <dt>**IDENTIFICADOR DEL MARCO WINBIO \_ \_**</dt> </dl>                                                                                     | Entero largo sin signo que contiene el identificador de una sesión de marco abierto.<br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <dt>**UUID de WINBIO \_**</dt> </dl>                                                                                                                          | Un GUID.<br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <dt>**CADENA \_ WINBIO**</dt> </dl>                                                                                                                    | Matriz de bytes que contiene una cadena Unicode terminada en NULL.<br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <dt>**WINBIO \_ MAX \_ STRING \_ LEN**</dt> </dl>                                                                                       | Longitud máxima de un **valor STRING \_ de WINBIO.** Actualmente, es 256.<br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <dt>**WINBIO \_ TAMAÑO \_ MÁXIMO DE BÚFER DE \_ \_ EJEMPLO**</dt> <dt>0x7FFFFFFF</dt> </dl> | Número máximo de bytes en una única captura de datos biométricos.<br/>                  |



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

 

 





