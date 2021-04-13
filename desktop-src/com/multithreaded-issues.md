---
title: Problemas con varios subprocesos
description: Problemas con varios subprocesos
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0910e1602d00d3429bb9e4c7a1667bf8113cd659
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419214"
---
# <a name="multi-threaded-issues"></a>Problemas con varios subprocesos

OLE proporciona compatibilidad con aplicaciones multiproceso, lo que permite a las aplicaciones realizar llamadas OLE desde varios subprocesos. Esta compatibilidad con multiproceso se conoce como el modelo de apartamento, es importante que todos los componentes OLE que usan varios subprocesos sigan este modelo. El modelo de Apartamento requiere que se calculen las referencias de los punteros de interfaz (mediante [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)y [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) cuando se pasan entre subprocesos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procesos, subprocesos y apartamentos](processes--threads--and-apartments.md)
</dt> </dl>

 

 




