---
description: A continuación se proporcionan algunas instancias comunes de instrucciones condicionales. Para obtener más información, vea sintaxis de la instrucción condicional.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Ejemplos de sintaxis de instrucciones condicionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca91a2b3e89160fad19ad5d9b1c6a3d33929e5d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001652"
---
# <a name="examples-of-conditional-statement-syntax"></a>Ejemplos de sintaxis de instrucciones condicionales

A continuación se proporcionan algunas instancias comunes de instrucciones condicionales. Para obtener más información, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).

## <a name="run-action-on-removal"></a>Ejecutar acción al quitar.

Para obtener más información, consulte [acondicionamiento de acciones para ejecutar durante la eliminación](conditioning-actions-to-run-during-removal.md).

## <a name="run-action-only-if-the-product-has-not-been-installed"></a>Ejecutar acción solo si el producto no se ha instalado.

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a>Ejecute la acción solo si el producto se va a instalar local. No ejecute la acción en una reinstalación.

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

El término "&FeatureName = 3" significa que la acción es instalar la característica local. El término "no (! FeatureName = 3) "significa que la característica no está instalada localmente.

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a>Ejecute la acción solo si se va a desinstalar la característica.

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

Esta condición solo comprueba si hay una transición de la característica de un estado instalado local al estado ausente.

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a>Ejecute la acción solo si el componente se instaló localmente, pero está pasando del estado.

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

El término "? ComponetName = 3 "significa que el componente está instalado localmente. El término "$ComponentName = 2" significa que falta el estado de la acción en el componente. El término "$ComponentName = 4" significa que el estado de la acción en el componente se ejecuta desde el origen. Tenga en cuenta que un estado de acción de anunciad no es válido para un componente.

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a>Ejecutar acción solo en la reinstalación de un componente.

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a>Ejecutar acción solo cuando se aplica una revisión determinada.

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

Para obtener más información, vea la sección Comentarios de la página de propiedades [**revisión**](patch.md) .

 

 



