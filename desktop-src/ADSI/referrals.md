---
title: Referencias (ADSI)
description: Las referencias se producen cuando el servidor que está consultando no contiene esos datos, pero puede encontrarlos.
ms.assetid: 2068ce7a-0b94-4d25-a18f-97f26863bd1d
ms.tgt_platform: multiple
keywords:
- ADSI de referencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e79e6b2e8a737f6bb40386effd68f7f31d8d490d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149618"
---
# <a name="referrals-adsi"></a>Referencias (ADSI)

Las referencias se producen cuando el servidor que está consultando no contiene esos datos, pero puede encontrarlos. El servidor de destino devuelve el conjunto de resultados, que puede incluir los datos reales y una referencia a otro servidor para recuperar los datos adicionales. Al habilitar el *seguimiento de referencias*, el código de cliente ADSI subyacente usará esos datos de referencia para intentar recuperar el objeto de destino del servidor descrito en los datos de referencia. Tenga en cuenta que la deshabilitación del seguimiento de la referencia puede dar lugar a un conjunto de resultados más pequeño, mientras que habilitar el seguimiento de la referencia puede hacer que una consulta abarque muchos servidores. Siempre que sea posible, la solución recomendada es usar el catálogo global.

Para obtener más información sobre las referencias y el seguimiento de referencias en Active Directory, vea [Referrals](/windows/desktop/AD/referrals).

Por ejemplo, cuando un cliente indica al servidor a (a) que consulte un objeto de usuario (U), puede sugerir que el cliente continúe la búsqueda en el servidor B (B) si U no reside en, pero se sabe que está en B. El cliente tiene la opción de proseguir con la referencia o no. Las referencias de búsqueda liberan al cliente para que requiera un reconocimiento avanzado de la capacidad de cada servidor. Sin embargo, el cliente debe especificar el tipo de referencias que debe crear un servidor.

Active Directory ofrece servicios de referencia de búsqueda. Un cliente puede elegir cualquiera de los siguientes tipos de seguimiento de referencia:

-   Nunca: el servidor no debe generar una referencia a un cliente aunque reconozca que otro servidor almacena los datos solicitados.
-   External: el servidor debe generar referencias si la solicitud se puede resolver en otro servidor de un árbol de directorios diferente. Por ejemplo, un cliente consulta "OU = sales, DC = Fabrikam, DC = COM" en el servidor "fab01" en el dominio "Fabrikam.com". Sin embargo, el objeto no pertenece a "fab01", pero se sabe que está en el servidor "arc01" en el dominio "Fabrikam.com". Por lo tanto, "fab01" hace referencia al cliente en "arc01".
-   Subordinado: el servidor debe generar referencias si la solicitud se puede resolver en un servidor cuyo nombre forme una ruta de acceso contigua desde el servidor de origen. El ámbito de búsqueda debe estar en el nivel de subárbol.

    Por ejemplo, el servidor A contiene objetos en "DC = sales, DC = Fabrikam, DC = com". El servidor B contiene objetos en "DC = Seattle, DC = sales, DC = Fabrikam, DC = com". Tenga en cuenta que el nombre del servidor B forma una ruta de acceso contigua al servidor A. Cuando un cliente se pone en contacto con el servidor A, solicita una búsqueda de subárbol en "DC = sales, DC = Fabrikam, DC = com" y especifica que la referencia sea un tipo subordinado, se produce el siguiente evento:

    -   El servidor A devuelve todos los objetos que conoce dentro de su ámbito.
    -   El servidor A informa al cliente de que los objetos de "DC = Seattle, DC = sales, DC = Fabrikam, DC = COM" se pueden encontrar en el servidor B.

    El cliente puede elegir ponerse en contacto con el servidor B. Si es así, se produce el evento siguiente:

    -   El servidor B responde con los objetos solicitados.
    -   Si el servidor B detecta otros servidores en la ruta de acceso de nomenclatura contigua y el proceso continúa.

-   Siempre: el servidor genera referencias si la búsqueda se puede resolver en función del tipo externo o del tipo subordinado.

> [!Note]  
> En Active Directory, el catálogo global contiene todos los objetos de una empresa determinada. La búsqueda de un servidor de catálogo global produce un mejor rendimiento que la realización de referencias de un servidor a otro.

 

En la mayoría de los casos, el seguimiento de la referencia será transparente para el autor de la llamada. Si la referencia es a un objeto de un dominio o bosque diferente, la API de LDAP subyacente intentará utilizar las credenciales actuales para enlazar con el destino de la referencia. Si esto se realiza correctamente, el seguimiento de la referencia será transparente. Si no se realiza correctamente, se devolverá el código de error de referencia y de referencia.

Para obtener más información sobre el uso de las opciones de búsqueda de referencias con una interfaz de búsqueda específica, vea:

-   [Referencia sobre el seguimiento con IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Buscar con Objetos de datos ActiveX](searching-with-activex-data-objects-ado.md)
-   [Buscar con OLE DB](searching-with-ole-db.md)

 

 