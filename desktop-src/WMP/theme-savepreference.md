---
title: THEME.savePreference
description: El método savePreference guarda una preferencia en el Registro.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- THEME.savePreference Reproductor de Windows Media
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89633d71dd75f4ef5e804aefddc85cf00ad5c03b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465856"
---
# <a name="themesavepreference"></a>THEME.savePreference

El **método savePreference** guarda una preferencia en el Registro.

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

Cadena **que** especifica la clave del valor de preferencia que se guardará.

</dd> <dt>

<span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*theValue*
</dt> <dd>

Cadena **que** especifica el valor que se guardará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una preferencia es un par clave-valor que se puede almacenar en el Registro para conservar información sobre el estado de las Reproductor de Windows Media entre ejecuciones. Esta característica se puede usar, por ejemplo, para guardar la configuración de personalización de modo que no tenga que volver a especificarse cada vez que Reproductor de Windows Media se inicia.

Las preferencias no están cifradas y, por tanto, no son un método seguro para conservar los datos. No use preferencias para almacenar datos privados.

## <a name="examples"></a>Ejemplos


```JScript
<THEME>
  <VIEW 
    id="View1" 
    onclose="jscript:theme.savePreference('drawer1','open');
             theme.savePreference('drawer2','close')">
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO THEME**](theme-element.md)
</dt> <dt>

[**THEME.loadPreference**](theme-loadpreference.md)
</dt> </dl>

 

 





