---
title: External.viewParameters
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | External.viewParameters
ms.assetid: 0afabe35-2857-413a-a662-1a76d3fb75fe
keywords:
- External.viewParameters Reproductor de Windows Media
topic_type:
- apiref
api_name:
- External.viewParameters
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0adec580a68bd3f6b92beef1de814729848179
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241791"
---
# <a name="externalviewparameters"></a>External.viewParameters

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad viewParameters** recupera los parámetros asociados a la vista actual en Reproductor de Windows Media.

## <a name="syntax"></a>Sintaxis

**window.external.viewParameters**

## <a name="possible-values"></a>Valores posibles

Esta propiedad devuelve una cadena de solo **lectura.**

## <a name="remarks"></a>Observaciones

Esta propiedad recupera los parámetros establecidos previamente por el almacén en línea. Por ejemplo, el almacén en línea puede especificar parámetros de vista en el parámetro *ViewParams* del método [changeView](external-changeview.md) o el parámetro *Params* del [método changeViewOnlineList.](external-changeviewonlinelist.md)

Los parámetros de vista no se interpretan Reproductor de Windows Media. Se crean mediante la tienda en línea y solo tienen significado para la tienda en línea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





