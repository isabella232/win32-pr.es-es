---
title: InvalidRole
description: InvalidRole
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531aa9917bd68b615c2cd2457d7a24bfc4af336c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714135"
---
# <a name="invalidrole"></a>InvalidRole

## <a name="text"></a>Texto

El valor int devuelto de Get \_ accRole no es una constante de rol válida, el sistema de roles de IE \_\_\*

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento está informando de un rol de MSAA no válido. Por ejemplo, el método [**Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) devuelve un valor entero que no se asigna a una constante de rol de objeto válida (como el \_ sistema de rol \_ ListItem).

Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación, ya que los elementos se pueden identificar incorrectamente al usuario.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tiene un rol de MSAA establecido incorrectamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible:: get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Roles de objeto**](object-roles.md)
</dt> </dl>

 

 




