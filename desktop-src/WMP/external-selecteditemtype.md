---
title: External.selectedItemType
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | External.selectedItemType
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- External.selectedItemType Reproductor de Windows Media
topic_type:
- apiref
api_name:
- External.selectedItemType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9755f66dd00947f295bdd40ea6ab79e69d655d49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241838"
---
# <a name="externalselecteditemtype"></a>External.selectedItemType

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad selectedItemType** recupera el tipo del elemento multimedia que está seleccionado actualmente en Reproductor de Windows Media.

## <a name="syntax"></a>Sintaxis

window.external.selectedItemType()

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura** que contiene una de las constantes [de ubicación de la biblioteca](library-location-constants.md).

## <a name="remarks"></a>Observaciones

Esta propiedad se usa en combinación con la **propiedad External.selectedItemID.** Por ejemplo, si **selectedItemType** es igual a CPTrackID, **selectedItemID** es el identificador de la pista seleccionada. Para obtener más información sobre cómo Reproductor de Windows Media las vistas del contenido de la tienda en línea, vea [Ubicación y elemento seleccionado.](location-and-selected-item.md)

Algunas vistas de Reproductor de Windows Media tienen un elemento multimedia determinado que está seleccionado. Por ejemplo, suponga que la vista actual representa un álbum. Un álbum es un contenedor de pistas, por lo que **selectedItemType** es igual a CPTrackID y **selectedItemID** es el identificador de la pista seleccionada. Otras vistas no tienen un elemento multimedia seleccionado. Por ejemplo, si el usuario hace clic en el nodo raíz de la tienda en línea en el control de vista de árbol, Reproductor de Windows Media muestra una página de detección proporcionada por el almacén en línea. El reproductor no muestra ningún contenedor de elementos multimedia en la interfaz de usuario del reproductor. En ese caso, **selectedItemType es** igual a UnknownLocation y **selectedItemID** es igual a la cadena vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.selectedItemID**](external-selecteditemid.md)
</dt> <dt>

[**Ubicación y elemento seleccionado**](location-and-selected-item.md)
</dt> </dl>

 

 





