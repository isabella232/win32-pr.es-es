---
title: THEME.loadPreference
description: El método loadPreference carga una preferencia del Registro.
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- THEME.loadPreference Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258751"
---
# <a name="themeloadpreference"></a>THEME.loadPreference

El **método loadPreference** carga una preferencia del Registro.

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

Cadena **que** especifica la clave del valor de preferencia que se debe cargar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena**.

## <a name="remarks"></a>Observaciones

Una preferencia es un par clave-valor que se puede almacenar en el Registro para conservar información sobre el estado de la Reproductor de Windows Media entre ejecuciones. Esta característica se puede usar, por ejemplo, para guardar la configuración de personalización de modo que no tenga que volver a especificarse cada vez que Reproductor de Windows Media se inicia.

Las preferencias no están cifradas y, por tanto, no son un método seguro para conservar los datos. No use preferencias para almacenar datos privados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ELEMENTO THEME**](theme-element.md)
</dt> <dt>

[**THEME.savePreference**](theme-savepreference.md)
</dt> </dl>

 

 





