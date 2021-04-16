---
title: External. viewParameters
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. viewParameters
ms.assetid: 0afabe35-2857-413a-a662-1a76d3fb75fe
keywords:
- Media Player de Windows externa. viewParameters
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699718"
---
# <a name="externalviewparameters"></a>External. viewParameters

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La propiedad **viewParameters** recupera los parámetros asociados a la vista actual en Windows Media Player.

## <a name="syntax"></a>Sintaxis

**Window. external. viewParameters**

## <a name="possible-values"></a>Valores posibles

Esta propiedad devuelve una **cadena** de solo lectura.

## <a name="remarks"></a>Observaciones

Esta propiedad recupera los parámetros que se establecieron previamente en la tienda en línea. Por ejemplo, la tienda en línea puede especificar parámetros de vista en el parámetro *ViewParams* del método [changeView](external-changeview.md) o el parámetro *params* del método [changeViewOnlineList](external-changeviewonlinelist.md) .

Los parámetros de vista no se interpretan en Windows Media Player. Los crea la tienda en línea y solo tienen significado en la tienda en línea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





