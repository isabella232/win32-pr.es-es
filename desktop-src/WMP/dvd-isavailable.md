---
title: DVD. isAvailable
description: La propiedad isAvailable indica si un tipo especificado de información está disponible o se puede realizar una acción especificada. | DVD. isAvailable
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- DVD. isAvailable Windows Media Player
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088b4b6365dd60d859fda8ec563cc9c8ff8a4c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698074"
---
# <a name="dvdisavailable"></a>DVD. isAvailable

La propiedad **isavailable** indica si un tipo especificado de información está disponible o se puede realizar una acción especificada.

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a>Parámetros

*name*

**Cadena** que contiene uno de los valores siguientes.



| String     | Descripción                                                                            |
|------------|----------------------------------------------------------------------------------------|
| atrás       | Determina si el método **back** está disponible.                                   |
| discos        | Determina si el DVD está cargado.                                                  |
| dvdDecoder | Determina si el descodificador de DVD está instalado en el sistema.                             |
| resume     | Determina si el método **resume** está disponible.                                 |
| titleMenu  | Determina si el método **titleMenu** está disponible.                              |
| Menú de menús    | Determina si el método de **menú de menús** está disponible. Normalmente denominado menú raíz. |



 

## <a name="return-values"></a>Valores devueltos

Este método devuelve un **valor booleano** de solo lectura que indica si el parámetro especificado está disponible.

## <a name="remarks"></a>Observaciones

Las características de DVD de Windows Media Player no funcionarán en equipos que no tengan instalado descodificadores de DVD de terceros. Puede determinar si un descodificador está disponible llamando a **isavailable**("dvdDecoder").

Cada DVD se crea de forma diferente. Los métodos disponibles durante la reproducción y la navegación por DVD dependen de cómo se cree el DVD.

**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Versión<br/>                  | Windows Media Player para Windows XP o posterior<br/>                            |
| Archivo DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de DVD**](dvd-object.md)
</dt> </dl>

 

 





