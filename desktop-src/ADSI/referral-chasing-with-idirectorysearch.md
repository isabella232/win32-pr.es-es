---
title: Recomendación de referencias con IDirectorySearch
description: Una referencia es el mecanismo que usa un servidor de directorios para dirigir un cliente a otro servidor cuando no contiene suficientes datos sobre el objeto solicitado por una consulta.
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- Recomendación de referencias con IDirectorySearch ADSI
- ADSI, Búsqueda, IDirectorySearch, Otras opciones de búsqueda, Referencias de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7fcc74103c5c09816976e9ff91c17ecca8578fcbf596b731df890a350e922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690694"
---
# <a name="referral-chasing-with-idirectorysearch"></a>Recomendación de referencias con IDirectorySearch

Una referencia es el mecanismo que usa un servidor de directorios para dirigir un cliente a otro servidor cuando no contiene suficientes datos sobre el objeto solicitado por una consulta.

En una búsqueda de un nivel o subárbol, las referencias se devuelven solo para contenedores de configuración, esquema o dominio subordinados conocidos e inmediatamente. es decir, dominios secundarios que son descendientes directos. Para obtener más información, vea [Ámbito de búsqueda.](/windows/desktop/AD/search-scope)

En un directorio, no todos los datos están disponibles en un solo servidor, sino que se distribuyen entre varios servidores diferentes a través de la red. Si los servidores comparten los datos que otros servidores pueden proporcionar, pueden proporcionar referencias a un cliente cuando no se puede resolver una consulta solicitada en el servidor de origen. Por ejemplo, cuando un cliente solicita al servidor A que consulte un objeto de usuario (U), A puede sugerir que el cliente continúe la búsqueda en el servidor B si U no reside en A, pero se identifica como en B. El cliente tiene la opción de seguir la referencia o no. Las referencias liberan al cliente de tener que poseer conocimientos previos de la funcionalidad de cada servidor, pero el cliente debe especificar el tipo de referencias que debe realizar un servidor.

Para habilitar o deshabilitar la búsqueda de referencias, establezca una opción de búsqueda **\_ ADS SEARCHPREF \_ CHASE \_ REFERRALS** con un valor **DE ADSTYPE \_ INTEGER** que contenga uno de los valores de enumeración [**\_ \_ \_ ENUM DE ADS CHASE REFERRALS**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) en la matriz [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

En el ejemplo de código siguiente se muestra cómo habilitar las referencias de búsqueda.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



Para obtener más información sobre las referencias en Active Directory, vea [Referencias](/windows/desktop/AD/referrals).

 

 