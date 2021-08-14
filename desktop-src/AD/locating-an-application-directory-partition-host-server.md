---
title: Buscar un servidor host de partición de directorio de aplicación
description: En este tema se describe cómo buscar un servidor host de partición de directorio de aplicación.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Buscar un servidor host de partición de directorio de aplicación AD
- Application Directory Partitions AD , Buscar un servidor host
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3cef9442d694b80893f67d5530b83aa188df4d172028271117492ed221bd239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186796"
---
# <a name="locating-an-application-directory-partition-host-server"></a>Buscar un servidor host de partición de directorio de aplicación

El servicio NetLogon registra la siguiente lista de registros SRV para una partición de directorio de aplicación:

-   \_ldap. \_ Tcp.<partition name>
-   \_ldap. \_ tcp. <site name> . \_ Sitios.<partition name>

Para buscar un controlador de dominio que hospeda una réplica de una partición de directorio de aplicación especificada, llame a la función [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) con el parámetro *DomainName* establecido en el nombre DNS de la partición del directorio de la aplicación y la marca LDAP NEEDED de **DS \_ ONLY \_ \_** establecida en el parámetro *Flags.* Para obtener más información y un ejemplo de código que muestra, mediante la función **DsGetDcName,** cómo buscar un controlador de dominio que hospeda una réplica de una partición de directorio de aplicación, vea Ejemplo de código para buscar un servidor host de partición de directorio de aplicación [.](example-code-for-locating-an-application-directory-partition-host-server.md)

 

 




