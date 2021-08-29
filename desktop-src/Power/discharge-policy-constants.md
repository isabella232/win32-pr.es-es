---
description: En la lista siguiente se describen las constantes de directiva de descarga.
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: Constantes de directiva de descarga (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a05237b7555cc7281f132f02110a10cb5b58cd342d6872b16c1a6319773ea8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961875"
---
# <a name="discharge-policy-constants"></a>Constantes de directiva de descarga

En la lista siguiente se describen las constantes de directiva de descarga.



| Constante o valor                                                                                                                                                                                                                                            | Descripción                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> <dt>**DESAPROBACIÓN \_ POLICY \_ CRITICAL**</dt> <dt>0</dt> </dl> | Cuál de las configuraciones de directiva de descarga de batería [**(estructuras \_ SYSTEM POWER \_ LEVEL)**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) se usa cuando la batería se descarga por debajo del umbral crítico.<br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> <dt>**DESAPROBACIÓN \_ DIRECTIVA \_ BAJA**</dt> <dt>1</dt> </dl>                | Cuál de las configuraciones de directiva de descarga de batería [**(estructuras \_ SYSTEM POWER \_ LEVEL)**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) se usa cuando la batería se descarga por debajo del umbral bajo.<br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> <dt>**NUM \_ DIRECTIVAS DE \_ DESCARGA**</dt> <dt>4</dt> </dl>          | Número de configuraciones de directiva de descarga de batería [**(estructuras \_ SYSTEM POWER \_ LEVEL)**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) especificadas.<br/>                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>WinNT.h (incluir Windows.h)</dt> </dl> |



 

 




