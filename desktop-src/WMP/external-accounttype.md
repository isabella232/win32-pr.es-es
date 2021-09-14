---
title: External.accountType
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad accountType recupera el tipo de cuenta del usuario actual.
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- External.accountType Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249638"
---
# <a name="externalaccounttype"></a>External.accountType

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad accountType** recupera el tipo de cuenta del usuario actual.

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura** que representa el tipo de cuenta. El almacén en línea define las cadenas que representan varios tipos de cuenta.

## <a name="remarks"></a>Observaciones

Esta propiedad recupera el tipo de cuenta llamando al método [IWMPContentPartner::GetContentPartnerInfo,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) que se implementa mediante el complemento de la tienda en línea. Si el usuario actual ha iniciado sesión en la tienda en línea o el complemento ha almacenado en caché las credenciales del usuario, el método **getContentPartnerInfo** puede determinar el tipo de cuenta del usuario y devolverlo a Reproductor de Windows Media. El tipo de cuenta es una cadena que Reproductor de Windows Media no interpreta. En su Reproductor de Windows Media pasa la cadena del complemento de la tienda en línea al script en la página de detección de la tienda en línea.

Si el usuario actual no ha iniciado sesión en la tienda en línea y el complemento de la tienda en línea no tiene credenciales almacenadas en caché para el usuario, esta propiedad recupera la cadena que devuelve el método **getContentPartnerInfo** en esa situación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





