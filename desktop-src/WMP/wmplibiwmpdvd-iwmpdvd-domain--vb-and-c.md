---
title: Propiedad de dominio IWMPDVD
description: La propiedad domain obtiene el dominio actual del DVD.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- dominio de propiedad Reproductor de Windows Media
- domain property Reproductor de Windows Media , IWMPDVD interface
- Interfaz IWMPDVD Reproductor de Windows Media , propiedad de dominio
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073176"
---
# <a name="iwmpdvddomain-property"></a>Propiedad IWMPDVD::d omain

La **propiedad** domain obtiene el dominio actual del DVD.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es uno de los valores siguientes.



| Value                                                                                        | Significado                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>firstPlay</dt> </dl>         | Realización de la inicialización predeterminada de un disco de DVD.<br/>                                                                                      |
| <dl> <dt>videoManagerMenu</dt> </dl>  | Mostrar menús para todo el disco. También se conoce como topMenu para Reproductor de Windows Media. Normalmente se denomina el menú de título o el menú superior.<br/> |
| <dl> <dt>videoTitleSetMenu</dt> </dl> | Mostrar menús para el conjunto de títulos actual. También se conoce como titleMenu para Reproductor de Windows Media. Normalmente se denomina menú raíz.<br/>          |
| <dl> <dt>title</dt> </dl>             | Normalmente, se muestra el título actual.<br/>                                                                                                |
| <dl> <dt>stop</dt> </dl>              | El navegador de DVD está en el dominio DVD Stop.<br/>                                                                                          |
| <dl> <dt>Indefinido</dt> </dl>         | Reproductor de Windows Media no está en ningún dominio de DVD.<br/>                                                                                        |



 

## <a name="remarks"></a>Observaciones

Cada DVD se ha escrito de forma diferente. Algunos DVD no contienen los dominios firstPlay, videoManagerMenu o videoTitleSetMenu.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPDVD (VB y C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





