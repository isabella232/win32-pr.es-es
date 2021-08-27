---
description: Al crear un paquete de seguridad del proveedor de soporte técnico de seguridad (SSP), no debe permitir que el cliente unido a un dominio se autentique en un controlador de dominio mediante un nombre de proveedor de servicios (SPN) de dos partes con el formato siguiente.
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: Usar nombres de entidad de seguridad de tres partes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ddc9ce552e71d97c5e795b7405e97803991133a96e7b3fac3e1a81bc45d5ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915196"
---
# <a name="using-three-part-principal-names"></a>Usar nombres de entidad de seguridad de tres partes

Al crear un paquete de seguridad del proveedor de soporte técnico de seguridad (SSP), no debe permitir que el cliente unido a un dominio se autentique en un controlador de dominio mediante un nombre de proveedor de servicios (SPN) de dos partes con el formato siguiente.

-   <*protocolo* >/< *nombre de host*>

Un cliente siempre debe autenticarse especificando el dominio.

-   <*protocolo* >/< *nombre de host* >/< *nombre de dominio*>

Un cliente unido a un dominio que inicia sesión con un SPN de dos partes puede suplantar al controlador de dominio. Si permite dos SPN de dos partes, debe crear una entrada de registro que contenga información suficiente para permitir que el administrador identifique al autor de la llamada.

 

 



