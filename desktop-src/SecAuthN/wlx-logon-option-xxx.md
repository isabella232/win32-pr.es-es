---
description: Los valores son usados por el parámetro dwOptions de WlxLoggedOutSAS.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8909f562b87eb3a8147b0684d9676b9ac55d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361026"
---
# <a name="wlx_logon_option_xxx"></a>WLX \_ opción de inicio de sesión \_ \_ XXX

\[La \_ constante XXX de la opción de inicio de sesión WLX ya \_ \_ no está disponible para su uso en Windows Server 2008 y Windows Vista.\]

El parámetro *dwOptions* de [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas)usa los valores de la **opción de inicio de \_ sesión \_ \_ WLX** .

> [!Note]  
> Los archivos dll de GINA se omiten en Windows Vista.

 

Tras un inicio de sesión correcto, el archivo DLL de GINA puede usar este valor para especificar la opción siguiente.



| Constante                                                                                                                                                                                          | Descripción                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <dt>**WLX \_ Inicio de sesión \_ \_ no opt ningún \_ Perfil**</dt> </dl> | Especifica que Winlogon no debe cargar un perfil para el usuario que ha iniciado sesión. En este caso, el archivo DLL de GINA cargará el perfil o el usuario no necesita un perfil.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winwlx. h</dt> </dl> |



 

 




