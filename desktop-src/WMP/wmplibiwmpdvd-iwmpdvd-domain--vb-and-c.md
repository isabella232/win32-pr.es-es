---
title: Propiedad de dominio IWMPDVD
description: La propiedad de dominio obtiene el dominio actual del DVD.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- Media Player de propiedades de dominio de Windows
- propiedad de dominio Windows Media Player, interfaz IWMPDVD
- Interfaz IWMPDVD Windows Media Player, propiedad de dominio
topic_type:
- apiref
api_name:
- IWMPDVD.domain
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6546a8288160fe80f7df4a7c41ea79a0edc905f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653911"
---
# <a name="iwmpdvddomain-property"></a>IWMPDVD::d propiedad omain

La propiedad de **dominio** obtiene el dominio actual del DVD.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System. String** que es uno de los valores siguientes.



| Value                                                                                        | Significado                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>firstPlay</dt> </dl>         | Realizar la inicialización predeterminada de un disco DVD.<br/>                                                                                      |
| <dl> <dt>videoManagerMenu</dt> </dl>  | Mostrar menús para todo el disco. También conocido como menú de Media Player para Windows. Normalmente denominado el menú de título o el menú superior.<br/> |
| <dl> <dt>videoTitleSetMenu</dt> </dl> | Mostrar los menús del conjunto de títulos actual. También conocido como titleMenu para Windows Media Player. Normalmente denominado menú raíz.<br/>          |
| <dl> <dt>title</dt> </dl>             | Normalmente, mostrando el título actual.<br/>                                                                                                |
| <dl> <dt>stop</dt> </dl>              | El navegador de DVD está en el dominio de detención de DVD.<br/>                                                                                          |
| <dl> <dt>indefinido</dt> </dl>         | Windows Media Player no está en ningún dominio de DVD.<br/>                                                                                        |



 

## <a name="remarks"></a>Observaciones

Cada DVD se crea de forma diferente. Algunos DVDs no contienen los dominios firstPlay, videoManagerMenu o videoTitleSetMenu.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPDVD (VB y C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





