---
title: Directrices de la interfaz de usuario para las extensiones de clase auxiliar NDF
description: Al compilar la clase auxiliar, tendrá que crear texto para ayudar al usuario a comprender la causa de un incidente y los posibles pasos de reparación que se pueden realizar.
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e48357ba6561ab135e2c341409c22d1edf3fb7d
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "104358455"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a>Directrices de la interfaz de usuario para las extensiones de clase auxiliar NDF

Al compilar la clase auxiliar, tendrá que crear texto para ayudar al usuario a comprender la causa de un incidente y los posibles pasos de reparación que se pueden realizar.

## <a name="root-cause-and-repair"></a>Causa raíz y reparación

Cuando se produce un incidente, aparecerá un cuadro de diálogo para informar al usuario sobre lo que ha sucedido. El texto que cree aparecerá en dos áreas independientes.

-   **Causa principal**: una breve descripción de la causa del problema. Contiene información para ayudar a un administrador o a un usuario avanzado a solucionar el problema.
-   **Reparación**: amplía la causa raíz para proporcionar más detalles sobre los pasos que puede llevar a cabo un usuario, sin que sea demasiado largo.

Cada causa o reparación raíz debe tener un título y una descripción. Se usará todo el texto antes del primer \\ carácter "n" para el título. Todo el texto que sigue al primer \\ carácter "n" (incluidos los saltos de línea posteriores) se utilizará para la descripción.

## <a name="title-guidelines"></a>Instrucciones de título

El título de una causa o reparación raíz debe seguir estas instrucciones:

-   Debe tener 128 caracteres como máximo. (se recomiendan 40 caracteres o menos).
-   No debe terminar con un punto.

## <a name="description-guidelines"></a>Instrucciones de Descripción

La descripción de una causa o reparación raíz debe seguir estas directrices:

-   Debe tener 512 caracteres como máximo.
-   Cada oración debe terminar con un punto.
-   El \\ carácter "n" se puede usar para crear un salto de línea en la descripción.

 

 




