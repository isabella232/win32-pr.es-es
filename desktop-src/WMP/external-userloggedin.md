---
title: External.userLoggedIn
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | External.userLoggedIn
ms.assetid: d02d9486-c692-4f46-bc29-f0aaa45cad0f
keywords:
- External.userLoggedIn Reproductor de Windows Media
topic_type:
- apiref
api_name:
- External.userLoggedIn
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5454dd9d2fa2d771005448a4157c33b5634a30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241803"
---
# <a name="externaluserloggedin"></a>External.userLoggedIn

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad userLoggedIn** recupera un valor que indica si el usuario ha iniciado sesión en la tienda en línea.

## <a name="syntax"></a>Sintaxis

``` syntax
window.external.userLoggedIn
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un booleano de solo **lectura.** **TRUE** indica que el usuario ha iniciado sesión y **FALSE** indica que el usuario ha cerrado la sesión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**Evento External.OnLoginChange**](external-onloginchange-event.md)
</dt> </dl>

 

 





