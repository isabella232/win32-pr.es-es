---
title: Problemas de varios subprocesos
description: Problemas de varios subprocesos
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ffd1dc3f73c33ca30ebee0072f1c5059c73f25e9e2318d384cd0c3d0dc7bc94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918535"
---
# <a name="multi-threaded-issues"></a>Problemas de varios subprocesos

OLE proporciona compatibilidad con aplicaciones multiproceso, lo que permite a las aplicaciones realizar llamadas OLE desde varios subprocesos. Esta compatibilidad multiproceso se denomina modelo de contenedor; es importante que todos los componentes OLE que usan varios subprocesos sigan este modelo. El modelo de apartamento requiere que se serializan los punteros de interfaz (mediante [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)y [**CoUnmarshalInterface)**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)cuando se pasan entre subprocesos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procesos, subprocesos y departamentos](processes--threads--and-apartments.md)
</dt> </dl>

 

 




