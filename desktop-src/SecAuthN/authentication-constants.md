---
description: Enumera las constantes usadas para las API de autenticación de Microsoft.
ms.assetid: 3e5b7fd8-01bf-4090-b68f-006b7e2228a9
title: Constantes de autenticación (autenticación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83345ffde59816a8c15276963cd9d60f2d2d24d179ed06acd2175aacb33ba2c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101395"
---
# <a name="authentication-constants-authentication"></a>Constantes de autenticación (autenticación)

## <a name="credentials-management-constants"></a>Constantes de administración de credenciales

Administración de credenciales usa las constantes siguientes para especificar el tamaño máximo de cadena.



| Constante                                        | Descripción                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| CREDUI \_ MAX \_ MESSAGE \_ LENGTH<br/>         | Número máximo de caracteres para el **miembro pszMessageText** de una [**estructura INFO \_ de CREDUI.**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa)<br/> |
| CREDUI \_ MAX \_ CAPTION \_ LENGTH<br/>         | Número máximo de caracteres para el **miembro pszCaptionText** de una [**estructura INFO \_ de CREDUI.**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa)<br/> |
| CREDUI \_ MAX \_ GENERIC \_ TARGET \_ LENGTH<br/> | Número máximo de caracteres de una cadena que especifica un nombre de destino.<br/>                                             |
| CREDUI \_ MAX \_ DOMAIN \_ TARGET \_ LENGTH<br/>  | Número máximo de caracteres de una cadena que especifica un nombre de dominio.<br/>                                             |
| CREDUI \_ MAX \_ USERNAME \_ LENGTH<br/>        | Número máximo de caracteres de una cadena que especifica un nombre de cuenta de usuario.<br/>                                       |
| CREDUI \_ MAX \_ PASSWORD \_ LENGTH<br/>        | Número máximo de caracteres de una cadena que especifica una contraseña.<br/>                                                |



 

## <a name="gina-defined-values"></a>Valores definidos por Gina

[*Las funciones de*](/windows/desktop/SecGloss/g-gly) interfaz GINA y [*las funciones de compatibilidad de Winlogon*](/windows/desktop/SecGloss/w-gly) usan los siguientes valores definidos.

> [!Note]  
> Los archivos DLL de GINA se omiten en Windows Vista.

 



| Value                                                              | Descripción                                                                                                                          |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**OPCIÓN DE INICIO DE SESIÓN DE WLX \_ \_ \_ XXX**](wlx-logon-option-xxx.md)<br/> | Contiene opciones de inicio de sesión predefinidas. Lo usa el *parámetro dwOptions* de [**WlxLoggedOutSAS.**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas)<br/> |
| [**WLX \_ SAS \_ TYPE \_ XXX**](wlx-sas-type-xxx.md)<br/>         | Define un tipo de SAS específico.<br/>                                                                                              |



 

 

