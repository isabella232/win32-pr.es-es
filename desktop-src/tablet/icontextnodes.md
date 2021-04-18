---
description: Contiene una colección de objetos que implementan la interfaz IContextNode y que son el resultado de una operación de análisis de tinta.
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: Interfaz IContextNodes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 306abcd32dcb0ee55978a6b95ee9f8a2c22cd19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715222"
---
# <a name="icontextnodes-interface"></a>Interfaz IContextNodes

Contiene una colección de objetos que implementan la interfaz [**IContextNode**](icontextnode.md) y que son el resultado de una operación de análisis de tinta.

## <a name="members"></a>Miembros

La interfaz **IContextNodes** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextNodes** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IContextNodes** tiene estos métodos.



| Método                                                       | Descripción                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**AddContextNode**](icontextnodes-addcontextnode.md)       | Agrega un objeto [**IContextNode**](icontextnode.md) a esta colección. <br/>                                  |
| [**GetContextNode**](icontextnodes-getcontextnode.md)       | Recupera el objeto [**IContextNode**](icontextnode.md) en el índice especificado de esta colección. <br/> |
| [**GetCount**](icontextnodes-getcount.md)                   | Recupera el número de objetos [**IContextNode**](icontextnode.md) contenidos en esta colección. <br/>       |
| [**RemoveContextNode**](icontextnodes-removecontextnode.md) | Quita un objeto [**IContextNode**](icontextnode.md) de esta colección. <br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

