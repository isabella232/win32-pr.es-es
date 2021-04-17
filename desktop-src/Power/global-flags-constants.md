---
description: Las constantes de las marcas globales se utilizan para habilitar o deshabilitar las opciones de directiva de energía de usuario.
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: Constantes de marcas globales (PowrProf. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd31340e3e7daf4f9dd034c3fa2db333680a626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667214"
---
# <a name="global-flags-constants"></a>Constantes de marcas globales

Las constantes de las marcas globales se utilizan para habilitar o deshabilitar las opciones de directiva de energía de usuario.



| Constante o valor                                                                                                                                                                                                                                                                                         | Descripción                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt> </dl> | Habilita o deshabilita la visualización de varias baterías en el medidor de energía del sistema.<br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <dt>**EnablePasswordLogon**</dt> <dt>0x04</dt> </dl>                         | Habilita o deshabilita la necesidad de inicio de sesión de contraseña cuando el sistema se reanuda desde el modo de espera o hibernación.<br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt> </dl> | Habilita o deshabilita el icono del medidor de la batería en la bandeja del sistema. Cuando esta marca está desactivada, no se muestra el icono del medidor de la batería.<br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt> </dl>                 | Habilita o deshabilita la compatibilidad para atenuar el vídeo que se muestra cuando el sistema cambia de funcionar con corriente alterna a la energía de la batería.<br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <dt>**EnableWakeOnRing**</dt> <dt>0x08</dt> </dl>                                     | Habilita o deshabilita la compatibilidad con Wake on Ring.<br/>                                                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>PowrProf. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Directiva de \_ energía de usuario global \_**](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 




