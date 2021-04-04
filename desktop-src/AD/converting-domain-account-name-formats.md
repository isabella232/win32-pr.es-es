---
title: Convertir formatos de nombre de cuenta de dominio
description: Las funciones de Microsoft Win32 para trabajar con el administrador de control de servicios (SCM) en un servidor host usan el \ 0034; el \\ formato de dominio nombre de usuario \ 0034; para las cuentas de servicio.
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ab1a6d0022b0a47979c1f6b3434e6227c23c30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789604"
---
# <a name="converting-domain-account-name-formats"></a>Convertir formatos de nombre de cuenta de dominio

Las funciones de Microsoft Win32 para trabajar con el administrador de control de servicios (SCM) en un servidor host usan el <domain> \\ <username> formato "" para las cuentas de servicio. Por ejemplo, si llama a la función [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) para recuperar la cuenta de usuario en la que se ejecuta el servicio, la función devuelve el nombre en formato "fabrikam \\ juanpérez". Para enlazar con la cuenta de usuario en el directorio, por ejemplo, para cambiar la contraseña de la cuenta, se requiere el nombre distintivo de la cuenta, que tiene el formato "CN = Jeff Smith, CN = users, DC = Fabrikam, DC = COM".

Para realizar la conversión entre los distintos formatos de nombre, utilice la función [**TranslateName**](/windows/desktop/api/secext/nf-secext-translatenamea) , que puede convertir un nombre a otros formatos, como un nombre principal de usuario (UPN).

 

 