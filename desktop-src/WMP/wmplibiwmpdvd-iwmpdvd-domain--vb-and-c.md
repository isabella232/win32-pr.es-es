---
title: Propiedad de dominio IWMPDVD
description: La propiedad domain obtiene el dominio actual del DVD.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- dominio de propiedad Reproductor de Windows Media
- domain property Reproductor de Windows Media , interfaz IWMPDVD
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
ms.openlocfilehash: b5b5f382d7c1db820905b45b924105225c0c5b55a569f85707e4e9f729e59596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000475"
---
# <a name="iwmpdvddomain-property"></a>Propiedad IWMPDVD::d omain

La **propiedad** domain obtiene el dominio actual del DVD.

## <a name="syntax"></a>Syntax


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
| <dl> <dt>firstPlay</dt> </dl>         | Realizar la inicialización predeterminada de un disco de DVD.<br/>                                                                                      |
| <dl> <dt>videoManagerMenu</dt> </dl>  | Mostrar menús para todo el disco. También se conoce como topMenu para Reproductor de Windows Media. Normalmente se denomina el menú de título o el menú superior.<br/> |
| <dl> <dt>videoTitleSetMenu</dt> </dl> | Mostrar menús para el conjunto de título actual. También se conoce como titleMenu para Reproductor de Windows Media. Normalmente se denomina menú raíz.<br/>          |
| <dl> <dt>title</dt> </dl>             | Normalmente, muestra el título actual.<br/>                                                                                                |
| <dl> <dt>stop</dt> </dl>              | El navegador de DVD está en el dominio DE DEtenerse de DVD.<br/>                                                                                          |
| <dl> <dt>Indefinido</dt> </dl>         | Reproductor de Windows Media no está en ningún dominio de DVD.<br/>                                                                                        |



 

## <a name="remarks"></a>Comentarios

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

 

 





