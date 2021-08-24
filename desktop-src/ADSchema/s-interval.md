---
title: Sintaxis de intervalo
description: Representa un valor de intervalo de tiempo.
ms.assetid: e41b71da-cd05-4a4a-8b97-9210dbe314de
ms.tgt_platform: multiple
keywords:
- Esquema de AD de sintaxis de intervalo
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e088c8347ff12172cb87c521e049e2646a0711e1eaedf805887b6988af1e284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580295"
---
# <a name="interval-syntax"></a>Sintaxis de intervalo

Representa un valor de intervalo de tiempo. Las unidades de tiempo reales dependen del atributo que usa esta sintaxis. Esta sintaxis es idéntica a la [**sintaxis LargeInteger,**](s-largeinteger.md) salvo que los valores altos y bajos son enteros sin signo.



| Entrada | Valor |
|--------------|------------------------------------------------------------------------------------|
| Nombre         | Intervalo                                                                           |
| Identificador de sintaxis    | 2.5.5.16                                                                           |
| Id. de OM        | 65                                                                                 |
| Tipo DE MAPI    | \-                                                                                 |
| ADS Type     | ADSTYPE \_ LARGE \_ INTEGER                                                            |
| Tipo de variante | VT \_ DISPATCH                                                                       |
| Tipo sds     | Objeto COM que se puede convertir en [**un IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger). |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger)
</dt> <dt>

[**LargeInteger**](s-largeinteger.md)
</dt> </dl>

 

 
