---
title: AccNameContainsInvalidString
description: AccNameContainsInvalidString
ms.assetid: 392E4D10-4A8E-4118-B0E7-F74571812043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681f9829f3675c469801e8f40325e83865e625b5f3496e865d1ec383c033b7f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955985"
---
# <a name="accnamecontainsinvalidstring"></a>AccNameContainsInvalidString

## <a name="text"></a>Texto

accName no debe contener la cadena {0}

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

El nombre de un elemento contiene caracteres no válidos (estos caracteres se reemplazan por AccChecker). Por ejemplo, el método [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) usado para recuperar el nombre MSAA de un elemento devuelve una cadena que contiene caracteres de tabulación, nueva línea o y comercial.

Este problema provoca problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque un elemento podría tener un nombre no reconocible y no intuitivo.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tienen un nombre o una etiqueta asignados incorrectamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propiedad Name](name-property.md)
</dt> </dl>

 

 




