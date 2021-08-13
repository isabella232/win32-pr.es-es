---
title: Referencias (ADSI)
description: Las referencias se producen cuando el servidor que está consultando no contiene los datos, pero puede encontrarlos.
ms.assetid: 2068ce7a-0b94-4d25-a18f-97f26863bd1d
ms.tgt_platform: multiple
keywords:
- ADSI de referencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5fb6ad299c2f47efa9723857b53cf7eee5350589757153eaaae869b2c37e6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444025"
---
# <a name="referrals-adsi"></a>Referencias (ADSI)

Las referencias se producen cuando el servidor que está consultando no contiene los datos, pero puede encontrarlos. El servidor de destino devuelve el conjunto de resultados, que puede incluir los datos reales y una referencia a otro servidor para recuperar los datos adicionales. Al habilitar *la búsqueda de* referencias , el código de cliente ADSI subyacente usará los datos de referencia para intentar recuperar el objeto de destino del servidor descrito en los datos de referencia. Tenga en cuenta que la deshabilitación de la búsqueda de referencias puede dar lugar a un conjunto de resultados más pequeño, mientras que la habilitación de la búsqueda de referencias puede hacer que una consulta abarque muchos servidores. Cuando sea posible, la solución recomendada es usar el catálogo global.

Para obtener más información sobre las referencias y la búsqueda de referencias en Active Directory, vea [Referencias.](/windows/desktop/AD/referrals)

Por ejemplo, cuando un cliente indica al servidor A (A) que consulte un objeto de usuario (U), A puede sugerir que el cliente continúe la búsqueda en el servidor B (B) si U no reside en A, pero se sabe que está en B. El cliente tiene la opción de buscar la referencia o no. Las referencias de búsqueda liberan al cliente de requerir un reconocimiento avanzado de la funcionalidad de cada servidor. Sin embargo, el cliente debe especificar el tipo de referencias que debe hacer un servidor.

Active Directory servicios de referencia de búsqueda. Un cliente puede elegir cualquiera de los siguientes tipos de búsqueda de referencias:

-   Nunca: el servidor no debe generar una referencia a un cliente aunque reconozca que otro servidor almacena los datos solicitados.
-   Externo: el servidor debe generar referencias si la solicitud se puede resolver en otro servidor de un árbol de directorios diferente. Por ejemplo, un cliente consulta "OU=Sales,DC=Fabrikam,DC=COM" en el servidor "fab01" en el dominio "Fabrikam.com". Sin embargo, el objeto no pertenece a "fab01", pero se sabe que está en el servidor "arc01" en el dominio "Fabrikam.com". Por lo tanto, "fab01" hace referencia al cliente a "arc01".
-   Subordinado: el servidor debe generar referencias si la solicitud se puede resolver en un servidor cuyo nombre forma una ruta de acceso contigua desde el servidor de origen. El ámbito de búsqueda debe estar en el nivel del subárbol.

    Por ejemplo, el servidor A contiene objetos en "DC=Sales,DC=Fabrikam,DC=Com". El servidor B contiene objetos en "DC=Seattle,DC=Sales,DC=Fabrikam,DC=Com". Tenga en cuenta que el nombre del servidor B forma una ruta de acceso contigua del servidor A. Cuando un cliente se pone en contacto con el servidor A, solicita una búsqueda de subárbol en "DC=Sales,DC=Fabrikam,DC=Com" y especifica que la referencia sea un tipo subordinado, se produce el siguiente evento:

    -   El servidor A devuelve todos los objetos que conoce dentro de su ámbito.
    -   El servidor A informa al cliente de que los objetos de "DC=Seattle,DC=Sales,DC=Fabrikam,DC=COM" se pueden encontrar en el servidor B.

    El cliente puede elegir ponerse en contacto con el servidor B. Si es así, se produce el siguiente evento:

    -   El servidor B responde con los objetos solicitados.
    -   Si el servidor B detecta otros servidores en la ruta de acceso de nomenclatura contigua y el proceso continúa.

-   Siempre: el servidor genera referencias si la búsqueda se puede resolver en función del tipo externo o del tipo subordinado.

> [!Note]  
> En Active Directory, el catálogo global contiene todos los objetos de una empresa determinada. La búsqueda de un servidor de catálogo global produce un mejor rendimiento que buscar referencias de un servidor a otro.

 

En la mayoría de los casos, la búsqueda de referencias será transparente para el autor de la llamada. Si la referencia es a un objeto de un dominio o bosque diferente, la API LDAP subyacente intentará usar las credenciales actuales para enlazar al destino de la referencia. Si se realiza correctamente, la búsqueda de referencias será transparente. Si esto no se realiza correctamente, se devolverán la referencia y un código de error de referencia.

Para obtener más información sobre el uso de las opciones de búsqueda de referencias con una interfaz de búsqueda específica, consulte:

-   [Recomendación de referencias con IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Buscar con objetos ActiveX datos](searching-with-activex-data-objects-ado.md)
-   [Búsqueda con OLE DB](searching-with-ole-db.md)

 

 