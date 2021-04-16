---
description: Al crear un paquete de seguridad del proveedor de compatibilidad para seguridad (SSP), no debe permitir que el cliente unido a un dominio se autentique en un controlador de dominio mediante el uso de un nombre de proveedor de servicios (SPN) de dos partes con el formato siguiente.
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: Usar tres nombres principales de parte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760ba740843c62c39a98e7e4683d25410a94ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666461"
---
# <a name="using-three-part-principal-names"></a>Usar tres nombres principales de parte

Al crear un paquete de seguridad del proveedor de compatibilidad para seguridad (SSP), no debe permitir que el cliente unido a un dominio se autentique en un controlador de dominio mediante el uso de un nombre de proveedor de servicios (SPN) de dos partes con el formato siguiente.

-   <*Protocolo* >/< de *nombre de host*>

Un cliente debe autenticarse siempre especificando el dominio.

-   <*Protocolo* >/< de *nombre* >/< de host *nombre de dominio*>

Un cliente unido a un dominio que inicia sesión con un SPN de dos partes puede suplantar al controlador de dominio. Si permite dos SPN de partes, debe crear una entrada de registro que contenga información suficiente para permitir que el administrador identifique al autor de la llamada.

 

 



