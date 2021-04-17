---
title: THEME. openDialog
description: El método openDialog abre un cuadro de diálogo de archivo.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- Media Player de Windows de THEME. openDialog
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79b9478b6b970b1d8d18b6f40975479e4755fa6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700424"
---
# <a name="themeopendialog"></a>THEME. openDialog

El método **openDialog** abre un cuadro de diálogo de archivo.

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*
</dt> <dd>

**Cadena** que especifica el tipo de cuadro de diálogo. Debe establecerse en "archivo \_ Abrir".

</dd> <dt>

<span id="parameters"></span><span id="PARAMETERS"></span>*los*
</dt> <dd>

**Cadena** que se puede utilizar para obtener información adicional. Debe establecerse en "archivos \_ ALLMEDIA".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena** que contiene la dirección URL del archivo seleccionado o "" (cadena vacía) si el usuario hace clic en Cancelar.

## <a name="remarks"></a>Observaciones

Este método se puede usar para los archivos de las unidades de disco duro locales o de las unidades de red.

## <a name="examples"></a>Ejemplos


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
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

[**Elemento THEME**](theme-element.md)
</dt> </dl>

 

 





