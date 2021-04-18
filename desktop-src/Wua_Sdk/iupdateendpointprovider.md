---
description: Contiene el método utilizado para obtener un punto de conexión que se utiliza para conectarse a un servicio.
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: Interfaz IUpdateEndpointProvider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 81e9481f5233fac05e7fa7bdf3afa53c4c55513a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715277"
---
# <a name="iupdateendpointprovider-interface"></a>Interfaz IUpdateEndpointProvider

Contiene el método utilizado para obtener un punto de conexión que se utiliza para conectarse a un servicio. Esta interfaz se implementa al escribir un proveedor de extremos.

## <a name="members"></a>Miembros

La interfaz **IUpdateEndpointProvider** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUpdateEndpointProvider** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IUpdateEndpointProvider** tiene estos métodos.



| Método                                                                       | Descripción                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) | Solicita un extremo que se utiliza para conectarse a un servicio.<br/> |



 

## <a name="remarks"></a>Observaciones

WUA llama al método [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) para iniciar el proceso de negociación. Cuando se realiza la llamada, WUA pasa los tipos de token registrados y la implementación de esta interfaz devuelve los tipos de token que prefiere usar.

 

 
