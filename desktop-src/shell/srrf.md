---
description: Marcas que restringen los datos que se van a establecer o devolver.
title: SRRF (shlwapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c9dbffd1-3b3e-4a25-89ee-1666e2812a62
api_name:
- SRRF_RT_REG_NONE
- SRRF_RT_REG_SZ
- SRRF_RT_REG_EXPAND_SZ
- SRRF_RT_REG_BINARY
- SRRF_RT_REG_DWORD
- SRRF_RT_REG_MULTI_SZ
- SRRF_RT_REG_QWORD
- SRRF_RT_DWORD
- SRRF_RT_QWORD
- SRRF_RT_ANY
- SRRF_RM_ANY
- SRRF_RM_NORMAL
- SRRF_RM_SAFE
- SRRF_RM_SAFENETWORK
- SRRF_NOEXPAND
- SRRF_ZEROONFAILURE
- SRRF_NOVIRT
api_type:
- HeaderDef
api_location:
- Shlwapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3ba36b64496413a54e6d8b8b96c16c265367d05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082806"
---
# <a name="srrf"></a>SRRF

Marcas que restringen los datos que se van a establecer o devolver.



| Constante o valor                                                                                                                                                                                                                                           | Descripción                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SRRF_RT_REG_NONE"></span><span id="srrf_rt_reg_none"></span><dl> <dt>**SRRF \_ RT \_ reg \_ ninguno**</dt> <dt>0x00000001</dt> </dl>                 | Escriba REG \_ None.<br/>                                                                                                                                                                                             |
| <span id="SRRF_RT_REG_SZ"></span><span id="srrf_rt_reg_sz"></span><dl> <dt>**SRRF \_ RT \_ reg \_ SZ**</dt> <dt>0x00000002</dt> </dl>                       | Escriba REG \_ SZ. REG \_ Expand \_ Types se convierten automáticamente en REG \_ SZ a menos que \_ se especifique la marca SRRF NOEXPAND.<br/>                                                                                     |
| <span id="SRRF_RT_REG_EXPAND_SZ"></span><span id="srrf_rt_reg_expand_sz"></span><dl> <dt>**SRRF \_ RT \_ reg \_ expanda \_ SZ**</dt> <dt>0x00000004</dt> </dl> | Escriba REG \_ Expander \_ . Si recupera un valor, también debe obtener la \_ marca SRRF NOEXPAND, o bien se produce un error en [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) con un \_ parámetro no válido \_ .<br/>                                     |
| <span id="SRRF_RT_REG_BINARY"></span><span id="srrf_rt_reg_binary"></span><dl> <dt>**SRRF \_ RT \_ reg \_ binario**</dt> <dt>0x00000008</dt> </dl>           | Escriba REG \_ Binary.<br/>                                                                                                                                                                                           |
| <span id="SRRF_RT_REG_DWORD"></span><span id="srrf_rt_reg_dword"></span><dl> <dt>**SRRF \_ RT \_ reg \_ DWORD**</dt> <dt>0x00000010</dt> </dl>              | Escriba REG \_ DWORD.<br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_REG_MULTI_SZ"></span><span id="srrf_rt_reg_multi_sz"></span><dl> <dt>**SRRF \_ RT \_ reg \_ multi \_ SZ**</dt> <dt>0x00000020</dt> </dl>    | Escriba REG \_ multi \_ SZ.<br/>                                                                                                                                                                                        |
| <span id="SRRF_RT_REG_QWORD"></span><span id="srrf_rt_reg_qword"></span><dl> <dt>**SRRF \_ RT \_ reg \_ QWord**</dt> <dt>0x00000040</dt> </dl>              | Escriba REG \_ QWord.<br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_DWORD"></span><span id="srrf_rt_dword"></span><dl> <dt>**SRRF \_ RT \_ DWORD**</dt> <dt>0x00000018</dt> </dl>                           | REG \_ DWORD y 32 bits reg \_ Binary Types. Es equivalente a SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ reg \_ DWORD. Si recupera un valor, si los datos binarios del valor son mayores de 32 bits, no se devuelve.<br/> |
| <span id="SRRF_RT_QWORD"></span><span id="srrf_rt_qword"></span><dl> <dt>**SRRF \_ 0x00000048 \_ QWord**</dt> <dt></dt> </dl>                           | \_Tipos binarios de reg QWord y 64 bits \_ . Esto es equivalente a SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ reg \_ QWord. Si recupera un valor, si los datos binarios del valor son mayores de 64 bits, no se devuelve.<br/> |
| <span id="SRRF_RT_ANY"></span><span id="srrf_rt_any"></span><dl> <dt>**SRRF \_ RT \_ any**</dt> <dt>0x0000FFFF</dt> </dl>                                 | Todos los tipos. Establezca esta marca si no \_ se establece ningún otro valor RT de SRRF.<br/>                                                                                                                                                 |
| <span id="SRRF_RM_ANY"></span><span id="srrf_rm_any"></span><dl> <dt>**SRRF \_ RM \_ cualquier**</dt> <dt>0x00000000</dt> </dl>                                 | No hay ninguna restricción de modo. Este es el valor predeterminado.<br/>                                                                                                                                                             |
| <span id="SRRF_RM_NORMAL"></span><span id="srrf_rm_normal"></span><dl> <dt>**SRRF \_ 0x00010000 de RM \_ normal**</dt> <dt></dt> </dl>                        | Restrinja el modo de inicio del sistema a "arranque normal".<br/>                                                                                                                                                              |
| <span id="SRRF_RM_SAFE"></span><span id="srrf_rm_safe"></span><dl> <dt>**SRRF \_ 0x00020000 \_ Safe de RM**</dt> <dt></dt> </dl>                              | Restrinja el modo de inicio del sistema a "modo seguro".<br/>                                                                                                                                                                |
| <span id="SRRF_RM_SAFENETWORK"></span><span id="srrf_rm_safenetwork"></span><dl> <dt>**SRRF \_ RM \_ SAFENETWORK**</dt> <dt>0x00040000</dt> </dl>         | Restrinja el modo de inicio del sistema a "modo seguro con funciones de red".<br/>                                                                                                                                                |
| <span id="SRRF_NOEXPAND"></span><span id="srrf_noexpand"></span><dl> <dt>**SRRF \_ NOEXPAND**</dt> <dt>0x10000000</dt> </dl>                            | No expanda automáticamente REG \_ Expand las \_ cadenas de entorno de.<br/>                                                                                                                                            |
| <span id="SRRF_ZEROONFAILURE"></span><span id="srrf_zeroonfailure"></span><dl> <dt>**SRRF \_ ZEROONFAILURE**</dt> <dt>0x20000000</dt> </dl>             | Si recupera un valor, si *pvData* no es **null**, establezca el contenido del búfer *pvData* en ceros en caso de error.<br/>                                                                                        |
| <span id="SRRF_NOVIRT"></span><span id="srrf_novirt"></span><dl> <dt>**SRRF \_ NOVIRT**</dt> <dt>0x40000000</dt> </dl>                                  | Al recuperar un valor, si la clave solicitada está virtualizada, se producirá un ERROR con el \_ archivo \_ no \_ encontrado.<br/>                                                                                                            |



## <a name="remarks"></a>Observaciones

Estos valores se definen en shlwapi. h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Shlwapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SHRegSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)
</dt> <dt>

[**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea)
</dt> </dl>

 

 




