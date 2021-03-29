---
description: Los valores definen un tipo de SAS específico.
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: WLX_SAS_TYPE_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a75c7d7a71855700c4c8c233db3cfc18e06b9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648555"
---
# <a name="wlx_sas_type_xxx"></a>WLX \_ SAS \_ tipo \_ XXX

\[La \_ constante de \_ tipo \_ XXX de SAS de WLX ya no está disponible para su uso en Windows Server 2008 y Windows Vista.\]

Los valores de **\_ \_ tipo \_ XXX de SAS de WLX** definen un tipo de SAS específico.

> [!Note]  
> Los archivos dll de GINA se omiten en Windows Vista.

 

Todos los valores de cero a 127 se reservan para los tipos definidos por Microsoft. Los valores por encima de 127 están disponibles para los tipos definidos por el cliente. Los tipos siguientes se pasan a las funciones que tienen un parámetro *dwSasType* .



| Constante                                                                                                                                                                                                         | Descripción                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <dt>**WLX \_ tipo de SAS \_ \_ Ctrl \_ ALT \_ Supr**</dt> </dl>            | Indica que un usuario ha escrito las SA estándar CTRL + ALT + SUPR.<br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <dt>**WLX \_ SAS \_ Type \_ SC \_ Insert**</dt> </dl>                      | Indica que se ha insertado una [*tarjeta inteligente*](../secgloss/s-gly.md) en un dispositivo compatible.<br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <dt>**WLX \_ SAS \_ tipo \_ SC \_ Remove**</dt> </dl>                      | Indica que se ha quitado una tarjeta inteligente de un dispositivo compatible.<br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <dt>**WLX \_ tipo de SAS \_ \_ SCRNSVR \_ actividad**</dt> </dl> | Indica que la actividad del teclado o del mouse se produjo mientras estaba activo un protector de pantalla seguro.<br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <dt>**WLX \_ tipo de SAS \_ \_ SCRNSVR \_ tiempo de espera**</dt> </dl>    | Indica que se ha producido la activación del protector de pantalla debido a la inactividad del teclado y del mouse.<br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <dt>**WLX \_ \_ tiempo de espera de tipo SAS \_**</dt> </dl>                             | Indica que no se ha recibido ninguna entrada de usuario dentro del período de tiempo de espera especificado.<br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <dt>**\_cierre de \_ \_ sesión de usuario de tipo SAS de WLX \_**</dt> </dl>                | Indica que el usuario está cerrando la sesión del sistema.<br/>                                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winwlx. h</dt> </dl> |



 

 
