---
description: Representa una relación entre dos objetos IContextNode.
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: Interfaz IContextLink (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df1e0d8717ba29532486277aced19f17adb1d79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715233"
---
# <a name="icontextlink-interface"></a>Interfaz IContextLink

Representa una relación entre dos objetos [**IContextNode**](icontextnode.md) .

## <a name="members"></a>Miembros

La interfaz **IContextLink** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextLink** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IContextLink** tiene estos métodos.



| Método                                                                  | Descripción                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md) | Recupera el tipo de relación que representa este **IContextLink** .<br/>                                         |
| [**GetDestinationNode**](icontextlink-getdestinationnode.md)           | Recupera el objeto [**IContextNode**](icontextnode.md) que es el destino de este **IContextLink**.<br/> |
| [**GetSourceNode**](icontextlink-getsourcenode.md)                     | Recupera el objeto [**IContextNode**](icontextnode.md) que es el origen de este **IContextLink**.<br/>      |



 

## <a name="remarks"></a>Observaciones

A continuación se presenta un ejemplo de una relación que se representa mediante un objeto **IContextLink** :

-   Cuando se usa un nodo AnalysisHint en el análisis de tinta, la operación de análisis de tinta crea un objeto **IContextLink** de tipo AnalysisHint entre el nodo de sugerencia de análisis y el nodo que contiene la escritura dentro del área de la sugerencia. El nodo de origen es el nodo de sugerencia de análisis y el nodo de destino es el nodo que contiene la escritura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Tipos de nodo de contexto](context-node-types.md)
</dt> </dl>

 

