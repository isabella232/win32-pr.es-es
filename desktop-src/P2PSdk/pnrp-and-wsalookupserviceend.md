---
description: PNRP usa la función WSALookupServiceEnd para hacer lo siguiente.
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP y WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db499c9a736e26d630b623a29baa4c18dcfceeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667929"
---
# <a name="pnrp-and-wsalookupserviceend"></a>PNRP y WSALookupServiceEnd

PNRP usa la función [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) para hacer lo siguiente:

-   Finalizar una consulta iniciada en una llamada anterior a [ **WSALookupServiceBegin**](winsock-nsp-reference-links.md)
-   Desbloquear una llamada a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) para detener la búsqueda

Una llamada a [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) finaliza una consulta y limpia el contexto. El identificador obtenido a partir de una llamada a **WSALookupServiceBegin** se debe pasar como un parámetro a **WSALookupServiceEnd**.

Para obtener más información acerca de PNRP y la función [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) , consulte [PNRP y WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[PNRP y WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[Códigos de error NSP de PNRP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSALookupServiceNext**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



