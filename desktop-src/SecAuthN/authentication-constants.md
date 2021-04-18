---
description: Muestra las constantes utilizadas para las API de autenticación de Microsoft.
ms.assetid: 3e5b7fd8-01bf-4090-b68f-006b7e2228a9
title: Constantes de autenticación (autenticación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d671f356f11ccaf1f5aece1dc1168d3106d578c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648575"
---
# <a name="authentication-constants-authentication"></a>Constantes de autenticación (autenticación)

## <a name="credentials-management-constants"></a>Constantes de administración de credenciales

La administración de credenciales utiliza las siguientes constantes para especificar tamaños de cadena máximos.



| Constante                                        | Descripción                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \_longitud máxima del \_ mensaje \_ de CREDUI<br/>         | Número máximo de caracteres para el miembro **pszMessageText** de una estructura de [**\_ información de CREDUI**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .<br/> |
| CREDUI \_ longitud máxima del \_ título \_<br/>         | Número máximo de caracteres para el miembro **pszCaptionText** de una estructura de [**\_ información de CREDUI**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .<br/> |
| \_longitud máxima \_ de \_ destino \_ genérico de CREDUI<br/> | Número máximo de caracteres de una cadena que especifica un nombre de destino.<br/>                                             |
| \_longitud máxima \_ de \_ destino de dominio \_ de CREDUI<br/>  | Número máximo de caracteres de una cadena que especifica un nombre de dominio.<br/>                                             |
| \_longitud máxima de \_ nombre de usuario de CREDUI \_<br/>        | Número máximo de caracteres de una cadena que especifica un nombre de cuenta de usuario.<br/>                                       |
| CREDUI \_ longitud máxima de la \_ contraseña \_<br/>        | Número máximo de caracteres de una cadena que especifica una contraseña.<br/>                                                |



 

## <a name="gina-defined-values"></a>Valores definidos de Gina

Las funciones de la interfaz [*Gina*](/windows/desktop/SecGloss/g-gly) y las funciones de compatibilidad con [*Winlogon*](/windows/desktop/SecGloss/w-gly) usan los siguientes valores definidos.

> [!Note]  
> Los archivos dll de GINA se omiten en Windows Vista.

 



| Value                                                              | Descripción                                                                                                                          |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**WLX \_ opción de inicio de sesión \_ \_ XXX**](wlx-logon-option-xxx.md)<br/> | Contiene opciones de inicio de sesión predefinidas. Lo usa el parámetro *dwOptions* de [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).<br/> |
| [**WLX \_ SAS \_ tipo \_ XXX**](wlx-sas-type-xxx.md)<br/>         | Define un tipo de SAS específico.<br/>                                                                                              |



 

 

