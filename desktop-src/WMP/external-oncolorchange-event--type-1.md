---
title: Evento external. OnColorChange (tipo 1)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | Evento external. OnColorChange (tipo 1)
ms.assetid: 45e6ec4a-e680-4d50-8fb7-410f12383eef
keywords:
- Evento external. OnColorChange (tipo 1) Windows Media Player
topic_type:
- apiref
api_name:
- External.OnColorChange Event (Type 1)
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11805cc154c60b8a765f46041f74d40929df418d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700021"
---
# <a name="externaloncolorchange-event-type-1"></a>Evento external. OnColorChange (tipo 1)

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El evento **OnColorChange** se produce cuando cambia el color de la interfaz de usuario de Windows Media Player.

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a>Valores posibles

Esta es una propiedad de solo escritura que especifica el nombre de la función en el script que Windows Media Player llama cuando se produce el evento.

## <a name="parameters"></a>Parámetros

La función que controla este evento no toma ningún parámetro.

## <a name="remarks"></a>Observaciones

Los usuarios pueden cambiar el color de la interfaz de usuario de Windows Media Player. Puede usar este evento para personalizar la apariencia de la página web hospedada para que coincida con el reproductor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





