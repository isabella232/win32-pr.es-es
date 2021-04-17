---
title: THEME. savePreference
description: El método savePreference guarda una preferencia en el registro.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- Media Player de Windows de THEME. savePreference
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709084"
---
# <a name="themesavepreference"></a>THEME. savePreference

El método **savePreference** guarda una preferencia en el registro.

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

**Cadena** que especifica la clave del valor de preferencia que se va a guardar.

</dd> <dt>

<span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*El valorque*
</dt> <dd>

**Cadena** que especifica el valor que se va a guardar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una preferencia es un par clave-valor que se puede almacenar en el registro para conservar información sobre el estado de Windows Media Player entre ejecuciones. Esta característica se puede usar, por ejemplo, para guardar la configuración de personalización para que no sea necesario volver a escribirla cada vez que se inicie Windows Media Player.

Las preferencias no se cifran y, por lo tanto, no son un método seguro para conservar los datos. No utilice preferencias para almacenar datos privados.

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
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME. loadPreference**](theme-loadpreference.md)
</dt> </dl>

 

 





