---
title: THEME. loadPreference
description: El método loadPreference carga una preferencia del registro.
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- Media Player de Windows de THEME. loadPreference
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d92135113495ac32ca81f602ea5836332159164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681274"
---
# <a name="themeloadpreference"></a>THEME. loadPreference

El método **loadPreference** carga una preferencia del registro.

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

**Cadena** que especifica la clave del valor de preferencia que se va a cargar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena**.

## <a name="remarks"></a>Observaciones

Una preferencia es un par clave-valor que se puede almacenar en el registro para conservar información sobre el estado de la Media Player de Windows entre ejecuciones. Esta característica se puede usar, por ejemplo, para guardar la configuración de personalización para que no sea necesario volver a escribirla cada vez que se inicie Windows Media Player.

Las preferencias no se cifran y, por lo tanto, no son un método seguro para conservar los datos. No utilice preferencias para almacenar datos privados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME. savePreference**](theme-savepreference.md)
</dt> </dl>

 

 





