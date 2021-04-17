---
title: VISTA. tamaño
description: El método size cambia el tamaño de la vista en un borde especificado.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- VISTA. tamaño de Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: def9b416dfe5eda052ef430b587fa1c6017b4e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708274"
---
# <a name="viewsize"></a>VISTA. tamaño

El método **size cambia** el tamaño de la **vista** en un borde especificado.

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="handle"></span><span id="HANDLE"></span>*asa*
</dt> <dd>

Cadena que especifica el borde o la esquina que se va a desplace al ajustar el tamaño. Esta cadena debe tener uno de los ocho valores siguientes.



| Edge   | Esquina      |
|--------|-------------|
| top    | esquina superior    |
| right  | PivotDetailRange |
| abajo | bottomleft  |
| izquierda   | a la izquierda     |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Normalmente, este método se llama desde dentro de un controlador **OnMouseDown** . Se encarga del cambio de tamaño mientras se arrastra el mouse y se detiene el cambio de tamaño cuando se suelta el botón del mouse. Si el tamaño de la **vista** está restringido, no puede arrastrar el mouse para cambiar el tamaño de la **vista** más allá de los límites restringidos.

## <a name="examples"></a>Ejemplos


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="sizer" horizontalAlignment="right" 
        verticalAlignment="bottom" image="Open.png" 
        onmousedown="jscript:View1.size('bottomright')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de vista**](view-element.md)
</dt> </dl>

 

 





