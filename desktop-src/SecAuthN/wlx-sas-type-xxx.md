---
description: Los valores definen un tipo de SAS específico.
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: WLX_SAS_TYPE_XXX (Winwlx.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a75c7d7a71855700c4c8c233db3cfc18e06b9d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160868"
---
# <a name="wlx_sas_type_xxx"></a>WLX \_ SAS \_ TYPE \_ XXX

\[La constante WLX SAS TYPE XXX ya no está disponible para su uso a partir \_ \_ de Windows Server \_ 2008 y Windows Vista.\]

Los **valores DE TIPO XXX de SAS \_ \_ \_ de WLX** definen un tipo de SAS específico.

> [!Note]  
> Los archivos DLL de GINA se omiten Windows Vista.

 

Todos los valores de cero a 127 están reservados para los tipos definidos por Microsoft. Los valores anteriores a 127 están disponibles para los tipos definidos por el cliente. Los siguientes tipos se pasan a las funciones que tienen un *parámetro dwSasType.*



| Constante                                                                                                                                                                                                         | Descripción                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <dt>**WLX \_ SAS \_ TYPE \_ CTRL \_ ALT \_ DEL**</dt> </dl>            | Indica que un usuario ha especificado la SAS estándar CTRL+ALT+SUPR.<br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <dt>**WLX \_ SAS \_ TYPE \_ SC \_ INSERT**</dt> </dl>                      | Indica que se [*ha insertado una*](../secgloss/s-gly.md) tarjeta inteligente en un dispositivo compatible.<br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <dt>**WLX \_ SAS \_ TYPE \_ SC \_ REMOVE**</dt> </dl>                      | Indica que se ha quitado una tarjeta inteligente de un dispositivo compatible.<br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <dt>**ACTIVIDAD \_ \_ SCRNSVR DE TIPO \_ SAS DE \_ WLX**</dt> </dl> | Indica que la actividad del teclado o del mouse se produjo mientras estaba activo un protector de pantalla seguro.<br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <dt>**TIEMPO DE ESPERA \_ DE \_ \_ SCRNSVR DE TIPO SAS \_ DE WLX**</dt> </dl>    | Indica que se ha producido la activación del protector de pantalla debido a la inactividad del teclado y del mouse.<br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <dt>**TIEMPO DE ESPERA \_ DE TIPO DE SAS \_ DE WLX \_**</dt> </dl>                             | Indica que no se recibió ninguna entrada del usuario dentro del período de tiempo de espera especificado.<br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <dt>**CIERRE DE \_ SESIÓN DE USUARIO DE TIPO SAS \_ \_ \_ DE WLX**</dt> </dl>                | Indica que el usuario ha cerrado la sesión del sistema.<br/>                                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winwlx.h</dt> </dl> |



 

 
