---
title: VIEW.size
description: El método size cambia el tamaño de VIEW en un borde especificado.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- View.size Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465915"
---
# <a name="viewsize"></a>VIEW.size

El **método size** cambia el tamaño de **VIEW** en un borde especificado.

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="handle"></span><span id="HANDLE"></span>*Manejar*
</dt> <dd>

Cadena que especifica el borde o la esquina que se va a mover al cambiar el tamaño. Esta cadena debe tener uno de los ocho valores siguientes.



| Edge   | Esquina      |
|--------|-------------|
| top    | topright    |
| right  | bottomright |
| abajo | bottomleft  |
| izquierda   | topleft     |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Normalmente se llama a este método desde dentro **de un controlador onmousedown.** Se encarga del redimensionamiento mientras se arrastra el mouse y deja de hacer el tamaño cuando se libera el botón del mouse. Si el tamaño de **view** está restringido, no puede arrastrar el mouse para cambiar el tamaño de la vista más **allá** de los límites restringidos.

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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO VIEW**](view-element.md)
</dt> </dl>

 

 





