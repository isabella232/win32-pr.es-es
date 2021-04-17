---
description: En la lista siguiente se describen las constantes de la Directiva de descargas.
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: Constantes de la Directiva de descarga (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 052d07a5fe538543b66ec8d48c940f63fe82a682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667220"
---
# <a name="discharge-policy-constants"></a>Constantes de la Directiva de descarga

En la lista siguiente se describen las constantes de la Directiva de descargas.



| Constante o valor                                                                                                                                                                                                                                            | Descripción                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> <dt>**Descarga \_ de DIRECTIVA \_ crítica**</dt> <dt>0</dt> </dl> | La configuración de la Directiva de descarga de la batería (estructuras de [**\_ \_ nivel de energía del sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) se usa cuando la batería se carga por debajo del umbral crítico.<br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> <dt>**Descarga \_ de DIRECTIVA \_ baja**</dt> <dt>1</dt> </dl>                | La configuración de la Directiva de descarga de la batería (estructuras de [**\_ \_ nivel de energía del sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) se usa cuando la batería se carga por debajo del umbral inferior.<br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> <dt>**Número \_ de \_Directivas de descarga**</dt> <dt>4</dt> </dl>          | Número de opciones de configuración de la Directiva de descarga de la batería (estructuras de [**\_ \_ nivel de energía del sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) especificadas.<br/>                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Winnt. h (incluye Windows. h)</dt> </dl> |



 

 




