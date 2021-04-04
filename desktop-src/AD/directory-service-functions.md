---
title: Funciones del servicio de directorio (AD DS)
description: Las funciones de servicio de directorio proporcionan una utilidad para buscar un controlador de dominio (DC) en un dominio de Windows NT o Windows 2000.
ms.assetid: 7b519c81-5a6c-470a-a525-1894efd53305
ms.tgt_platform: multiple
keywords:
- Funciones del servicio de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b071128806926e07cf61d62e53b823d8e7e1ac
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2019
ms.locfileid: "104077207"
---
# <a name="directory-service-functions-ad-ds"></a>Funciones del servicio de directorio (AD DS)

Las funciones de servicio de directorio proporcionan una utilidad para buscar un controlador de dominio (DC) en un dominio de Windows NT o Windows 2000. La arquitectura interactúa con los clientes, así como con los servidores en todas las versiones de Windows NT y Windows 2000. Las siguientes funciones permiten a los desarrolladores trabajar con el controlador de dominio y la pertenencia al dominio en el servicio de directorio:

-   [**DsAddressToSiteNames**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesa)
-   [**DsAddressToSiteNamesEx**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesexa)
-   [**DsDeregisterDnsHostRecords**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsderegisterdnshostrecordsa)
-   [**DsEnumerateDomainTrusts**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsenumeratedomaintrustsa)
-   [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)
-   [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)
-   [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)
-   [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)
-   [**DsGetDcSiteCoverage**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcsitecoveragea)
-   [**DsGetForestTrustInformationW**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetforesttrustinformationw)
-   [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea)
-   [**DsMergeForestTrustInformationW**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsmergeforesttrustinformationw)
-   [**DsRoleFreeMemory**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolefreememory)
-   [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation)
-   [**DsValidateSubnetName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea)

El servicio NetLogon implementa el ubicador de DC, [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea). Cada DC registra su nombre DNS en el servidor DNS y su nombre NetBIOS mediante un mecanismo específico de transporte, por ejemplo, en WINS. El localizador de DC busca el nombre y, a continuación, envía un datagrama al DC que registró el nombre, o hace ping en él. En el caso de los nombres de dominio NetBIOS, el datagrama es un mensaje de buzón. En el caso de los nombres de dominio DNS, el datagrama es una búsqueda UDP de LDAP. Cada uno de estos DC responde que indica que está operativo actualmente. El primer controlador de dominio que responde se devuelve al autor de la llamada.

El controlador de dominio devuelto se almacena en caché, por lo que los llamadores subsiguientes no necesitan repetir el algoritmo anterior y animar a todos los autores de llamadas a usar ese mismo DC. Esto garantiza que un solo cliente tiene una vista coherente del contenido del controlador de dominio.

Al buscar un DC por el nombre de dominio DNS, el ubicador de DC intenta encontrar un controlador de dominio en el sitio "más cercano". Cada DC registra registros DNS adicionales que indican en qué sitio se encuentra el controlador de dominio y qué sitios incluye el controlador de dominio. El ubicador de DC primero busca este registro DNS específico del sitio antes de buscar el registro de DNS que no es específico del sitio y, por tanto, precede un controlador de dominio en ese sitio. Cuando el ubicador de DC envía un datagrama al controlador de dominio, el controlador de dominio busca la dirección IP del cliente en el contenedor configuración/sitios/subred del DS para encontrar un objeto de subred. La propiedad **siteObject** del objeto subnet define el nombre del sitio que contiene el cliente. El controlador de dominio responde al ping con el nombre del sitio que contiene el cliente, junto con un indicador de si este controlador de dominio cubre ese sitio. Si el controlador de dominio no incluye ese sitio y el ubicador de DC todavía no ha intentado encontrar un controlador de dominio en ese sitio, el ubicador de DC intenta buscar de nuevo un controlador de dominio en el sitio.

Para buscar el nombre del sitio que contiene el cliente, utilice la función [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea) . Los nombres de los objetos del contenedor configuración/sitios/subred deben ser nombres de subred válidos. La función [**DsValidateSubnetName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea) indica si un nombre de subred especificado es válido.

 

 




