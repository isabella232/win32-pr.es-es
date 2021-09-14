---
description: En la lista siguiente se describen las constantes de directiva de descarga.
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: Constantes de directiva de descarga (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 052d07a5fe538543b66ec8d48c940f63fe82a682
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062869"
---
# <a name="discharge-policy-constants"></a>Constantes de directiva de descarga

En la lista siguiente se describen las constantes de directiva de descarga.



| Constante o valor                                                                                                                                                                                                                                            | Descripción                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> <dt>**DESAPROBACIÓN \_ DIRECTIVA \_ CRÍTICA**</dt> <dt>0</dt> </dl> | Cuál de las configuraciones de directiva de descarga de batería [**(estructuras \_ DE NIVEL \_ DE ENERGÍA**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) DEL SISTEMA) se usa cuando la batería se descarga por debajo del umbral crítico.<br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> <dt>**DESAPROBACIÓN \_ DIRECTIVA \_ BAJA**</dt> <dt>1</dt> </dl>                | Cuál de las configuraciones de directiva de descarga de batería [**(estructuras \_ SYSTEM POWER \_ LEVEL)**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) se usa cuando la batería se descarga por debajo del umbral bajo.<br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> <dt>**NUM \_ DIRECTIVAS \_ DE DESCARGA**</dt> <dt>4</dt> </dl>          | Número de configuraciones de directiva de descarga de batería [**(estructuras \_ SYSTEM POWER \_ LEVEL)**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) especificadas.<br/>                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>WinNT.h (incluir Windows.h)</dt> </dl> |



 

 




