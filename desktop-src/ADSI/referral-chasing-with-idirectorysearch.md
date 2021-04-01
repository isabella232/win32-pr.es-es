---
title: Referencia sobre el seguimiento con IDirectorySearch
description: Una referencia es el mecanismo que utiliza un servidor de directorio para dirigir un cliente a otro servidor cuando no contiene suficientes datos sobre el objeto solicitado por una consulta.
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- Referencia sobre el seguimiento con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, seguimiento de referencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae76139dc1a68c9345cd7a7b3bb894a50a2d7b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995627"
---
# <a name="referral-chasing-with-idirectorysearch"></a>Referencia sobre el seguimiento con IDirectorySearch

Una referencia es el mecanismo que utiliza un servidor de directorio para dirigir un cliente a otro servidor cuando no contiene suficientes datos sobre el objeto solicitado por una consulta.

En una búsqueda de un solo nivel o de subárbol, las referencias se devuelven para los contenedores de dominio, esquema o configuración de solo subordinados inmediatos. es decir, dominios secundarios que son descendientes directos. Para obtener más información, vea [ámbito de búsqueda](/windows/desktop/AD/search-scope).

En un directorio, no todos los datos están disponibles en un solo servidor, sino que se distribuyen a través de varios servidores diferentes a través de la red. Si los servidores comparten los datos que otros servidores pueden proporcionar, pueden proporcionar referencias a un cliente cuando una consulta solicitada no se puede resolver en el servidor de origen. Por ejemplo, cuando un cliente pide al servidor a que consulte un objeto de usuario (U), puede sugerir que el cliente continúe la búsqueda en el servidor B si U no reside en, pero se identifica como en B. El cliente tiene la opción de llevar a cabo la referencia o no. Las referencias liberan al cliente de tener que poseer el conocimiento anterior de la capacidad de cada servidor, pero el cliente debe especificar el tipo de referencias que debe realizar un servidor.

Para habilitar o deshabilitar el seguimiento de la referencia, establezca una opción de búsqueda de referencias **\_ SEARCHPREF de \_ \_ seguimiento de ADS** con un valor **\_ entero de ADSTYPE** que contenga uno de los valores de enumeración de las referencias de [**\_ seguimiento \_ \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) de anuncios en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

En el ejemplo de código siguiente se muestra cómo habilitar las referencias de seguimiento.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



Para obtener más información sobre las referencias en Active Directory, vea [Referrals](/windows/desktop/AD/referrals).

 

 