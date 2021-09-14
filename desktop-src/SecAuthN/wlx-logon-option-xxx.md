---
description: El parámetro dwOptions de WlxLoggedOutSAS usa valores.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (Winwlx.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8909f562b87eb3a8147b0684d9676b9ac55d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160867"
---
# <a name="wlx_logon_option_xxx"></a>OPCIÓN DE INICIO DE SESIÓN DE WLX \_ \_ \_ XXX

\[La constante WLX LOGON OPTION XXX ya no está disponible para su uso a partir \_ \_ de Windows Server \_ 2008 y Windows Vista.\]

El parámetro *dwOptions* de [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas)usa los valores **DE WLX \_ LOGON \_ OPTION \_** XXX.

> [!Note]  
> Los archivos DLL de GINA se omiten Windows Vista.

 

Tras un inicio de sesión correcto, el archivo DLL de GINA puede usar este valor para especificar la opción siguiente.



| Constante                                                                                                                                                                                          | Descripción                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <dt>**WLX \_ LOGON \_ OPT \_ NO \_ PROFILE**</dt> </dl> | Especifica que Winlogon no debe cargar un perfil para el usuario que ha iniciado sesión. En este caso, el archivo DLL de GINA cargará el perfil o el usuario no necesita un perfil.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winwlx.h</dt> </dl> |



 

 




