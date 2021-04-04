---
title: Interfaz ISearchResult (WdsSharedIDL. h)
description: Expone información y propiedades sobre el conjunto de resultados.
ms.assetid: 2f50b9d7-f6fd-481c-a5db-d622a7b02017
keywords:
- Interfaz ISearchResult características del entorno heredado de Windows
- Interfaz ISearchResult características del entorno heredado de Windows, descritas
topic_type:
- apiref
api_name:
- ISearchResult
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89387ebe02c87ca6a5c5ac663a67ea060bd78948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802882"
---
# <a name="isearchresult-interface"></a>Interfaz ISearchResult

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Expone información y propiedades sobre el conjunto de resultados.

## <a name="members"></a>Miembros

La interfaz **ISearchResult** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ISearchResult** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ISearchResult** tiene estos métodos.



| Método                                                            | Descripción                 |
|:------------------------------------------------------------------|:----------------------------|
| [**Disponibilidad**](-search-2x-isearchresult-availability.md)     | Sin implementar.<br/> |
| [**Doverb**](-search-2x-isearchresult-doverb.md)                 | Sin implementar.<br/> |
| [**GetIcon**](-search-2x-isearchresult-geticon.md)               | Sin implementar.<br/> |
| [**GetThumbnail**](-search-2x-isearchresult-getthumbnail.md)     | Sin implementar.<br/> |
| [**GetValue**](-search-2x-isearchresult-getvalue.md)             | Sin implementar.<br/> |
| [**GetVerb**](-search-2x-isearchresult-getverb.md)               | Sin implementar.<br/> |
| [**IconCount**](-search-2x-isearchresult-iconcount.md)           | Sin implementar.<br/> |
| [**Ajustar**](-search-2x-isearchresult-index.md)                   | Sin implementar.<br/> |
| [**LoadState**](-search-2x-isearchresult-loadstate.md)           | Sin implementar.<br/> |
| [**Controlador de vista previa**](-search-2x-isearchresult-previewer.md)           | Sin implementar.<br/> |
| [**PutValue**](-search-2x-isearchresult-putvalue.md)             | Sin implementar.<br/> |
| [**ThumbnailState**](-search-2x-isearchresult-thumbnailstate.md) | Sin implementar.<br/> |
| [**Tipo**](-search-2x-isearchresult-type.md)                     | Sin implementar.<br/> |
| [**VerbCount**](-search-2x-isearchresult-verbcount.md)           | Sin implementar.<br/> |



 

## <a name="remarks"></a>Observaciones

Estos métodos exponen propiedades y acciones aplicables al conjunto de resultados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>                                               |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

