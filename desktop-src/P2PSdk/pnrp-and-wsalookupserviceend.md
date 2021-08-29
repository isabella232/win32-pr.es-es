---
description: PNRP usa la función WSALookupServiceEnd para hacer lo siguiente.
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP y WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9d91dea87b5a8c41cb5f689d89464bf7fd7e0179b1cad71943c14d107842b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553385"
---
# <a name="pnrp-and-wsalookupserviceend"></a>PNRP y WSALookupServiceEnd

PNRP usa la [**función WSALookupServiceEnd**](winsock-nsp-reference-links.md) para hacer lo siguiente:

-   Finalizar una consulta iniciada en una llamada anterior a [ **WSALookupServiceBegin**](winsock-nsp-reference-links.md)
-   Desbloquear una llamada a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) para detener la búsqueda

Una llamada a [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) finaliza una consulta y limpia el contexto. El identificador obtenido de una llamada a **WSALookupServiceBegin** debe pasarse como parámetro a **WSALookupServiceEnd**.

Para obtener más información sobre PNRP y la función [**WSALookupServiceBegin,**](winsock-nsp-reference-links.md) vea [PNRP y WSALookupServiceBegin.](pnrp-and-wsalookupservicebegin.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[PNRP y WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[Códigos de error de PNRP NSP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSALookupServiceNext**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



