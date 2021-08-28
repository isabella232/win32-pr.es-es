---
title: Convertir formatos de nombre de cuenta de dominio
description: Las funciones de Microsoft Win32 para trabajar con el administrador de control de servicios (SCM) en un servidor host usan \ 0034; nombre \\ de usuario del dominio \ 0034; formato para las cuentas de servicio.
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aaa1b3664cc0ad372f82b498153862e69013fb1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881592"
---
# <a name="converting-domain-account-name-formats"></a>Convertir formatos de nombre de cuenta de dominio

Las funciones de Microsoft Win32 para trabajar con el administrador de control de servicios (SCM) en un servidor host usan el formato "nombre de usuario de dominio" para &lt; &gt; \\ &lt; las cuentas &gt; de servicio. Por ejemplo, si llama a la función [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) para recuperar la cuenta de usuario con la que se ejecuta el servicio, la función devuelve el nombre en formato "Fabrikam \\ jeffsmith". Para enlazar a la cuenta de usuario en el directorio, por ejemplo, para cambiar la contraseña de la cuenta, se requiere el nombre distintivo de la cuenta, que tiene el formato "CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=COM".

Para realizar la conversión entre los distintos formatos de nombre, use la función [**TranslateName,**](/windows/desktop/api/secext/nf-secext-translatenamea) que puede convertir un nombre a otros formatos, como un nombre principal de usuario (UPN).

 

 
