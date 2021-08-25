---
description: A continuación se proporcionan algunas instancias comunes de instrucciones condicionales. Para obtener más información, vea Sintaxis de instrucciones condicionales.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Ejemplos de sintaxis de instrucciones condicionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88445e1e4b371669c43b47d1ca54e9fd677c5414985ade3908b95e00717de887
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811035"
---
# <a name="examples-of-conditional-statement-syntax"></a>Ejemplos de sintaxis de instrucciones condicionales

A continuación se proporcionan algunas instancias comunes de instrucciones condicionales. Para obtener más información, vea [Sintaxis de instrucciones condicionales.](conditional-statement-syntax.md)

## <a name="run-action-on-removal"></a>Ejecute la acción al quitarla.

Para obtener información, vea [Acciones de a acondicionador que se ejecutarán durante la eliminación.](conditioning-actions-to-run-during-removal.md)

## <a name="run-action-only-if-the-product-has-not-been-installed"></a>Ejecute la acción solo si el producto no se ha instalado.

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a>Ejecute la acción solo si el producto se instalará localmente. No ejecute ninguna acción en una reinstalación.

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

El término "&FeatureName=3" significa que la acción es instalar la característica local. El término "NOT(! FeatureName=3)" significa que la característica no está instalada localmente.

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a>Ejecute la acción solo si se desinstalará la característica.

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

Esta condición solo comprueba si hay una transición de la característica de un estado instalado de local al estado ausente.

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a>Ejecute la acción solo si el componente se instaló localmente, pero está en transición fuera de estado.

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

¿El término "? ComponetName=3" significa que el componente está instalado localmente. El término "$ComponentName=2" significa que el estado de acción en el componente es Absent. El término "$ComponentName=4" significa que el estado de acción en el componente se ejecuta desde el origen. Tenga en cuenta que un estado de acción de anuncio no es válido para un componente.

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a>Ejecute la acción solo en la reinstalación de un componente.

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a>Ejecute la acción solo cuando se aplique una revisión determinada.

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

Para obtener más información, vea la sección Comentarios de la [**página de propiedades PATCH.**](patch.md)

 

 



