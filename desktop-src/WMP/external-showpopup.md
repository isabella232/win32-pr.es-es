---
title: External. showPopup (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. showPopup (método)
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- showPopup (método) de Windows Media Player
- showPopup (método) Windows Media Player, clase externa
- Clase externa Windows Media Player, método showPopup
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
ms.openlocfilehash: acaecb559e7df60067e89ec754ec9432233500f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699414"
---
# <a name="externalshowpopup-method"></a>External. showPopup (método)

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **ShowPopup** indica a Windows Media Player que muestre una página web emergente; es decir, una página web que aparece en una ventana independiente.

## <a name="syntax"></a>Sintaxis


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PopupIndex* \[ de\]
</dt> <dd>

**Número** (**Long**) que especifica el índice de la página web emergente.

</dd> <dt>

*Parámetros* \[ de de\]
</dt> <dd>

**Cadena** que Windows Media Player anexa a la dirección URL de la Página Web.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Windows Media Player no interpreta el índice emergente. Los índices que identifican las páginas web emergentes se crean en la tienda en línea y solo tienen significado en la tienda en línea.

En los pasos siguientes se muestra cómo Windows Media Player utiliza los parámetros del método **ShowPopup** para crear una dirección URL para la ventana emergente.

1.  El script de una página de detección llama a **ShowPopup**, pasando un entero en *PopupIndex* y una cadena en *parámetros*.

2.  Windows Media Player pasa el índice a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) para recuperar la dirección URL de la página web que se va a mostrar.

3.  Windows Media Player anexa *parámetros* a la dirección URL como una cadena de consulta. Por ejemplo, si **GetItemInfo** devuelve " https://www.Proseware.com/Pages/Popup1.htm " y *los parámetros* son iguales a "DlgX = 800&DlgY = 400&Greeting = HI", Windows Media Player crea la siguiente dirección URL:

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

Puede usar *parámetros* para especificar el tamaño de la ventana emergente. Por ejemplo, si establece *los parámetros* en "DlgX = 800&DlgY = 400", la ventana emergente tendrá un tamaño de 800 píxeles por 400 píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





