---
title: API de ampliación
description: La API de ampliación permite a las aplicaciones ampliar toda la pantalla o partes de la pantalla y aplicar efectos de color.
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 7e6c652c2cca8e3c5675b390e93b70ad0b522a44
ms.sourcegitcommit: 541c08d5d36109b754f39bf89e57404f007c5f63
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/08/2020
ms.locfileid: "103904388"
---
# <a name="magnification-api"></a>API de ampliación

## <a name="purpose"></a>Propósito

La API de ampliación permite a las aplicaciones ampliar toda la pantalla o partes de la pantalla y aplicar efectos de color.

## <a name="where-applicable"></a>Donde sea aplicable

Mediante el uso de la API de ampliación, los desarrolladores pueden crear aplicaciones de tecnología de asistencia basadas en Windows que amplían la pantalla y aplican efectos de color al contenido de la pantalla ampliada. En el caso de los usuarios con poca visión, el tamaño de imagen y los efectos de color más grandes pueden facilitar la visualización y el uso del equipo.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de ampliación está diseñada principalmente para desarrolladores de C y C++ que entienden la programación de Windows y que están familiarizados con los conceptos de programación de gráficos.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La versión inicial de la API de ampliación es compatible con Windows Vista y sistemas operativos posteriores. Una segunda versión agrega capacidades de ampliación de pantalla completa y se admite en Windows 8 y versiones posteriores.

La API es compatible con Magnification.dll. Para compilar la aplicación, incluya proprof. h y vincule a Amplification. lib.

> [!Note]  
> La API de ampliación no se admite en WOW64; es decir, una aplicación del ampliador de 32 bits no se ejecutará correctamente en Windows de 64 bits.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|:---|:---|
| [Introducción a la API de ampliación](magapi-intro.md)<br/> | En este tema se describe la API de ampliación y se explica cómo utilizarla en una aplicación.<br/> |
| [Referencia](entry-magapi-ref.md)<br/>  | Esta sección contiene información de referencia de la API de ampliación.<br/>|
| [Ejemplos](magapi-samples-entry.md)<br/> | En la aplicación de ejemplo siguiente se muestra cómo usar la API de ampliación para crear un ampliador de pantalla completa que amplía toda la pantalla y un ampliador en ventanas que amplía y muestra una parte de la pantalla en una ventana.<br/> |

## <a name="related-topics"></a>Temas relacionados

[Sitio web de accesibilidad de Microsoft](https://www.microsoft.com/accessibility/), [accesibilidad en Windows 10](/windows/apps/accessibility)
