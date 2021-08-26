---
description: Contiene el método utilizado para obtener un punto de conexión que se usa para conectarse a un servicio.
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
ms.openlocfilehash: 2242e30ccd64c0252d5a1ea97eedd865f9e80bee2c58f749ca6d2eabd64c6167
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896845"
---
# <a name="iupdateendpointprovider-interface"></a>Interfaz IUpdateEndpointProvider

Contiene el método utilizado para obtener un punto de conexión que se usa para conectarse a un servicio. Esta interfaz se implementa al escribir un proveedor de puntos de conexión.

## <a name="members"></a>Miembros

La **interfaz IUpdateEndpointProvider** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUpdateEndpointProvider también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IUpdateEndpointProvider** tiene estos métodos.



| Método                                                                       | Descripción                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) | Solicita un punto de conexión que se usa para conectarse a un servicio.<br/> |



 

## <a name="remarks"></a>Comentarios

WUA llama al [**método GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) para iniciar el proceso de negociación. Cuando se realiza la llamada, WUA pasa los tipos de token registrados y la implementación de esta interfaz devuelve los tipos de token que prefiere usar.

 

 
