---
description: Las constantes de marcas globales se usan para habilitar o deshabilitar las opciones de directiva de energía del usuario.
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: Constantes de marcas globales (PowrProf.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd31340e3e7daf4f9dd034c3fa2db333680a626
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062864"
---
# <a name="global-flags-constants"></a>Constantes de marcas globales

Las constantes de marcas globales se usan para habilitar o deshabilitar las opciones de directiva de energía del usuario.



| Constante o valor                                                                                                                                                                                                                                                                                         | Descripción                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt> </dl> | Habilita o deshabilita la visualización de varias baterías en el medidor de energía del sistema.<br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <dt>**EnablePasswordLogon**</dt> <dt>0x04</dt> </dl>                         | Habilita o deshabilita la necesidad de iniciar sesión con contraseña cuando el sistema se reanuda de modo de espera o hibernación.<br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt> </dl> | Habilita o deshabilita el icono del medidor de batería en la bandeja del sistema. Cuando se borra esta marca, no se muestra el icono del medidor de baterías.<br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt> </dl>                 | Habilita o deshabilita la compatibilidad para atenuar la pantalla de vídeo cuando el sistema cambia de ejecutarse en la alimentación de CA a ejecutarse con batería.<br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <dt>**EnableWakeOnRing**</dt> <dt>0x08</dt> </dl>                                     | Habilita o deshabilita la activación en la compatibilidad con anillos.<br/>                                                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>PowrProf.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DIRECTIVA \_ DE ENERGÍA DE USUARIO \_ \_ GLOBAL**](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 




