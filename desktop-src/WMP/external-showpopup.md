---
title: Método External.showPopup
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Método External.showPopup
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- Método showPopup Reproductor de Windows Media
- método showPopup Reproductor de Windows Media , Clase externa
- Clase externa Reproductor de Windows Media , método showPopup
topic_type:
- apiref
api_name:
- External.showPopup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a651add93e32c1c2eb82827a4089a338341f2506ba26d9fbb06061aa6d185d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648354"
---
# <a name="externalshowpopup-method"></a>Método External.showPopup

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método showPopup** indica a Reproductor de Windows Media que muestre una página web emergente; es decir, una página web que aparece en una ventana independiente.

## <a name="syntax"></a>Sintaxis


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PopupIndex* \[ En\]
</dt> <dd>

**Number** (**long**) que especifica el índice de la página web emergente.

</dd> <dt>

*Parámetros* \[ En\]
</dt> <dd>

**Cadena** que Reproductor de Windows Media anexa a la dirección URL de la página web.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El índice emergente no se interpreta mediante Reproductor de Windows Media. Los índices que identifican las páginas web emergentes se crean mediante la tienda en línea y solo tienen significado para la tienda en línea.

Los pasos siguientes muestran cómo Reproductor de Windows Media los parámetros del **método showPopup** para crear una dirección URL para la ventana emergente.

1.  El script de una página de detección llama a **showPopup**, pasando un entero en *PopupIndex* y una cadena en *Parameters*.

2.  Reproductor de Windows Media pasa el índice a [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) para recuperar la dirección URL de la página web que se va a mostrar.

3.  Reproductor de Windows Media parámetros a *la* dirección URL como una cadena de consulta. Por ejemplo, si **GetItemInfo** devuelve " " y parameters es igual a https://www.Proseware.com/Pages/Popup1.htm "DlgX=800&DlgY=400&Greeting=Hi", Reproductor de Windows Media crea la siguiente dirección URL: 

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

Puede usar *Parámetros para* especificar el tamaño de la ventana emergente. Por ejemplo, si establece *Parámetros* en "DlgX=800&DlgY=400", la ventana emergente tendrá un tamaño de 800 píxeles por 400 píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





