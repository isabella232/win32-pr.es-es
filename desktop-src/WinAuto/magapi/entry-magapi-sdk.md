---
title: API de ampliación
description: La API de ampliación permite a las aplicaciones ampliar toda la pantalla o partes de la pantalla y aplicar efectos de color.
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 2a6c7a7ffb103b39c506c41b6b7b88f82319685226aff0d479558977caa9d46b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998444"
---
# <a name="magnification-api"></a>API de ampliación

## <a name="purpose"></a>Propósito

La API de ampliación permite a las aplicaciones ampliar toda la pantalla o partes de la pantalla y aplicar efectos de color.

## <a name="where-applicable"></a>Donde sea aplicable

Mediante la API de ampliación, los desarrolladores pueden crear aplicaciones de tecnología de asistencia basadas en Windows que amplían la pantalla y aplican efectos de color al contenido de la pantalla ampliada. Para los usuarios con visión baja, el tamaño ampliado de la imagen y los efectos de color pueden ayudar a que el equipo sea más fácil de ver y usar.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de ampliación está diseñada principalmente para desarrolladores de C y C++ que entienden Windows programación y que están familiarizados con los conceptos de programación de gráficos.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La versión inicial de La API de ampliación se admite en Windows Vista y sistemas operativos posteriores. Una segunda versión agrega funcionalidades de ampliación de pantalla completa y se admite en Windows 8 y versiones posteriores.

La API es compatible con Magnification.dll. Para compilar la aplicación, incluya Ampliation.h y vincule a Ampliation.lib.

> [!Note]  
> La API de Ampliacióntion no se admite en WOW64; Es decir, una aplicación de lupa de 32 bits no se ejecutará correctamente en servidores de 64 Windows.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|:---|:---|
| [Información general de la API de ampliación](magapi-intro.md)<br/> | En este tema se describe La API de ampliación y se explica cómo usarla en una aplicación.<br/> |
| [Referencia](entry-magapi-ref.md)<br/>  | Esta sección contiene información de referencia para La API de ampliación.<br/>|
| [Ejemplos](magapi-samples-entry.md)<br/> | En la siguiente aplicación de ejemplo se muestra cómo usar La API de ampliación para crear una lupa de pantalla completa que amplía toda la pantalla y una lupa con ventanas que amplía y muestra una parte de la pantalla en una ventana.<br/> |

## <a name="related-topics"></a>Temas relacionados

[Sitio web de accesibilidad de Microsoft,](https://www.microsoft.com/accessibility/) [Accesibilidad en Windows 10](/windows/apps/accessibility)
