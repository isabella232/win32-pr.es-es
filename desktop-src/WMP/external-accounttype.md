---
title: External. accountType
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad accountType recupera el tipo de cuenta del usuario actual.
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- Media Player de Windows externa. accountType
topic_type:
- apiref
api_name:
- External.accountType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16fce659f38af19157536a4bf763362c35fc9dfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699874"
---
# <a name="externalaccounttype"></a>External. accountType

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La propiedad **accountType** recupera el tipo de cuenta del usuario actual.

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de solo lectura que representa el tipo de cuenta. Las cadenas que representan varios tipos de cuenta se definen en la tienda en línea.

## <a name="remarks"></a>Observaciones

Esta propiedad recupera el tipo de cuenta llamando al método [IWMPContentPartner:: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) , que se implementa mediante el complemento de la tienda en línea. Si el usuario actual ha iniciado sesión en la tienda en línea o el complemento ha almacenado en caché las credenciales del usuario, el método **getContentPartnerInfo** puede determinar el tipo de cuenta del usuario y devolverlo a Windows Media Player. El tipo de cuenta es una cadena que Windows Media Player no interpreta. En su lugar, Windows Media Player pasa la cadena del complemento de la tienda en línea al script en la página de detección de la tienda en línea.

Si el usuario actual no ha iniciado sesión en la tienda en línea y el complemento de la tienda en línea no tiene credenciales almacenadas en caché para el usuario, esta propiedad recupera cualquier cadena que devuelva el método **getContentPartnerInfo** en esa situación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





